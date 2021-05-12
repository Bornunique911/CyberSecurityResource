---
author: Nickapic
title: "Cross Side Scripting Attacks"
date: 2021-04-24
description: This is a article to teach people on a very basic level about how to use Nessus and list some resources to learn and practice with this tool.
series: ["Cross Side Scripting"]
tags: ["XSS","Web",Hacking", "Web Security"]
categories: ["Offensive Hacking", "Begginers"]
ShowBreadCrumbs: true
--- 

3 types of XSS →

Reflected XSS→ iNJECT SOMETHING MALICIOUS AND we get a pop up and its reflected to us its never stored on the server and will be reflected on the page so its on the client side

Stored XSS→This is the opposite of Reflected this will inject malicious payload in the server and even if we leave and come back the payload will still be there.

Dom XSS→ Client Side it basically effects the DOM of the website .

Example of Reflected. 

index.php 

```
<?php

$username = $_GET['username']

echo "Hi $username!";

?>
```
So in case we run index.php?username=aniket 

We get Hi Aniket!

and if we do `index.php?username=<script>alert(1)</script>`

If we manage to do Stored Xss this will execute everytime someone opens the website like in this case it will make a popup saying 1 to everyone who visits the site.

Reflected and DOM XXS attacks require socila enginerring to work we will need them to click on a link or so and we can get a cookie or something from them we can also do key logging, stealing cookie, ddos attacks etc.

Good Resource on DOM Based XSS → [https://www.scip.ch/en/?labs.20171214](https://www.scip.ch/en/?labs.20171214)

### Reflected XSS Attacks→

We inspect anything and everything that we can type into and use that to do cross side scripting there and see if something works out .And we can try stuff like `<iframe src="javascript:alert(`xss`)">` . Maybe try it in the Registration or feedback or review or anything that you can just try everywhere.A thing we can use to improve our xss game is a game called [http://xss-game.appspot.com/level1](http://xss-game.appspot.com/level1)

### Stored XSS Attacks →

This is the most dangerous version of XSS attacks maybe thing of stuff like gettting the admins cookie by just doing stuff like that now to do this in our Juice Shop website we can basically do this . We gotta think on how we can bypass stuff for example in the example we can do stuff to bypass it like sif we know it removes the first script tag try adding two of them or soemthing like thatand you can try doing it through Intruder in Burp Suite maybe and you can get payloads from github like this one below→[https://github.com/pgaijin66/XSS-Payloads/blob/master/payload.txt](https://github.com/pgaijin66/XSS-Payloads/blob/master/payload.txt)

### Preventinf XSS →

Encoding the text might help us so < becomes &lt filtering it so `<script>` will become script and we can also implement validating so we compare the iput against white list.Sanitization so we try combination of escaping,filtering and validation.We can also use http only cookies so we cant extract the cookies from the website.

Resources : 
