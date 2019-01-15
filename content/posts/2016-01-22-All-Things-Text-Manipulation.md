---
categories:
- bioinformatics
date: 2016-01-22T00:00:00Z
tags:
- shell
- awk
- sed
title: All Things Text Manipulation
url: text-manipulation
---

## sed

### Multiple Find and Replace instances in a Single Command

The `sed` command is one of the most useful to me in day to day work. It makes text manipulation relatively easy and can be great for lossless large scale manpulations by streaming output to a separate file.

I'm working on some copy number data I wanted to strip some leading and trailing arrows from the output of an algorithm I was testing. I used the following `sed` command do it in one fell swoop, rather than having to chain more commands together.

```bash
cat data.txt
1   <DEL>
5   <DUP>
sed 's/<//g; s/>//g' data.txt
1   DEL
5   DUP
```

Simples.

## awk

`awk` isn't really a command, rather it is more properly described as a language. I use even more than `sed` because it plays so nicely with tab delimited data.

In this case I had a file where not every row had a value in every column. I wanted to pull out all the rows with a value in the nth column. Using the following `awk` command was the easiest way to do it:

```bash
cat data2.txt
1   12345	A
2   23456	B
3   34567
4   45678	C

awk '$3' data2.txt
1   12345	A
2   23456	B
4   45678	C
```

This printed every row where the third column was True (i.e. had content).

## sort

`sort` is a very useful unix command. I tend to use it mostly for correcting the order of bed files. This employs the very hand version flag (`sort -V`) which mixes numbers and letters in a logical way.

The below command uses version sort on the first three columns of a file to ensure that regions are in chromosome and coordinate order.

```bash
sort -V -k1,1 -k2,2 -k3,3 input.bed > sorted.input.bed
```
