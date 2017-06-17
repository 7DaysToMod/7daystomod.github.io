---
layout: default
title: 7DaysToMod - Dedicated Server Mods - 7dtmlib
---
<ul style="list-style: none;">
	<li class="link-toolbar-right">
		<a href="https://github.com/7DaysToMod/7DTMLib" class="social-icon" target="_blank" title="View on Github">
			<img src="/images/Octocat.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://trello.com/b/yYcV165k/7dtmlib" class="social-icon" target="_blank" title="TODO List on Trello">
			<img src="/images/trello.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="http://7daystodie.com/forums/" class="social-icon" target="_blank" title="7DaysToDie.com Forum Post">
			<img src="/images/placeholder_small.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://github.com/7DaysToMod/7dtmlib/releases" class="social-icon" target="_blank" title="Downloads">
			<img src="/images/download.png" height="30">
		</a>
	</li>
</ul>

# 7dtmlib - Dedicated Servers Only
Modding Utility Library for 7 Days to Die Dedicated Server Mods

## Features

- Expanded Modding Events
- Extended Group Based Permissions
- Chat Command Handlers
- Modding Utility Classes

## Extended Events
7dtmlib wraps the existing mod functions using c# events and delegates and adds many new events for you to access within your mods including Entity and player Events, Block and Chunk events and Loot Container Events, among others.

See the [Events](./docs/events.md) doc for more information.

## ExPerm - Node Based Permissions Manager
7dtmlib provides a node based Group and user permissions manager, allowing server administrators fine grained control over the features of your mod.

See the [ExPerm](./docs/experm.md) doc for more information.


## Chat Commands

7dtmlib provides a mechanism for easy construction of chat command handlers.

See the [Chat Commands](./docs/chatcommands.md) docs for more infortmation.

## Modding Utility Classes

7dtmlib wraps many common tasks into handy utility classes for faster mod development.

See the [Utility Classes](./docs/utilityclasses.md) docs for more information.

{% include serverinstall.md %}

## Using 7dtmlib in your Server Mods
Simply download the .dll file and add a reference to it in your project.

More information can be found in the [Events](./docs/events.md), [ExPerm](./docs/experm.md), [ChatCommands](./docs/chatcommands.md) and [Utility Classes](./docs/utilityclasses.md) documentation.