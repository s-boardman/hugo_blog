---
categories:
- bioinformatics
date: 2015-11-13T00:00:00Z
tags:
- shell
- rsync
title: rsync tricks
url: /bioinformatics/rsync-tricks
---

## Copy Directory Structure and Specific File Types

I wanted to copy over some bams and maintain the directory structure (`Sample/bam/Sample.bam`) using `rsync` to preserve timestamps and ownership.

The command I used:

``` bash
rsync -av  --include='*.bam*' --include='*/'--exclude='*' /path/to/Samples* ./Destination/
```

This copied the entire directory structure for each sample and the required bam files. I could have excluded the empty directories using `--prune-empty-dirs` but like to have it just in case.

This [stackexchange question](http://unix.stackexchange.com/questions/2161/rsync-filter-copying-one-pattern-only) was very useful.
