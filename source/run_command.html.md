---
title: "run_command - Itamae wiki (WIP)"
---

# `run_command`

You can run commands on the server you are provisioning, in a recipe by `run_command`. This method returns an instance of [Specinfra::CommandResult](https://github.com/serverspec/specinfra/blob/master/lib/specinfra/command_result.rb).

## Example

```ruby
# recipe.rb

# You can use run_command in a recipe
result = run_command("echo -n Hello")
result.stdout == "Hello"
result.exit_status == 0

define :run_command_in_definition do
  # You can use run_command in definition block
  run_command("echo -n Hello")
end

execute "echo Hello" do
  # You can use run_command in resource block
  run_command("echo -n Hello")
end

local_ruby_block 'execute run_command' do
  # You can use run_command with local_ruby_block
  block do
    run_command("echo -n Hello")
  end
end
```
