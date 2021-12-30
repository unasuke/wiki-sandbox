---
title: "http_request resource - Itamae wiki (WIP)"
---

## Actions

- delete
- post
- options
- get
- put
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
      <td><code>:get</code></td>
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
      <td><code>headers</code></td>
      <td>Hash</td>
      <td><code>{}</code></td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>message</code></td>
      <td>String</td>
      <td><code>""</code></td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>redirect_limit</code></td>
      <td>Integer</td>
      <td><code>10</code></td>
      <td>No</td>
    </tr>
    <tr>
      <td><code>url</code></td>
      <td>String</td>
      <td>(no default)</td>
      <td>Yes</td>
    </tr>
</table>


***

_Do not edit this page because this is generated automatically with Itamae v1.12.3_
