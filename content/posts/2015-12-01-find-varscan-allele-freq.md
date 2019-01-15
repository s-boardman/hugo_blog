---
categories:
- bioinformatics
date: 2015-12-01T00:00:00Z
published: true
tags:
- awk
- vcf
- shell
title: Finding Allele Frequency from Varscan VCFs
url: varscan-frequency
---

To pull the allele frequency for a given position use the following command:

```bash
awk '{if($1=="chr3" && $2=="178922324" && $5=="A") print $10}' /path/to/varscan/vcf | awk '{FS=":"}{print $7}'
```

The first awk command pulls all variants from position chr3:178922324 where the alternate allele is an A. This outputs the INFO field from the vcfs which match the conditions.

The INFO field looks like this:

```bash
$ awk '{if($1=="chr3" && $2=="178922324" && $5=="A") print $10}' /path/to/varscan/vcf
0/1:20:5652:5652:5611:17:0.3%:8.3982E-3:35:16:2569:3042:7:10
```

The second awk command takes the information field we just passed and splits it using a colon as a delimiter then prints the seventh field which is the allele frequency.

From our above example the output we expect to see is:

```bash
$ awk '{FS=":"}{print $7}
0.3%
```
