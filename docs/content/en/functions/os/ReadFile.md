---
title: os.ReadFile
description: Returns the contents of a file.
categories: []
keywords: []
params:
  functions_and_methods:
    aliases: [readFile]
    returnType: string
    signatures: [os.ReadFile PATH]
aliases: [/functions/readfile]
---

The `os.ReadFile` function attempts to resolve the path relative to the root of your project directory. If a matching file is not found, it will attempt to resolve the path relative to the [`contentDir`](/configuration/all/#contentdir). A leading path separator (`/`) is optional.

With a file named README.md in the root of your project directory:

```text
This is **bold** text.
```

This template code:

```go-html-template
{{ readFile "README.md" }}
```

Produces:

```html
This is **bold** text.
```

Note that `os.ReadFile` returns raw (uninterpreted) content.
