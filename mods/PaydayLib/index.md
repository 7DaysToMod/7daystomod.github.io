---
layout: default
title: 7DaysToMod - Dedicated Server Mods - PaydayLib
---
<ul style="list-style: none;">
	<li class="link-toolbar-right">
		<a href="https://github.com/7DaysToMod/PaydayLib" class="social-icon" target="_blank" title="View on Github">
			<img src="/images/Octocat.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://trello.com/b/7mB92CKm/paydaylib" class="social-icon" target="_blank" title="TODO List on Trello">
			<img src="/images/trello.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="http://7daystodie.com/forums/" class="social-icon" target="_blank" title="7DaysToDie.com Forum Post">
			<img src="/images/placeholder_small.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://github.com/7DaysToMod/PaydayLib/releases" class="social-icon" target="_blank" title="Downloads">
			<img src="/images/download.png" height="30">
		</a>
	</li>
</ul>

# PaydayLib

Server Economy mod for 7 days to die dedicated servers.

{% include serverinstall.md %}

## Console Commands

__paydaylib info__ - Displays the current configuration settings for PaydayLib

__paydaylib reload__ - Reloads the PaydayLib Config and Player Data

__paydaylib enabletimer__ - Enables the PaydayLib User Pay Timer

__paydaylib disabletimer__ - Disables the PaydayLib User Pay Timer

__paydaylib currency &lt;currency_name&gt;__ - Changes the name of the in game Currency (The Currency name defaults to "Coins")

__paydaylib rate &lt;amount&gt;__ - Sets the amount of points a player receives each real-world Minute.

__paydaylib startrate &lt;starting_balance&gt;__ - Sets the amount of points a player recieves the first time they join the server.


## Chat Commands

__!balance__ - Show your current balance

__!listproducts__ - Shows you a list of purchasble products

__!buy &lt;ProductMame&gt;__ - Buy the product &lt;ProductName&gt;

__!pay &lt;PlayerName&gt; &lt;amount&gt;__ - Transfer &lt;amount&gt; coins from your balance to &lt;PlayerName&gt;

## Quick Setup Guide

Ensure you have admin rights and run the following commands

This will set up Paydaylib with a currency called "MyCoolNameForCoins".  Each player will recieve 50 MyCoolNameForCoins when they first join, and an additional 1 MyCoolNameForCoins per minute they are on the server.

```

paydaylib currency MyCoolNameForCoins

paydaylib rate 1

paydaylib startrate 50

paydaylib enabletimer

```

## Addons

[PaydayBounties](http://7daystmod.com/mods/paydaybounties) - Player Bounty chat commands for PvP enabled servers.

[7dtmWarpLib](http://7daystomod.com/mods/warplib) - Adds purchasable chat commands for player home warps.