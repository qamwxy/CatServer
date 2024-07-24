# CatServer (1.16.5)
![](https://img.shields.io/badge/Minecraft-1.16.5-brightgreen.svg?colorB=469C00)
![](https://img.shields.io/badge/Forge-36.2.39-brightgreen.svg?colorB=469C00)
![](https://img.shields.io/badge/Spigot-1.16.5-brightgreen.svg?colorB=469C00)

CatServer is a high-performance Forge+Bukkit+Spigot server core.<br>
The early 1.16.5 version was co-developed with the LoliServer project team. Currently supports most mods and plugins to run stably stably.<br>
It will now continue to be maintained as a fork of LoliServer, providing better optimization and compatibility.<br>
You can download the latest version from [Jenkins](https://jenkins.rbqcloud.cn:30011/job/CatServer-1.16.5/lastSuccessfulBuild/).<br>

All versions of CatServer:
|    Version    |    Status     |
| ------------- | ------------- |
| [1.18.2](https://github.com/Luohuayu/CatServer/tree/1.18.2)  |  Active      |
| [1.16.5](https://github.com/Luohuayu/CatServer/tree/1.16.5)  |  LTS/STABLE  |
| [1.12.2](https://github.com/Luohuayu/CatServer/tree/1.12.2)  |  LTS/STABLE  |

QQ Group: [591257](https://jq.qq.com/?_wv=1027&k=5B5aKkW) | Telegram: [@CatServer](https://t.me/CatServer) | Discord: [点击加入](https://discord.gg/wvBJN4d)

### Features
Uses self-written optimization and some Paper optimization to greatly improve performance.<br>
Has a powerful Remap system to ensure good plugin compatibility.<br>
Has a good compatibility with FakePlayer.<br>
Fixes most vanilla bugs related to safety.<br>
Has very user-friendly configuration.<br>
Provides API allowing plugins to interact with mods easily.<br>

### Installation
1. Download or build the latest version.
2. Create startup script and run (Sample script: java -Xmx2G -jar CatServer-1.16.5-xxxxxxx-server.jar).
3. Wait for the libraries and assets to download on the first startup.

##### Recommended to run on Java 8 or 11, although Java 12-17 and later versions are supported, although there may be compatibility issues with mods and plugins.

### Building
- 1.Clone 1.16.5 branch: `git clone -b 1.16.5 https://github.com/Luohuayu/CatServer.git`.
- 2.Open directory: `cd CatServer`.
- 3.Setup project: `gradlew setup`.
- 4.Generate patch(If you modify the Minecraft code): `gradlew genPatches`.
- 5.Build: `gradlew buildCatServer`

### Generate dependency
1. Run the server, Wait for the libraries to download and generate the SRG.
2. Import the following jar in order as dependencies (Add more libraries if you need to use):
```
libraries/net/minecraftforge/forge/{MC_VERSION}-{FORGE_VERSION}/forge-{MC_VERSION}-{FORGE_VERSION}-universal.jar
libraries/net/minecraftforge/forge/{MC_VERSION}-{FORGE_VERSION}/forge-{MC_VERSION}-{FORGE_VERSION}-server.jar
libraries/net/minecraft/server/{MC_VERSION}-{MCP_VERSION}/server-{MC_VERSION}-{MCP_VERSION}-srg.jar
libraries/net/minecraftforge/eventbus/{EVENTBUS_VERSION}/eventbus-{EVENTBUS_VERSION}.jar
libraries/net/minecraftforge/forgespi/{SPI_VERSION}/forgespi-{SPI_VERSION}.jar
```
