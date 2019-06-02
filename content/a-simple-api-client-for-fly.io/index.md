---
title: "A simple API client for Fly.io"
description: "We use Fly.io internally for providing custom domain support to our customers. As we built our product, I put together a Node.js API client for Fly. I realized that it could be easily modified and…"
date: "2018-07-25T20:13:19.174Z"
categories: 
  - JavaScript
  - Nodejs
  - Custom Domain
  - Https
  - Security

published: true
canonicalLink: https://medium.com/filiosoft/a-simple-api-client-for-fly-io-c061c9ab0e03
---

![“Three people in the basket of a colorful hot air balloon floating against a blue sky” by [Aaron Burden](https://unsplash.com/@aaronburden?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)](./asset-1)

We use Fly.io internally for providing custom domain support to our customers. As we built our product, I put together a Node.js API client for Fly. I realized that it could be easily modified and then published publicly for others to use. And that’s what I just did!

The API client is pretty simple and allows you to do some basic things such as creating, deleting, or getting app hostnames.

```
const Fly = require("@filiosoft/fly");

const fly = new Fly("your-access-token");

const hostnames = await fly.getHostnames('example-app')
// responds with an array of the hostnames

const response = await fly.postHostname('example-app', 'example.com')
// responds with a preview_hostname
```

We have released this simple library under the MIT license so that you can use it in your project! You can find the full documentation for the library [here](https://oss.eventone.page/fly-api/), Fly’s API docs [here](https://fly.io/docs/api/), and the source code on [GitHub](https://github.com/eventOneHQ/fly-api).