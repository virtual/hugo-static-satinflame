---
title: "Setting Up A Multi Website Magento Store"
date: 2017-03-04T09:37:25-06:00
banner: "img/banners/magento-1-1024x493.png"
tags: ["programming", "magento"]
categories: ["blog"]
authors:
  - jeanine
excerpt: "Though there is a lot to learn, understanding the file structure of Magento is essential in order to migrate a store into a multi-website for an upgraded store. Here is an overview of the steps to migrate a second store into Magento."
---



Last year I had the opportunity to learn about working in the e-commerce platform Magento–creating products, adding modules, updating security patches and more. Though there is a lot to learn, understanding the file structure of Magento was essential in order to migrate another store (running version 1.4) into a multi-website for another store that had been recently upgraded to 1.9.2\. While searching for the best process, I learned there are many ways to set up a second store on the same Magento install—but there were many things I still didn’t understand being the novice server administer of a one-person web team.

Below is an overview of the steps I took to migrate a second store into Magento; please note that this is not an exhaustive list but an overview to point you in the direction of which parts you may need to learn more about.

Add second website to Magento
---------------------

There are many guides that cover this including [How To Setup Multiple Stores On Magento](https://www.cloudways.com/blog/how-to-setup-multiple-stores-on-magento/). Be sure to understand the difference between a website, store and language. Separate websites can reference the same products and CMS pages, but they are typically used for completely different product catalogs. Set up your categories and website from the store settings, keeping the website code in mind, as you will want to make this consistent in your settings. Try it out now and [set up your second store.](https://www.cloudways.com/blog/how-to-setup-multiple-stores-on-magento/)



## Modify server to accommodate multiple Magento websites



To me, the most daunting part of adding a new website to an existing Magento install was the fear of making an error that would take down the current website. After testing with local web servers, here are the steps I took on our Apache server (running Debian 7×64):



### Update DNS settings



From your second domain (or a test domain) update the CNAME/A name to point to the server address of your primary Magento website. For example, my setup looks like this:

**Store2 Advanced DNS (A Records)**

Host |	TTL	Numeric | IP
--------|----|-----
www	| 7200	| 192.168.x.x
@ (None)	| 7200	| 192.168.x.x
* (All Others)	| 7200	| 192.168.x.x

### Add to your virtual hosts

Add your second domain to sites-available on your server. Once you are satisfied with the setup, you can run aen2mod enabled, to enable to the second domain on your server. Ensure your server is using Named Virtual Hosts.

**Test apache server config prior to restarting:**

`/usr/sbin/apachectl configtest`

**Restart:**

`sudo service apache2 restart`

## Update primary website web files

In order to use shared themes between websites with minimal changes, it is best to centralize any settings that are the same between your websites, and only override the default themes as necessary using a local theme. I found it easiest to copy the local theme, rename it to match your website id and update the styles and HTML only when needed.

### Support secondary website and multiple themes

Copy the local design files (which override your default design theme) and rename the copied folders to match your website code.

*   app\design\frontend
*   skin\frontend
*   skin\frontend\THEME

### Redirect incoming requests to the appropriate store

When typing in your primary or secondary website URL, the server must have a way to decide which files to use. In addition to the updates you made when setting up your second website, you must include web store codes in your index.php or [.htaccess file](https://www.hostknox.com/tutorials/magento/multistore). Here is how I’ve set mine up:

**index.php:**

```php
<?php 
/* Store or website code */  
$mageRunCode = isset($_SERVER['MAGE_RUN_CODE']) ? $_SERVER['MAGE_RUN_CODE'] : '';  
/* Run store or run website */  
$mageRunType = isset($_SERVER['MAGE_RUN_TYPE']) ? $_SERVER['MAGE_RUN_TYPE'] : 'website';

switch($_SERVER['HTTP_HOST']) {  
  case 'store1.com':  
  case 'www.store1.com':  
  $mageRunCode = 'store1';  
  $mageRunType = 'website';  
  break;  
  case 'store2.com':  
  case 'www.store2.com':  
  $mageRunCode = 'store2';  
  $mageRunType = 'website';  
  break;  
}  
Mage::run($mageRunCode, $mageRunType);
``` 

## Additional Magento updates

### Share pages when applicable

Visit each CMS page and/or static block from your install and update the store permissions as necessary. Be sure to notice the selection to apply to “All stores” (versus selecting both stores) as this will keep your pages available to a third website if you ever do add one.

### Point design settings to a copy of local design files

Update the Design settings to point to this second website theme for overrides as needed.

**Store2 Website:**

*   Config > General > Web > Base URL update (http://magentostore2.local/)
*   Default Pages: store2_home
*   Config > General > Design > change “store1” to “store2”

**HTML Head**

Header: images/store2.png

http://magentostore2.local/ (or similar) should now load an basic page similar to that of Store1.

### Use store variables

If you find that your pages are very similar aside from the occasional store name sprinkled in, you can update your page to use a site variable (e.g. reference the Store name variable) instead of using text. This allows a page to display the name of the store it is referenced from so you only have to maintain one page for two websites.

## Other considerations

### SSL

If you are already using an SSL certificate, simply copy this code into a new sites-available similar to how you added the second website previously. However the code for the SSL should be within the `<:443>` module.

### Restricting your second website for testing

In order to restrict viewing of your second website to your IP only, use the <Location /> within the sites-available. (The [developer IPs in the Magento admin settings are NOT for restricting access](http://magento.stackexchange.com/questions/4564/setting-up-magento-staging-environment-with-restricted-access)!) Here is an example of my full sites-enabled code including the `<Location />` tag. When you are ready for the world to see your second website, remove the entire `<Location />` block. Restart your server after testing and making changes.

**sites-available/secondstore:**
```.htaccess
<Location />  
Order deny,allow  
Deny from all  
Allow from 174.45.x.x  
</Location> 
```
### Import/Export

Although I did a lot of development testing using MAGMI, I ended up recreating the products from scratch on my second website. The easiest way to do this is to create your configurable product and then create the Associated Products using the Quick-Create. You can then go back and fill in all product information on the parent product as necessary.

To transfer customers, I was able to use the built-in [Import and Export functions for Magento](https://www.templatemonster.com/help/magento-how-to-exportimport-data-in-csv-files.html#gref). For orders and sales, I found [Aitoc Orders Export and Import](https://www.aitoc.com/en/magentomods_orders_export_and_import.html) to be extremely efficient. Since you are adding sales and orders into an existing system, be sure to update the order IDs to start with 20000 instead of 10000 using find replace on any exported CSV files. After you’ve finished, you must update your indexes so they are ready for new orders.

## Additional Resources:

*   [No Frills Magento Layout by Alan Storm](http://store.pulsestorm.net/products/no-frills-magento-layout)
*   [Magento Multi-Website Checklist](http://www.eddiemay.me.uk/2013/08/10/magento-multi-website-checklist/)
*   [How To Setup Multiple Stores On Magento](https://www.cloudways.com/blog/how-to-setup-multiple-stores-on-magento/)