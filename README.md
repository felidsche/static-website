# My personal website
- `*.md` files are editable and `*.html` files are generated
## Structure
- `_config.yml`
  - the main config file
- `_posts/*.md`
  - the blog posts live here

## Development
- start a dev server
`bundle exec jekyll serve`

## Deployment
- `bundle exec jekyll build --lsi`
- which will (re-)generate the static webpage in the _site/ folder. Then simply copy the contents of the _site/ directory to your hosting server.