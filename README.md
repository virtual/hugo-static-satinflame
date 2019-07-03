# hugo-static-satinflame
Rebuilt portfolio using gohugo.io

## Development
- Install Hugo: `brew install hugo`
- Install [Universal Theme](https://github.com/devcows/hugo-universal-theme): `cd themes`
- `git clone https://github.com/devcows/hugo-universal-theme`

## Run
- Run server from project root: `hugo server`

## Build site
- [Hugo command](https://gohugo.io/commands/hugo/): `hugo`
- `gulp build` to compress HTML
- commit to git repo
- Add remote: `git remote add githubio https://github.com/virtual/virtual.github.io.git`
- Push to [github page](https://github.com/virtual/virtual.github.io): `git subtree push --prefix docs githubio master`

## New Post
- `hugo new blog/my-post-name.md`
- `hugo server -D` (show drafts)