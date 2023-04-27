# FAQ
We thought that you may have some questions about our bot, so here is a small Q&A. We hope that this will help you!

### How does this work?
When you install *minecraft-addon* your server will be able to connect to the BedrockBridge discord bot. If you invite this bot to your discord server, chat will be streamed and you will be able to run several useful commands form discord.
So this is the configuration:
* Minecraft-Server <-> BedrockBridge Bot <-> DiscordServer

### It doesn't work! What should I do?
First thing to do is understanding where the problem is:
* Does the addon work at all? Log into your bedrock server and run `!status` in chat. If you simply see in chat "!status" then the addon is not working. Most common reasons for this error are: 
  * Your world doesn't have *experiments* on.
  * You are using the wrong version: there is a version of this pack for each major minecraft update. Versions are not interchangeable (you need to instal the right one). Check the github [*tags*](https://github.com/InnateAlpaca/BedrockBridge/tags) for the right one.
* Nice it works... but it says "offline". Then your server was not able to connect to the bot, try to run in chat `!messages` and see if is there any. Most probable issue is:
  * You haven't added the token to the [config file](BedrockBridge#bedrock-setup) (or your token is no longer valid, in this case request a new one from your discord server).
* Nope that was all fine, but I still can't see the chat! Well, in this case the problem is with discord setup. 
  * make sure that you ran `/setup` on your discord server
  * try to reinvite the bot
  * give the bot ADMIN permissions. (Some servers have options that will prevent the bot from setting up webhooks)

If you are still having troubles don't hesitate to **contact us** on the [official discord](https://discord.gg/A2SDjxQshJ) or open a [ticket](https://github.com/InnateAlpaca/BedrockBridge/issues) here on github.

*Note: Github tickets will typically take longer to be addressed than discord reports.*

### How is it possible that everyone can run all commands??
Yes, some bots let you choose what roles can run certain commands, why does this bot not do it? well yes I still need to code that part, that's a reason. Another reason is that discord already allows you to do that natively. 
**How?**
Go to `Menu->Integrations->BedrockBridge` and you will find a list of commands. You can chose what roles can run bot's commands, and what channels can the commands be run from. Then you can even customise single commands' permissions. 
Here's an example ![discord_setup](https://i.imgur.com/QRKOWRb.png) 

### Updating the pack: how do I do?
Installing them on your server is very easy:
1) download the new pack and unzip server_pack.
2) now take the content of development_behaviour_pack folder and past it into the folder with the same name on your server-folder (replacing the old existing one). 
3) when you restart the server the new version will be working (but you don't need to do it immediately).
Note another way to summarize this is "replace the old `main.js` with the new `main.js`"