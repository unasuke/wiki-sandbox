---
title: "package resource - Itamae wiki (WIP)"
---

## Actions

- install
- remove
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
      <td><code>:install</code></td>
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
      <td><code>name</code></td>
      <td>String</td>
      <td>(name of resource)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>version</code></td>
      <td>String</td>
      <td>(no default)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>options</code></td>
      <td>String</td>
      <td>(no default)</td>
      <td>No</td>
    </tr>
</table>

## Example

```ruby
package 'sl' do
  version '3.03-17'
end
```


***

_Do not edit this page because this is generated automatically with Itamae v1.12.3_
