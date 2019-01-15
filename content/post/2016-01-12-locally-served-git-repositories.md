---
categories:
- bioinformatics
date: 2016-01-12T00:00:00Z
published: true
tags:
- git
- shell
title: Setting up a Git Repository Across a Local Network
url: /bioinformatics/local-git
---

I mostly use [GitHub](https://github.com) for distributing code I'm working on. For the odd occasion I want to distribute across a local network without using a private repository these are the steps I'll need to use for setting up a repository.

## Overall Structure

The structure I'm aiming for is as follows:

<pre>
 /local_server/repository
|
|--/local_desktop/repository
|
|--/local_laptop/repository
</pre>

Where the work is done on local machines (laptop/desktop) and pushed to the local server for distribution ensuring that both local machines can access the repository easily.

## Setting Up the Remote

On the local server navigate to where the repository is to be hosted:

```bash
cd /path/to/remote/host
```

Make a directory for storing all the clever code Git runs. Then initialise a bare repository which has no working tree. This is important for making sure our initial push and pull between remotes works as intended[^1].

```bash
mkdir repository_name
cd repository_name
git init --bare
```

## Setting Up a Repository on the Local Machines

On each local machine we can now clone the bare remote repository and have them all link together nicely.

To set up the local repository using an existing folder containing files you want to include:

```bash
cd /local_machine/path/to/desired/folder
ls
file1	file2
git clone /path/to/remote/host/repository_name
cd repository_name
git add file1 file2
git commit -m 'first commit'
git push origin master
```

Make sure you include `origin master` for the first push otherwise you'll get the following errors:

```bash
 No refs in common and none specified; doing nothing.
Perhaps you should specify a branch such as 'master'.
fatal: The remote end hung up unexpectedly
error: failed to push some refs to '/path/to/remote/host/repository_name'
```

## Cloning the Remote Repository into a new Local Location

To add the repository onto a new local machine you can clone from the remote (server) and have everything automatically imported and linked up.

```bash
cd /local_machine/path/to/desired/folder
git clone /path/to/remote/host/repository_name
cd repository_name
ls
file1	file2
```

You can then do the normal git things like adding, commiting, making branches, and have all your code and commit history nicely synced up.


## Troubleshooting

If Git isn't installed the following commands should work on most Unix systems:

```bash
# Fedora distributions
sudo yum install git-all

# Debian distributions
sudo apt-get install git-all
```

Further details on installation are located on the [Git documentation pages](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git/).

[^1]: This [StackOverflow post](http://stackoverflow.com/questions/7632454/how-do-you-use-git-bare-init-repository) gives a few more details.
