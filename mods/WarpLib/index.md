---
layout: default
title: 7DaysToMod - Dedicated Server Mods - WarpLib
---
<ul style="list-style: none;">
	<li class="link-toolbar-right">
		<a href="https://github.com/7DaysToMod/warplib" class="social-icon" target="_blank" title="View on Github">
			<img src="/images/Octocat.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://trello.com/b/yEuvu0cS/warplib" class="social-icon" target="_blank" title="TODO List on Trello">
			<img src="/images/trello.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="http://7daystodie.com/forums/" class="social-icon" target="_blank" title="7DaysToDie.com Forum Post">
			<img src="/images/placeholder_small.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://github.com/7DaysToMod/warplib/releases" class="social-icon" target="_blank" title="Downloads">
			<img src="/images/download.png" height="30">
		</a>
	</li>
</ul>

# WarpLib

Server Warps.

## Dependencies

This mod requires the following mods to already be installed on the server.

[7dtmlib](http://7daystomod.com/mods/7dtmlib)

## Optional dependencies

This mod also contains support for the following mods, if they are already installed on the server.

[PaydayLib](http://7daystomod.com/mods/PaydayLib)

## Console Commands

__warps list__ - Lists all available server warps

__warps add &lt;WarpName&gt; &lt;WarpCost&gt;__ - Creates a new warp at the player location called &lt;WarpName&gt;, with and optional PaydayLib cost of &lt;WarpCost&gt;.

__warps remove &lt;WarpName&gt;__ - Removes the server warp called &lt;WarpName&gt;

__warp &lt;WarpName&gt;__ Warps the player to the location of the server warp &lt;WarpName&gt;

__sethome__ - Sets the player home warp Location to their current position

__clearhome__ - Clears the player home warp location.

__gohome__ - Warp the player to their current home warp location.

## Chat Commands

__!warps__ - Lists all available server warps

__!warp &lt;WarpName&gt;__ Warps the player to the location of the server warp &lt;WarpName&gt;

__!sethome__ - Sets the player home warp Location to their current position

__!clearhome__ - Clears the player home warp location.

__!gohome__ - Warp the player to their current home warp location.

## PaydayLib Integration

WarpLib adds a product to the PaydayLib product list, allowing players to purchase permission to use the sethome, clearhome and gohome commands.

The cost for use of the sethome, clearhome and gohome commands can also be set using the pdlsetprice command.

{% include serverinstall.md %}
