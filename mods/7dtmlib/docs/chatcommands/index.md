# Chat Commands

## Creating a ChatCommand method

Below is a basic example of creating and registering a chat command.

This command can be run in the in game chat window using "!customcommand".  Only users or groups who have the permission "custom.permission.name" can use this chat command.

```
public class API: ModApiAbstract
{
	public API ()
	{
		SDTM.API.Instance.RegisterChatCommand ("customcommand", "Command Description", "Help Text", MyChatCommand, "custom.permission.name");
	}

	public static void MyChatCommand(List<string> _params, ClientInfo _cInfo){
		PlayerUtils.SendChatMessageAs (_cInfo, "You ran a chat command, "CustomChatName");
	}
}


```