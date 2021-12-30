---
title: "Recipe Plugins - Itamae wiki (WIP)"
---

Itamae supports recipes in rubygems. You can create recipe gem and control dependencies with Bundler.

## Create a gem

The gem name must be `itamae-plugin-recipe-yourrecipe` like `itamae-plugin-recipe-nginx`.

## Add dependency to Gemfile

```ruby
gem 'itamae-plugin-recipe-nginx'
```

## Include recipes

Then, you can load the recipe file in gems by `include_recipe`

```ruby
# To include recipe at lib/itamae/plugin/recipe/nginx/default.rb or lib/itamae/plugin/recipe/nginx.rb
# default.rb is preferred location but it requires Itamae v1.5.2 or later
include_recipe 'nginx'

# To include recipe at lib/itamae/plugin/recipe/nginx/debug.rb
include_recipe 'nginx::debug'
```
