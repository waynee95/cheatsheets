# Pandoc

## Including packages

```yaml
---
title: "Hello World"
header-includes:
  - \usepackage{...}
---

```

## Documentclass options

```yaml
---
documentclass: scrartcl
lang: de
title: "Hello World"
classoption:
  - twocolumn
  - landscape
---

```

## Insert comments ([Reference](https://alvinalexander.com/technology/markdown-comments-syntax-not-in-generated-output/))

```
[//]: # (This syntax works like a comment, and won't appear in any output.)
```
