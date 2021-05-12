---
author: Nickapic
title: "Git Hacking"
date: 2021-04-24
description: This is a article to help people with how to ennumerate and exploit when you find public repostries.
series: ["Formal Documentation"]
tags: ["Git","Github","Tryhackme"]
categories: ["Offensive Hacking"]
ShowBreadCrumbs: true
---

So to enumerate over .git folder and also to dump them to your desktop and stuff we use tools from this repository [GitTools](https://github.com/internetwache/GitTools)  and we can just git clone this repositry and use all the tool and the guides for them are given in the repo.

But in general we can use gitfinder tool to find websites with their .git repository available to the public. It identifies websites with publicly accessible .git repositories. It checks if the .git/HEAD file contains refs/heads

The gitdumper tool can be used to download as much as possible from the found .git repository from webservers which do not have directory listing enabled. This is what we will use in our case to solve this box.

The extractor is script to extract commits and their content from a broken repository.

This script tries to recover incomplete git repositories:

- Iterate through all commit-objects of a repository
- Try to restore the contents of the commit
- Commits are not sorted by date

Soo lets start using our gitdumper tool to dump the publicly accessible .git directory and to use this command here we can use :

```bash
./gitdumper.sh <ip>/.git .
```

and this will dump the private git directory for us in the current directory and also this is gonna be hidden as its the git directory so we can use all the git commands on it and we can traverse into the directory and use commands like git log and see all the commits done and lets scroll down to the bottom and we find the Initial Commit and use its SHA1 hash

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/192693b9-4f79-4b3f-9ef4-4f4325732932/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/192693b9-4f79-4b3f-9ef4-4f4325732932/Untitled.png)

and now we can use this SHA1 hashes next to commit we wanna see and we can use the command

```bash
git show 2f423697bf81fe5956684f66fb6fc6596a1903cc
```

and we can show the whole commit and all the files in that commit there 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dd2df77c-6d76-42ad-80cc-8b5d63977b27/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dd2df77c-6d76-42ad-80cc-8b5d63977b27/Untitled.png)

and there you go we can see the password which is the flag here and again if you find this as a bug bounty you can report and its gonna be a pretty good payout for that because this will let us track all the code and all sensitive information in the commits if there ever was something.

## Resources :
