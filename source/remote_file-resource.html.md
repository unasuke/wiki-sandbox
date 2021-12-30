---
title: "remote_file resource - Itamae wiki (WIP)"
---

## Actions

- delete
- edit
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
      <td><code>path</code></td>
      <td>String</td>
      <td>(name of resource)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>content</code></td>
      <td>String</td>
      <td>(no default)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>sensitive</code></td>
      <td></td>
      <td>(no default)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>mode</code></td>
      <td>String</td>
      <td>(no default)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>owner</code></td>
      <td>String</td>
      <td>(no default)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>group</code></td>
      <td>String</td>
      <td>(no default)</td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>block</code></td>
      <td>Proc</td>
      <td><code>Proc</code></td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>source</code></td>
      <td>one of String, Symbol</td>
      <td><code>:auto</code></td>
      <td>No</td>
    </tr>
</table>


***

_Do not edit this page because this is generated automatically with Itamae v1.12.3_
