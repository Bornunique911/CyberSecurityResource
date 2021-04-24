---
author: Nickapic
title: "Nessus"
date: 2021-04-24
description: This is a article to teach people on a very basic level about how to use Nessus and list some resources to learn and practice with this tool.
series: ["Formal Documentation"]
tags: ["Nessus","Vulnerbaility Scanner","Web Apps", "Network Security"]
categories: ["Offensive Hacking"]
ShowBreadCrumbs: true
--- 

## Introduction and Installations

Nessus is a scanning tool that we can utilize for external and internal assesments.

To download and install it we go to google type nessus download and t hen we find this site called Tenable we find the image which is compatible with our debian system and download that then go to the terminal traverse to the download directory and then do

```bash
dpkg -i Nessusfilename
```

and then we type in the path it gives us in the terminal again like shown below 

![Image](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d5c3e114-3a9b-470f-b045-e0756a30ab75/Untitled.png)

So we start nessus by doing /etc/init.d/nessusd start 

and then we go to our browser and go to the the page kali:8834 

and then we can install tool by signing up and stuff like that and it should like like something like this after its done installing and everything.

![Image](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e1cb56c7-0c5d-486a-aee1-c37f7d844706/Untitled.png)

This is the free dition which allows us to scan any private IP address and we can scan 15 of these so class A to class C cant scan an external ip tho.

You can schedule Scans here and every thing 

We can then go to the discovery tab and select what ports we wanna scan so like all of them or some of them that are defined in the program and then also in the assesment tab we can scan for diffrent types like Scan for all known web Vulnerablities,Scan for all web vulnerabilites and stuff like that .

![Image](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ee986477-4e95-4a6a-ae3c-e2d6d130863d/Untitled.png)

Its kind of a slow scan btw it takes a while to do and its preety through.

In the new scan tab we have a lot of types of scans like 

Malware Scans,Ransomware Scans ,Mobile Device Scan,Advanced Scan 

The most common ones though would be basic and advanced scan

![Image](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/48190871-e658-463f-8091-ac363a79a8a1/Untitled.png)

So after our scan is complete we can go to it and check all the vulnerabilites listed in their like below- 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6c639289-265f-4f29-a3af-7d15ec20de92/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6c639289-265f-4f29-a3af-7d15ec20de92/Untitled.png)

We can export these list of Vulnerablities by clicking the export button and we can get nessus document which we can then convert to excel and put in our report .

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/497a522c-dff1-4de3-b057-57129d1481bf/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/497a522c-dff1-4de3-b057-57129d1481bf/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/29a78e73-7c73-4916-b420-090e54edb392/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/29a78e73-7c73-4916-b420-090e54edb392/Untitled.png)


## Resource and places to learn more :
1. Nessus : https://tryhackme.com/room/rpnessusredux
2. The Cyber Mentor : https://academy.tcm-sec.com/p/practical-ethical-hacking-the-complete-course