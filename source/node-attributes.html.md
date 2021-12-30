---
title: "Node Attributes - Itamae wiki (WIP)"
---

You can pass node-specific attributes to Itamae by `--node-json` option.

Example
-------

```
$ cat node.json
{"name": "app-1"}
```

```
$ cat template.erb
<%= node[:name] %>
```

```
$ cat recipe.rb
execute "hostname #{node[:name]}"
template "/path/to/dest" do
  source "template.erb"
end
```

```
$ itamae local --node-json node.json recipe.rb
```
