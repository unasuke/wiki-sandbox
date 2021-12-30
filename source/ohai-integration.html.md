---
title: "Ohai integration - Itamae wiki (WIP)"
---

You can load node attributes from Ohai.
To load attributes from Ohai, pass `--ohai` to command.

```
$ itamae local --ohai recipe.rb
```

Note that if ohai is not found on the target host, Itamae will install it to the host.
