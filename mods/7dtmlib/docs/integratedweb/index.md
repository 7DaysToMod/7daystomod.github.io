---
layout: default
title: 7DaysToMod - Dedicated Server Mods - 7dtmlib - Integrated Web Server
---
# Integrated Web Server

7dtmlib adds an optional Integrated web server, providing a central point of management for common server tasks.  An API is also provided to allow other mods to add their own settings and pages.

## Activating the Integrated Web Server

Once installed, you will need to configure the port number for the server to an available port and turning the web server on:

```
integratedweb true port_number

```

after running this command, restart your server and then navigate your brower to the ip address of your server followed by the port number
http://<ip_address>:<port_number>