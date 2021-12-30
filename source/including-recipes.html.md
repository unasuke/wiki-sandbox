---
title: "Including Recipes - Itamae wiki (WIP)"
---

You can include a recipe in other recipe.

```ruby
include_recipe "/path/to/recipe.rb"

# You can include a recipe by relative path.
# This relative path is resolved from a directory that including recipe exists.
include_recipe "../recipe.rb"
```

[You can also include recipes in rubygems.](https://github.com/itamae-kitchen/itamae/wiki/Recipe-Plugins)
