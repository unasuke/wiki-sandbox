---
title: "execute resource - Itamae wiki (WIP)"
---

## Actions

- run
- nothing

## Attributes

<table>
  <tr>
    <th>Name</th>
    <th>Value</th>
    <th>Default</th>
    <th>Required</th>
  </tr>
    <tr>
      <td><code>action</code></td>
      <td>one of Symbol, Array</td>
      <td><code>:run</code></td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><code>user</code></td>
      <td>String</td>
      <td>(no default)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>cwd</code></td>
      <td>String</td>
      <td>(no default)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>command</code></td>
      <td>String</td>
      <td>(name of resource)</td>
      <td>No</td>
    </tr>
</table>

## Example

```ruby
execute "create an empty file" do
  command "touch /path/to/file"
  not_if "test -e /path/to/file"
end
```


***

_Do not edit this page because this is generated automatically with Itamae v1.12.3_
