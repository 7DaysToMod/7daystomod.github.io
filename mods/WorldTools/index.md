---
layout: default
title: 7DaysToMod - Dedicated Server Mods - WorldTools
---
<ul style="list-style: none;">
	<li class="link-toolbar-right">
		<a href="https://github.com/7DaysToMod/worldtools" class="social-icon" target="_blank" title="View on Github">
			<img src="/images/Octocat.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://trello.com/b/ubhbKNfD/worldtools" class="social-icon" target="_blank" title="TODO List on Trello">
			<img src="/images/trello.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="http://7daystodie.com/forums/" class="social-icon" target="_blank" title="7DaysToDie.com Forum Post">
			<img src="/images/placeholder_small.png" height="30">
		</a>
	</li>
	<li class="link-toolbar-right">
		<a href="https://github.com/7DaysToMod/worldtools/releases" class="social-icon" target="_blank" title="Downloads">
			<img src="/images/download.png" height="30">
		</a>
	</li>
</ul>

# WorldTools

World Editing commands for Dedicated Servers.

## Dependencies

This mod requires the following mods to already be installed on the server.

[7dtmlib](http://7daystomod.com/mods/7dtmlib)

## Console Commands

__wtselect__ - Sets the start or end point for a selection to the current player position

__wtselect &lt;StartX&gt; &lt;StartY&gt; &lt;StartZ&gt; \[&lt;EndX&gt; &lt;EndY&gt; &lt;EndZ&gt;\]__ - Sets the start and end position of the current selection to coordinates provided

__wtselect clear__ - clears the current selection

__wtclosest &lt;PrefabName&gt;__ - Finds the closest instance of &lt;PrefabName&gt; to the player position

__despawn &lt;EntityID&gt;__ - Completely Despawns the entity with an id of &lt;EntityID&gt;

__wtrotateent &lt;EntityID&gt; &lt;DegreesToRotate&gt;__ - Rotate the way the entity with &lt;EntityID&gt; by the number ofdegrees supplied in &lt;DegreesToRotate&gt;

__wtcopy__ - Copies the content of the current selection

__wtexport &lt;PrefabName&gt; [&lt;yOffset&gt;]__ - Creates a new prefab called &lt;PrefabName&gt; with the content of the current selection, with the optional yOffset of &lt;yOffset&gt;

__wtfill &lt;BlockName&gt;__ - Fills the current selection with the block &lt;BlockName&gt;

__wtimport &lt;PrefabName&gt;__ - Import the Prefab &lt;PrefabName&gt; into the current player selection

__wtpaste [&lt;Rotations&gt; &lt;yOffset&gt;]__ - Paste the current selection at the players current position with optional rotation and yOffset

__wtpasteprefab &lt;PrefabName&gt; [&lt;Rotations&gt;]__ - Paste the Prefab called &lt;PrefabName&gt; at the current player position with optional number of rotations

__wtrotate &lt;Rotations&gt;__ - Rotate the current player selection.  This will modify your world directly.

__wtundo__ - Undo the last WorldTools Command.

{% include serverinstall.md %}