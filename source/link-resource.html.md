---
title: "link resource - Itamae wiki (WIP)"
---

## Actions

- create
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
      <td><code>:create</code></td>
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
      <td><code>link</code></td>
      <td>String</td>
      <td>(name of resource)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>to</code></td>
      <td>String</td>
      <td>(no default)</td>
      <td>Yes</td>
    </tr>
    <tr>
      <td><code>force</code></td>
      <td>one of TrueClass, FalseClass</td>
      <td>(no default)</td>
      <td>No</td>
    </tr>
</table>

## Example

```ruby
link "/path/of/destination"  do
  to "/path/of/source"
end
```


***

_Do not edit this page because this is generated automatically with Itamae v1.12.3_
