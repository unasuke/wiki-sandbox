---
title: "Best Practice - Itamae wiki (WIP)"
---

Itamae doesn't force users to use on a specific way. This is just recommendation.

## Directory Structure

```
.
├── cookbooks
│   └── nginx
│       ├── default.rb
│       ├── files
│       │   └── etc
│       │       └── nginx
│       │           └── conf.d
│       │               └── static.conf
│       └── templates
│           └── etc
│               └── nginx
│                   └── conf.d
│                       └── dynamic.conf
└── roles
    └── web.rb
```

- A "cookbook" is a collection of recipes and typically manages specific software or middleware.
- A "role" is role of a server such as web, db and proxy server.

`cookbooks/nginx/default.rb`:

```ruby
package "nginx"

remote_file "/etc/nginx/conf.d/static.conf"
template "/etc/nginx/conf.d/dynamic.conf"
```

`roles/web.rb`:

```ruby
include_recipe "../cookbooks/nginx"
```

Then, you can provision your server:

```
itamae local roles/web.rb
# (or) itamae ssh
```

## Use `source :auto` for remote_file and template resources.

`remote_file` and `template` resources have `source` attribute which indicates where the source file or template exists. If `source` is set to `:auto` or is not set any value (`:auto` is default value), Itamae will find source file automatically. This is recommended way.

```ruby
# .
# ├── recipe.rb
# ├── files
# │   └── etc
# │       └── nginx
# │           └── conf.d
# │               └── static.conf
# └── templates
#     └── etc
#         └── nginx
#             └── conf.d
#                 └── dynamic.conf

# recipe.rb
remote_file "/etc/nginx/conf.d/static.conf"
template "/etc/nginx/conf.d/dynamic.conf"
```

If `source` of `remote_file` resource is `:auto` and `path` is `/foo/bar/baz.conf`, Itamae will search files from top to bottom of the following list.

- files/foo/bar/baz.conf (most recommended)
- files/bar/baz.conf
- files/baz.conf

If `source` of `template` resource is `:auto` and `path` is `/foo/bar/baz.conf`, Itamae will search files from top to bottom of the following list.

- templates/foo/bar/baz.conf.erb (most recommended)
- templates/foo/bar/baz.conf
- templates/bar/baz.conf.erb
- templates/bar/baz.conf
- templates/baz.conf.erb
- templates/baz.conf

## Use node.validate! in recipes that will be included.

```ruby
node.validate! do
  {
    nginx: {
      user: string, # required field
      worker_processes: optional(integer), # optional field
      sites: array_of({
        server_name: string,
        root: string,
        allowed_ips: array_of(string),
      }),
    },
  }
end

# valid example
{
  nginx: {
    user: "www-data",
    worker_processes: 4,
    sites: [{
      server_name: "itamae.kitchen",
      root: "/var/www/itamae",
      allowed_ips: ["127.0.0.1/32"],
    }],
  },
}
```

If validation error occurs, provisioning won't be executed.
