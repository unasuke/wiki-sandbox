---
title: "Resources - Itamae wiki (WIP)"
---

## Resource Type

- [directory resource](/directory-resource)
- [execute resource](/execute-resource)
- [file resource](/file-resource)
- [gem_package resource](/gem_package-resource)
- [git resource](/git-resource)
- [group resource](/group-resource)
- [http_request resource](/http_request-resource)
- [link resource](/link-resource)
- [local_ruby_block resource](/local_ruby_block-resource)
- [package resource](/package-resource)
- [remote_directory resource](/remote_directory-resource)
- [remote_file resource](/remote_file-resource)
- [service resource](/service-resource)
- [template resource](/template-resource)
- [user resource](/user-resource)

## Common Attributes

All resource types have the following common attributes.

- `action`
  - Symbol or Array
  - If you would like to execute multiple actions, the action can be an Array of Symbols.
- `only_if`
  - String
  - If `only_if` command exits with non-zero status, the resource will not be executed.
- `not_if`
  - String
  - If `not_if` command exits with zero status, the resource will not be executed.
- `notifies`
  - `notifies :action, resource_type[resource_name]", :delayed` (`:delayed` is a default value)
  - `notifies :action, resource_type[resource_name]", :immediately`
- `subscribes`
  - `subscribes :action, resource_type[resource_name]", :delayed` (`:delayed` is a default value)
  - `subscribes :action, resource_type[resource_name]", :immediately`
- `user`
  - String
  - If you specified this, commands related with the resource will be executed as the user.

***

_Do not edit this page because this is generated automatically with Itamae v1.12.3_
