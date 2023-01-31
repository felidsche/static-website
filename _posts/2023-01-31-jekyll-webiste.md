---
layout: post
title: Install and deploy a Jekyll website
date: 2023-01-31 19:00:00-0000
description: How to deploy a Jekyll website to GitHub pages for Ruby newbies
categories: blog-posts
tags: code
giscus_comments: true
---

- OS: Ubuntu 22.04.1 LTS

## Update the apt package manager
`sudo apt update && upgrade -y`
## Install a Ruby version manager for this project
```
sudo apt install rbenv
rbenv init
```
## reload or restart the shell
`source ~/.bashrc`
## install `ruby-build` for a simplified ruby installation as an `rbenv` plugin
```
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
git -C "$(rbenv root)"/plugins/ruby-build pull
```
## install your prefered Ruby version (I used `3.1.2`):
`rbenv install X.X.X`
## Set a Ruby version to finish and start using Ruby
```
rbenv global 3.1.2   # set the default Ruby version for this machine
# or:
rbenv local 3.1.2    # set the Ruby version for this directory
```
## Install the `bundler` gem
`gem install bundler`
## Fork the Jekyll theme from github.com:alshedivat/al-folio to github.com:<your-username>/<your-username.github.io>
## Setup your theme
```
cd <your-repo-name>
bundle install
bundle exec jekyll serve
```
## Customize the theme (e.g. using VS Code)
`code .`
- Tip: You can navigate to http://127.0.0.1:4000/al-folio/ to see your portfolio. Refresh to see changes.

## Sources
1. [rbenv README](https://github.com/rbenv/rbenv/#readme)
2. [ruby-build README](https://github.com/rbenv/ruby-build#readme)
3. [al-folio README](https://github.com/alshedivat/al-folio#readme)