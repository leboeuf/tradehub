---
layout: home
---

## Discovery

The only dependency common to all components. Lists IP or URLs of every components so that they can communicate with each other without having to change a config file every time an IP changes.

Registers the IP address of the querying host and logs to TradeHub.Monitor (unless the dev parameter is present in the URL, which is used when developing a component) the component queries Discovery upon every launch and when links are broken.
