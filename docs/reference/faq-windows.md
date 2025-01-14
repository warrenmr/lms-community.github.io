---
layout: default
title: Lyrion Music Server on Windows - Frequently Asked Question
---


# FAQ: Lyrion Music Server on Windows

## After installation I'm told Lyrion Music Server wasn't started. What can I do?


## Can I have more than one music folder?

## How can I connect to my music on a NAS?


## I can't connect to my NAS using my Microsoft Account. What's wrong with it?

## Where's the tray icon to start/stop Lyrion Music Server?

The tool to build the old tray icon is no longer available. Starting with Logitech Music Server 9.0 we can no longer provide that tool.

But you might be interested in this [Service Tray](https://www.coretechnologies.com/products/ServiceTray/) utility. It can be configured to start/stop the LMS service and the icon in the system tray has colors so you can see the status of your service that you configured it for. And it's free to use.

[Control any Windows Service with a Taskbar Tray Icon](https://www.coretechnologies.com/products/ServiceTray/).\

## Lyrion Music Server does not always restart properly.  How can I fix this?

If you are experiencing odd restart problems, for example after a plugin installation or perhaps just after a restart, it may be due to the LMS service taking too long to start.  Windows has a 30 second limitation for thread starting by default, and if LMS takes longer than that, Windows will simply shut it down before startup completes.  The fix for this requires a Windows registry edit which can be a bit daunting if you haven't done it before.  However, it needs to be only done once and there is a Microsoft thread that explains how it is done here:  https://learn.microsoft.com/en-us/troubleshoot/windows-server/system-management-components/service-not-start-events-7000-7011-time-out-error

Start with increasing the timeout length to 60 seconds, as the article suggests.
