---
categories:
- bioinformatics
date: 2016-01-05T00:00:00Z
published: true
tags:
- shell
title: Useful Shell Commands
url: /bioinformatics/shell-utilities
---

## Using Secure Copy to transfer files between networks

Copy local files to remote destination:

```bash
scp file_to_copy user@destination.ip:/destination/path
```

## Search bash history and repeat command

Sometimes I want to repeat a command that I used a while ago. Often I have to Google it which is lazy. Now using this trick I can find it in my history without having to scroll through lots of entries.

```bash
#ctrl-R
(reverse-i-search)`': search_term
#enter to bring to current line
```
