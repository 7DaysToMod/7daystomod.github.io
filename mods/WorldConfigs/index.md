---
layout: default
title: 7DaysToMod - Dedicated Server Mods - 7dtmlib
---
<ul style="list-style: none;">
	<li class="link-toolbar-right">
		<a href="https://github.com/7DaysToMod/worldconfigs" class="social-icon" target="_blank" title="View on Github">
			<img src="/images/Octocat.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://trello.com/b/56hyB7rT/worldconfigs" class="social-icon" target="_blank" title="TODO List on Trello">
			<img src="/images/trello.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://7daystodie.com/forums/showthread.php?65053-DEDI-WorldConfigs-Automated-XML-Config-Switching-for-Servers" class="social-icon" target="_blank" title="7DaysToDie.com Forum Post">
			<img src="/images/placeholder_small.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://github.com/7DaysToMod/worldconfigs/releases" class="social-icon" target="_blank" title="Downloads">
			<img src="/images/download.png" height="30">
		</a>
	</li>
</ul>

# WorldConfigs

Switch XML Configs on your server by changing the world name.


On server startup, World Configs will check to see if a backup of the XML Configs for the server exists in the current World Save Directory.  If it does not exist, WorldConfigs will backup the default Config directory into the world save folder.  If it does exist, WorldConfigs will copy the backup into the default config directory.

This allows you to switch between custom xml configs without the hassle of manually backing up and restoring the XML Configs.

__Be aware!__  Once enabled, and run for the first time, any changes to the XML Configs in the default Config directory will be overwritten by the backup in the world save folder.  You must remember to change the configs in the world save folder. 

For example 7daystodie_folder/saves/&lt;world_type&gt;/&lt;WorldSaveName&gt;/WorldConfigs/Data/Config

## Using World Configs

Once installed, there is nothing you have to do to utilise the WorldConfigs mod.  Simply change your world type or world name via your normal method, and WorldConfigs will take care of the rest.

__Be aware!__  Once enabled, and run for the first time, any changes to the XML Configs in the default Config directory will be overwritten by the backup in the world save folder.  You must remember to change the configs in the world save folder. 

For example 7daystodie_folder/saves/&lt;world_type&gt;/&lt;WorldSaveName&gt;/WorldConfigs/Data/Config


## Chat Commands

__Coming soon wcset worldtype worldname__ - Set the world type and name

{% include serverinstall.md %}
