---
title: "Getting Started - Itamae wiki (WIP)"
---

## Installation

Add this line to your Gemfile:

```ruby
gem 'itamae'
```

And then execute:

```shell
$ bundle
```

Or install it yourself as:

```shell
$ gem install itamae
```

## Getting Started

Create a recipe file as `recipe.rb`:

```ruby
package 'nginx' do
  action :install
end

service 'nginx' do
  action [:enable, :start]
end
```

And then excute `itamae` command to apply a recipe to a local machine.

```shell
$ itamae local recipe.rb
 INFO : Starting Itamae...
 INFO : Recipe: /home/user/recipe.rb
 INFO :    package[nginx]
 INFO :       action: install
 INFO :          installed will change from 'false' to 'true'
 INFO :    service[nginx]
 INFO :       action: enable
 INFO :       action: start
```

Or you can apply a recipe to a remote machine by `itamae ssh`.


```shell
$ itamae ssh --host host001.example.jp recipe.rb
```

You can also apply a recipe to Vagrant VM by `itamae ssh --vagrant`.

```shell
$ itamae ssh --vagrant --host vm_name recipe.rb
```

### Built-in Help

You can see the help by executing `itamae help`.

```shell
$ itamae help
Commands:
  itamae help [COMMAND]            # Describe available commands or one specific command
  itamae local RECIPE [RECIPE...]  # Run Itamae locally
  itamae ssh RECIPE [RECIPE...]    # Run Itamae via ssh
  itamae version                   # Print version

Options:
  -l, [--log-level=LOG_LEVEL]
                               # Default: info
      [--color], [--no-color]
                               # Default: true
```

You can get available options of `itamae local` by executing `itamae help local`.

```shell
$ itamae help local
Usage:
  itamae local RECIPE [RECIPE...]

Options:
      [--dot=PATH]                 # Only write dependency graph in DOT
  -j, [--node-json=NODE_JSON]
  -y, [--node-yaml=NODE_YAML]
  -n, [--dry-run], [--no-dry-run]
      [--ohai], [--no-ohai]
  -l, [--log-level=LOG_LEVEL]
                                   # Default: info
      [--color], [--no-color]
                                   # Default: true

Run Itamae locally
```

You can get available options of `itamae ssh`  by executing `itamae help ssh`.


```shell
$ itamae help ssh
Usage:
  itamae ssh RECIPE [RECIPE...]

Options:
      [--dot=PATH]                           # Only write dependency graph in DOT
  -j, [--node-json=NODE_JSON]
  -y, [--node-yaml=NODE_YAML]
  -n, [--dry-run], [--no-dry-run]
  -h, [--host=HOST]
  -u, [--user=USER]
  -i, [--key=KEY]
  -p, [--port=N]
      [--ohai], [--no-ohai]
      [--vagrant], [--no-vagrant]
      [--ask-password], [--no-ask-password]
      [--sudo], [--no-sudo]
                                             # Default: true
  -l, [--log-level=LOG_LEVEL]
                                             # Default: info
      [--color], [--no-color]
                                             # Default: true

Run Itamae via ssh
```


## Further Information

You can find further information to use Itamae on [Itamae Wiki](https://github.com/itamae-kitchen/itamae/wiki).

Enjoy!
