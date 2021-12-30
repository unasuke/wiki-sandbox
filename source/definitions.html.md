---
title: "Definitions - Itamae wiki (WIP)"
---

Itamae has Chef-like _definitions_ feature.

You can define _definition_ with a collection of multiple resources, like:

```ruby
define :install_and_enable_package, version: nil do
  v = params[:version]
  package params[:name] do
    version v if v
    action :install
  end

  service params[:name] do
    action :enable
  end
end
```

Then, you can use it:

```ruby
install_and_enable_package 'nginx' do
  version '1.6.1'
end
```

Note that a `define` should be done before using the defined resource.
