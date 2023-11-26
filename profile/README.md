<img width="1920" alt="Artboard_272x" src="https://github.com/mc-nations/.github/assets/44354000/5f00753e-a4cb-4d6e-bbd4-de5d02da147b">


# Minecraft Nations

In this github organization you will find consolidated all the code and all the plugins that [Timo](https://github.com/TPausL), [Joshi](https://github.com/Jozys) and me ([Yannik](https://github.com/ItsZiroy)) wrote for the project. Be mindful that not all plugins are perfect, and some contain fixed German language strings that we didn't have the time to put into language files. If you would like to use any of the plugins, feel free to do so and create a PR to fix the language strings. We will happily merge it. If you need any help setting up or using the plugins, feel free to contact me on discord (ziroy).

## What repositories are there?

- [Nations](https://github.com/mc-nations/nations) - This is the main plugin that handles all the utility stuff like team management, random spawns, chat and everything that we thought doesn't deserve its own plugin.
- [ServerTimeLock](https://github.com/mc-nations/server-time-lock) - This plugin is used to lock the server at a specific time. Mainly known as the server opening times.
- [PlayerTimeLimit](https://github.com/mc-nations/player-time-limit) - This is a fork of the [PlayerTimeLimit Plugin](https://github.com/Ajneb97/PlayerTimeLimit) by Ajneb97 that uses gradle as a built tool like all our repositories and allows for a weekly time limit instead of a daily.
- [ShrineRevive](https://github.com/mc-nations/shrine-revive) - This plugin is used to revive players at the shrine and makes sure that dead players cannot join the server.
- [BukkitRedisInterface](https://github.com/mc-nations/bukkit-redis-interface) - This is a pretty handy plugin that allows us to publish events from the minecraft server on redis and subscribe to them on other platforms like discord or the web. It is used as a foundation plugin by all the other ones.
- [Nations Discord Bot](https://github.com/mc-nations/discord-bot) - This is the discord bot that we use to publish events from the minecraft server on discord and distribute roles etc. It uses the events published on the redis.
- [MC-To-Redis-Utility](https://github.com/mc-nations/mc-to-redis-utility) - This utility plugins only purpose is to add the discord uuid of a player to all events. We use DiscordSRV for the conenction. We use a custom [fork](https://github.com/mc-nations/DiscordSRV) of DiscordSRV that fixes one of their voice chat issues. Mainly not deleting groups when two or more people leave the network. Unfortunately, DiscordSRV still seems to be incapable of handling a large amount of users, which is why we switched to the [simple voice chat mod](https://modrinth.com/plugin/simple-voice-chat/versions) instead. 
- [Config/Docker](https://github.com/mc-nations/config) - And now to bring it all together. This is the configuration repository that contains all the plugins and its configs that we used to run the project. If you want a one to one replica of the project, you can simply run the docker compose file in this repository and you are good to go.

## How do I build the plugins?
All jars can be found under https://github.com/mc-nations/config/tree/main/plugins. But those are in the version that we used, maybe containing some fixed German strings, so you will have to clone the project and manually build it, if you want to change that. Simply use the gradle wrapper to build the jar afterwards. Some projects will have the fatJar/ shadow jar plugin. For those to function, you will have to build a shadow jar.

## License
The code and the plugins are **all** licensed under the MIT license. You can find the license [here](/LICENSE.txt). If you use any of the plugins, we would appreciate it if you would give us credit and let us know what cool projects you have come up with :)
