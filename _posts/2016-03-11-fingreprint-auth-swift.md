---
layout: post
section-type: post
title: Fingerprint authentication in Swift 2
category: tech
tags: [ 'ios', 'security' ]
---

It's a nice way to protect your app from being accessed by someone that is not the device owner.

The code is simple, but don't forget to fallback to a pin prompt in case the
fingerprint sensor is not present on the device.

In my opinion the best place this method should be called from, is the AppDelegate.
That way you will be able to spawn the authentication when the devices is starting,
or while entering the foreground (from the background).

<script src="https://gist.github.com/PanosSakkos/570c9afe0748176a952a.js"></script>

And will look like this

![misc](/img/posts/touch-id/touch-id.jpg)
