---
layout: default
title: 7DaysToMod - Dedicated Server Mods - 7dtmlib - Events
---

# Events

7dtmlib wraps the existing API Methods into an expanded event system.

More detailed information will be available soon

__Example__

```

namespace MyCustomMod
{
	public class MyCustomMod: ModApiAbstract
	{
		SDTM.API.Events.OnGameMinute += MyGameMinuteHandler;
	}
	
	public void MyGameMinuteHandler(int day, int hour, int minute){
		Log.Out(String.Format("Game Time: Day {0}, {1}:{2}", day, hour, minute));
	}
}

```

## Server Events

#### OnGameStarted()

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Event wrapper for the ModApiAbstract.GameAwake method

#### OnGameStopped()

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Event Wrapper for the ModApiAbstract.GameShutdown method

#### OnGameStartDone()

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;EventWrapper for the ModApiAbstract.GameStartDone method

#### OnGameUpdate()

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Event Wrapper for the ModApiAbstract.GameUpdate method

#### OnGameStatsChanged(string StateName, object NewValue)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a value in the GameStat object has changed

#### OnGamePrefsChanged(EnumGamePrefs GamePref)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a value in the GamePrefs object has changed

## Chunk Events

#### OnChunkColorsDone(Chunk chunk)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Event Wrapper for the ModApiAbstract.ChunkColorsDone method

#### OnChunkAdded(Chunk chunk)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a chunk has been loaded on the server

#### OnBeforeChunkRemoved(Chunk chunk)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when before a chunk is unloaded on the server

#### OnBeforeChunkSaved(Chunk chunk)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired before a chunk is saved on the server

## Game Time Events

#### OnLibTick()

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired every 40 game ticks.  This rate can be modified in the 7dtmlib config.

#### OnGameMinute(int day, int hour, int minute)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired on the change of every in game minute

#### OnGameHour(int day, int hour);

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired on the changed of every in game hour

## Player Events

#### OnPlayerLogin(ClientInfo cInfo, string compatibilityVersion)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Event wrapper for the ModApiAbstract.PlayerLogin method

#### OnPlayerSpawning(EntityPlayer player)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Event Wrapper for the ModApiAbstract.PlayerSpawning method

#### OnPlayerSpawned(ClientInfo cInfo, RespawnType respawnReason)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Event Wrapper for the ModApiAbstract.PlayerSpawnedInWorld method

#### OnPlayerDisconnected(EntityPlayer player)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Event Wrapper for ModApiAbstract.PlayerDisconnected method

#### OnPlayerDataSaved(ClientInfo cInfo, PlayerDataFile playerDataFile)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Event Wrapper for the ModApiAbstract.SavePlayerData method

#### OnPlayerDroppedItem(EntityPlayer player, EntityItem item)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a player drops an item.

#### OnPlayerCollectedItem(EntityPlayer player, ItemStack itemStack)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a player picks up an item from the ground.

#### OnPlayerBuffAdded(EntityPlayer player, Buff buff)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a new buff is applied to a player

#### OnPlayerBuffRemoved(EntityPlayer player, Buff buff)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a buff is remobed from a player

#### OnPlayerWellnessChanged(EntityPlayer player, float amount)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when the wellness value of a player changes

#### OnPlayerKilledByPlayer(EntityPlayer player, EntityPlayer killer)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a player kills another player.

#### OnPersistentPlayerDataEvent(PersistentPlayerData player, PersistentPlayerData otherPlayer, EnumPersistentPlayerDataReason reason)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when the persistent player data file is saved for a player

#### OnPlayerACLInviteSent(PersistentPlayerData player, PersistentPlayerData invitedPlayer)

Fired when a player sends a friend request to another player

#### OnPlayerACLInviteAccepted(PersistentPlayerData player, PersistentPlayerData invitedPlayer)

Fired when a player accepts a friend invite from another player

#### OnPlayerACLInviteDeclined(PersistentPlayerData player, PersistentPlayerData invitedPlayer)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a player declines a friend invite from another player

#### OnPlayerACLRemoved(PersistentPlayerData player, PersistentPlayerData invitedPlayer)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a player removes a friend from their friend list.

## Entity Events

#### OnEntityLoaded(Entity entity)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when an entity is loaded into the world.  These include item entities.

#### OnEntityUnloaded(Entity entity, string reason)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when an entity is unloaded from the world.  These include item entities.

#### OnNPCLoaded(EntityNPC entity)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when an NPC is loaded.  This can be triggered by new entities being spawned, or existing entities being loaded within an existing chunk.

#### OnNPCUnloaded(EntityNPC entity, string reason)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when an NPC is unloaded.  This can be triggered by entities being killed, as well as being unloaded with their chunk.

#### OnNPCBanditLoaded(EntityBandit entity)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a Bandit Entity is loaded.

#### OnNPCBanditUnloaded(EntityBandit entity, string reason)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a Bandit Entity is unloaded.

#### OnNPCSurvivorLoaded(EntitySurvivor entity)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a Survivor Entity is loaded.

#### OnNPCSurvivorUnloaded(EntitySurvivor entity, string reason)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a Survivor Entity is unloeded.

#### OnTraderPrimaryInventoryChanged(EntityNPC entity, List&lt;ItemStack&gt; previousInventory)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when the primary inventory of a trader has changed.  This is only fired after the player closes the trader interface.

#### OnTraderSecretStashChanged(EntityNPC entity, List&lt;ItemStack[]&gt; previousStash)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when the secret stash of a trader has changed.  This is only fired after the player closes the trader interface.

## Block Events

#### OnBlockChanged(Vector3i pos, BlockValue oldBlock, BlockValue newBlock)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a block in the world is changed.  There is currenlty no way to determine who changed the block.

#### OnBlockDamaged(Vector3i blockPos, BlockValue blockValue, int damage, int attackerEntityId) //this does not fire when a player damages a block

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when Non-Player entity damages a block.

## LootContainer Events

#### OnLootContainerTouchChanged(TileEntityLootContainer container, ulong oldValue, ulong newValue);

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when the Last touched time of a container changes.  The last touched time is an indicator of the last time a player passed within range of the container.

#### OnLootContainerOpenedTimeChanged(TileEntityLootContainer container, float oldValue, float newValue)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when the Last Opened time of a container changes

#### OnLootContainerItemChanged(TileEntityLootContainer container, int slot, ItemStack oldStack, ItemStack newStack)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when the contents of a loot container changes.  If the change was made by a player adding or removing items, it is only fired after the player closes the container

		
## Chat Command Events

#### OnChatCommand(ClientInfo playerCI, string command, string params)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Fired when a player enters a chat command into the in game chat window.  a chat command is any text that begins with "!"
