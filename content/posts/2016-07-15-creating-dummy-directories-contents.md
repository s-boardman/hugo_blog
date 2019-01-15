---
categories:
- bioinformatics
date: 2016-07-15T00:00:00Z
tags:
- shell
title: Creating Dummy Directories and Contents
url: dummy-directories-contents
---

Take a source directory and make a copy of its subdirectories and contents.

```bash
find src/ -type d -exec mkdir -p dest/{} \; \
       -o -type f -exec touch dest/{} \;
```

Use `find` to identify a directory (`-d`) under (`src/`) and create (`mkdir -p`) the contents under `dest/` then (`-o`) find files (`-f`) and touch them under `dest/` to make empty copies with the same name.

Best done in the source directory, if in the destination directory you get the full file path at the start which requires a move to bring it to the right level and deletion of empty directory structure.

Source: [StackOverflow](http://stackoverflow.com/a/11952522)
