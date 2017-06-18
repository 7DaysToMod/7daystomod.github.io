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

Event Wrapper for the ModApiAbstract.ChunkColorsDone method

#### OnChunkAdded(Chunk chunk)

Fired when a chunk has been loaded on the server

#### OnBeforeChunkRemoved(Chunk chunk)

Fired when before a chunk is unloaded on the server

#### OnBeforeChunkSaved(Chunk chunk)

Fired before a chunk is saved on the server

## Game Time Events

#### OnLibTick()

Fired every 40 game ticks.  This rate can be modified in the 7dtmlib config.

#### OnGameMinute(int day, int hour, int minute)

Fired on the change of every in game minute

#### OnGameHour(int day, int hour);

Fired on the changed of every in game hour

## Player Events
- OnPlayerLogin(ClientInfo cInfo, string compatibilityVersion)
- OnPlayerSpawning(EntityPlayer player)
- OnPlayerSpawned(ClientInfo cInfo, RespawnType respawnReason)
- OnPlayerDisconnected(EntityPlayer player)
- OnPlayerDataSaved(ClientInfo cInfo, PlayerDataFile playerDataFile)
- OnPlayerDroppedItem(EntityPlayer player, EntityItem item)
- OnPlayerCollectedItem(EntityPlayer player, ItemStack itemStack)
- OnPlayerBuffAdded(EntityPlayer player, Buff buff)
- OnPlayerBuffRemoved(EntityPlayer player, Buff buff)
- OnPlayerWellnessChanged(EntityPlayer player, float amount)
- OnPlayerKilledByPlayer(EntityPlayer player, EntityPlayer killer)
- OnPersistentPlayerDataEvent(PersistentPlayerData player, PersistentPlayerData otherPlayer, EnumPersistentPlayerDataReason reason)
- OnPlayerACLInviteSent(PersistentPlayerData player, PersistentPlayerData invitedPlayer)
- OnPlayerACLInviteAccepted(PersistentPlayerData player, PersistentPlayerData invitedPlayer)
- OnPlayerACLInviteDeclined(PersistentPlayerData player, PersistentPlayerData invitedPlayer)
- OnPlayerACLRemoved(PersistentPlayerData player, PersistentPlayerData invitedPlayer)


## Entity Events
- OnEntityLoaded(Entity entity)
- OnEntityUnloaded(Entity entity, string reason)
- OnNPCLoaded(EntityNPC entity)
- OnNPCUnloaded(EntityNPC entity, string reason)
- OnNPCBanditLoaded(EntityBandit entity)
- OnNPCBanditUnloaded(EntityBandit entity, string reason)
- OnNPCSurvivorLoaded(EntitySurvivor entity)
- OnNPCSurvivorUnloaded(EntitySurvivor entity, string reason)
- OnTraderPrimaryInventoryChanged(EntityNPC entity, List&lt;ItemStack&gt; previousInventory)
- OnTraderSecretStashChanged(EntityNPC entity, List&lt;ItemStack[]&gt; previousStash)

## Block Events
- OnBlockChanged(Vector3i pos, BlockValue oldBlock, BlockValue newBlock)
- OnBlockDamaged(Vector3i blockPos, BlockValue blockValue, int damage, int attackerEntityId) //this does not fire when a player damages a block

## LootContainer Events
- OnLootContainerTouchChanged(TileEntityLootContainer container, ulong oldValue, ulong newValue);
- OnLootContainerOpenedTimeChanged(TileEntityLootContainer container, float oldValue, float newValue)
- OnLootContainerItemChanged(TileEntityLootContainer container, int slot, ItemStack oldStack, ItemStack newStack)

		
## Chat Command Events
- OnChatCommand(ClientInfo playerCI, string command, string params)
