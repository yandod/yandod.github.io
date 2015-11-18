---
layout: post
title:  "JavaScriptでマインクラフトMOD作成"
date:   2015-11-17 12:00:00 +9:00
categories: blog
---

マインクラフトのMOD作成といえばJavaを使うのが本来の方法です。
それよりもお手軽なJavaScriptを使う方法があると知り試して見ました。

## ScriptCraft

[https://github.com/walterhiggins/ScriptCraft](https://github.com/walterhiggins/ScriptCraft)

ScriptCraftはJavaScriptを通じてCanaryModやBukkit-compatibleなModのAPIを呼び出す仕組みです。
推奨はCanaryModとなっており、CanaryModで建てたサーバーにScriptCraftを導入する形です。
実際のゲームの動作は標準のクライアントからCanaryModに接続する形になり、マルチプレイヤーに対応したMod開発ができます。

## インストール

### CanaryModのインストール

まずはCanaryModをインストールします。CanaryModは1.8系互換のものも開発中ですが安定版は1.7系です。
公式サイトから1.7系の最新版のjarをダウンロードしてCanaryMod用のディレクトリに保存します。

```
mkdir mcserver
cd mcserver/
curl -O https://canarymod.net/releases/CanaryMod-1.7.10-1.1.3.jar
```

ダウンロードしたCanaryModを起動します。
起動するとjarの内容が展開され設定ファイルやディレクトリが作成されます。

```
$ java -jar CanaryMod-1.7.10-1.1.3.jar
Please wait while the libraries initialize...
Starting: CanaryMod 1.7.10-1.1.3
Canary Path: /Users/yandod/develop/mcserver/CanaryMod-1.7.10-1.1.3.jar & Working From: /Users/yandod/develop/mcserver
Could not find the server configuration at config/server.cfg, creating default.
Could not find the database configuration at config/db.cfg, creating default.
Registered xml Database
Could not find config/ops.cfg. Creating one for you...
You can now add ops to config/ops.cfg (one per line!). We left you a note.
Failed to scan for plugins. 'plugins/' is not a directory. Creating...
[00:02:02] [CanaryMod] [INFO]: Starting: CanaryMod 1.7.10-1.1.3
[00:02:02] [CanaryMod] [INFO]: Canary Path: /Users/yandod/develop/mcserver/CanaryMod-1.7.10-1.1.3.jar & Working From: /Users/yandod/develop/mcserver
[00:02:02] [CanaryMod] [INFO]: Could not find the server configuration at config/server.cfg, creating default.
[00:02:02] [CanaryMod] [INFO]: Could not find the database configuration at config/db.cfg, creating default.
[00:02:02] [CanaryMod] [INFO]: Registered xml Database
[00:02:02] [CanaryMod] [INFO]: Could not find config/ops.cfg. Creating one for you...
[00:02:02] [CanaryMod] [INFO]: You can now add ops to config/ops.cfg (one per line!). We left you a note.
[00:02:02] [CanaryMod] [WARN]: Failed to scan for plugins. 'plugins/' is not a directory. Creating...
[00:02:02] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Starting minecraft server version 1.7.10
[00:02:02] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Loading properties
[00:02:02] [net.minecraft.server.ServerEula] [WARN]: Failed to load eula.txt
[00:02:02] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: You need to agree to the EULA in order to run the server. Go to eula.txt for more info.
[00:02:02] [net.minecraft.server.MinecraftServer] [INFO]: Stopping server
[00:02:02] [net.minecraft.server.MinecraftServer] [INFO]: Saving worlds
[00:02:02] [CanaryMod] [INFO]: Disabling Plugins ...
> [00:02:02] [net.minecraft.server.MinecraftServer] [INFO]: Stopping server
[00:02:02] [net.minecraft.server.MinecraftServer] [INFO]: Saving worlds
[00:02:02] [CanaryMod] [INFO]: Disabling Plugins ...
```

初回起動時は規約への同意を求める形で終了します。
規約に同意するには<code>eula.txt</code>を開き、eula=falseをtrueに変更します。

```
#By changing the setting below to TRUE you are indicating your agreement to our EULA (https://account.mojang.com/documents/minecraft_eula).
#Thu Nov 19 00:02:02 JST 2015
eula=true
```

ここまで済めばあとはCanaryModを再度起動するだけです。

```
$ java -jar CanaryMod-1.7.10-1.1.3.jar
Please wait while the libraries initialize...
Starting: CanaryMod 1.7.10-1.1.3
Canary Path: /Users/yandod/develop/mcserver/CanaryMod-1.7.10-1.1.3.jar & Working From: /Users/yandod/develop/mcserver
Registered xml Database
Failed to translate Username into a UUID
Failed to translate Username into a UUID
Found 0 plugins; total: 0
[00:08:28] [CanaryMod] [INFO]: Starting: CanaryMod 1.7.10-1.1.3
[00:08:28] [CanaryMod] [INFO]: Canary Path: /Users/yandod/develop/mcserver/CanaryMod-1.7.10-1.1.3.jar & Working From: /Users/yandod/develop/mcserver
[00:08:28] [CanaryMod] [INFO]: Registered xml Database
[00:08:29] [CanaryMod] [WARN]: Failed to translate Username into a UUID
[00:08:30] [CanaryMod] [WARN]: Failed to translate Username into a UUID
[00:08:30] [CanaryMod] [INFO]: Found 0 plugins; total: 0
[00:08:30] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Starting minecraft server version 1.7.10
[00:08:30] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Loading properties
[00:08:30] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Generating keypair
[00:08:30] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Starting Minecraft server on *:25565
[00:08:30] [CanaryMod] [INFO]: Could not find the world configuration for default_NORMAL at config/worlds/default, creating default.
[00:08:31] [CanaryMod] [INFO]: Enabling Plugins...
[00:08:31] [net.minecraft.server.MinecraftServer] [INFO]: Preparing start region for level default
[00:08:32] [net.minecraft.server.MinecraftServer] [INFO]: Preparing spawn area: 11%
[00:08:33] [net.minecraft.server.MinecraftServer] [INFO]: Preparing spawn area: 22%
[00:08:34] [net.minecraft.server.MinecraftServer] [INFO]: Preparing spawn area: 35%
[00:08:35] [net.minecraft.server.MinecraftServer] [INFO]: Preparing spawn area: 53%
[00:08:36] [net.minecraft.server.MinecraftServer] [INFO]: Preparing spawn area: 70%
[00:08:37] [net.minecraft.server.MinecraftServer] [INFO]: Preparing spawn area: 89%
[00:08:37] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Done (6.893s)! For help, type "help" or "?"
```

終了する場合はサーバーコンソールに<code>stop</code>と打ちます。

### ScriptCraftのインストール

次にScriptCraftをインストールします。

[http://scriptcraftjs.org/download/latest/](http://scriptcraftjs.org/download/latest/)

SciptCraftはCanaryModのプラグインとしてインストールします。
具体的にはpluginsディレクトリの下に配置し、CanaryModを起動します。

```
$ ls -l
total 45096
-rw-r-----@  1 yandod  staff  23078132 11 19 00:00 CanaryMod-1.7.10-1.1.3.jar
drwxr-xr-x   7 yandod  staff       238 11 19 00:08 config
drwxr-xr-x   2 yandod  staff        68 11 19 00:02 databases
drwxr-xr-x  12 yandod  staff       408 11 19 00:08 db
-rw-r--r--   1 yandod  staff       180 11 19 00:04 eula.txt
drwxr-xr-x   3 yandod  staff       102 11 19 00:08 lang
drwxr-xr-x   4 yandod  staff       136 11 19 00:08 logs
drwxr-xr-x   2 yandod  staff        68 11 19 00:02 plugins
-rw-r--r--   1 yandod  staff         2 11 19 00:08 usercache.json
drwxr-xr-x   5 yandod  staff       170 11 19 00:08 worlds
```

ダウンロードページからjarへのURLを取得しダウンロード。

```
$ cd plugins
$ curl -O http://scriptcraftjs.org/download/latest/scriptcraft-3.1.10/scriptcraft.jar
```

ダウンロードが完了した再度、CanaryModを起動するとScriptCraftが展開されインストールされます。

```
$ java -jar CanaryMod-1.7.10-1.1.3.jar
Please wait while the libraries initialize...
Starting: CanaryMod 1.7.10-1.1.3
Canary Path: /Users/yandod/develop/mcserver/CanaryMod-1.7.10-1.1.3.jar & Working From: /Users/yandod/develop/mcserver
Registered xml Database
Failed to translate Username into a UUID
Failed to translate Username into a UUID
Found 1 plugins; total: 1
[00:17:15] [CanaryMod] [INFO]: Starting: CanaryMod 1.7.10-1.1.3
[00:17:15] [CanaryMod] [INFO]: Canary Path: /Users/yandod/develop/mcserver/CanaryMod-1.7.10-1.1.3.jar & Working From: /Users/yandod/develop/mcserver
[00:17:15] [CanaryMod] [INFO]: Registered xml Database
[00:17:17] [CanaryMod] [WARN]: Failed to translate Username into a UUID
[00:17:17] [CanaryMod] [WARN]: Failed to translate Username into a UUID
[00:17:17] [CanaryMod] [INFO]: Found 1 plugins; total: 1
[00:17:18] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Starting minecraft server version 1.7.10
[00:17:18] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Loading properties
[00:17:18] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Generating keypair
[00:17:18] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Starting Minecraft server on *:25565
[00:17:18] [CanaryMod] [INFO]: Enabling Plugins...
[00:17:18] [ScriptCraft] [INFO]: Directory /Users/yandod/develop/mcserver/scriptcraft does not exist.
[00:17:18] [ScriptCraft] [INFO]: Initializing /Users/yandod/develop/mcserver/scriptcraft directory with contents from plugin archive.
〜省略〜
[00:17:20] [ScriptCraft] [WARN]: alias plugin is not yet supported in CanaryMod
[00:17:21] [ScriptCraft] [WARN]: commando-test not yet supported in CanaryMod
[00:17:21] [ScriptCraft] [WARN]: commando plugin is not yet supported in CanaryMod
[00:17:21] [ScriptCraft] [WARN]: cow-clicker minigame is not yet supported in CanaryMod and Craftbukkit
[00:17:21] [net.minecraft.server.MinecraftServer] [INFO]: Preparing start region for level default
[00:17:22] [net.minecraft.server.dedicated.DedicatedServer] [INFO]: Done (4.029s)! For help, type "help" or "?"
[00:17:22] [ScriptCraft] [INFO]: js-patch setTimeout() test complete
```

## ScriptCraftの動作確認

ScriptCraftの動作確認をクライアントから行います。
1.7.10を指定したプロファイルを作りクライアントを起動します。
マルチプレイヤーモードを選択し、サーバーアドレスにlocalhostを指定して接続します。

<iframe width="420" height="315" src="https://www.youtube.com/embed/dNjWhL4kZSo" frameborder="0" allowfullscreen></iframe>

次に接続した自分のユーザーにサーバー側から管理者権限を与えます。

```
[00:40:31] [net.minecraft.server.MinecraftServer] [INFO]: yandod joined the game
> op yandod
> [00:40:37] [CanaryMod] [INFO]: [SERVER] Opped yandod
[00:41:08] [net.minecraft.server.MinecraftServer] [INFO]: [yandod: Set the time to 200]
[00:41:08] [CanaryMod] [INFO]: Command used by yandod: /time set 200
[00:41:18] [CanaryMod] [INFO]: Command used by yandod: /js 2 + 3
```

これにより接続中のプレイヤーが管理者となり管理コマンドの実行とJavaScriptの実行が許可されます。
JavaScriptはコンソールから<code>/js 2 + 3</code>のように実行できます。

<iframe width="420" height="315" src="https://www.youtube.com/embed/SCGi8O-19N0" frameborder="0" allowfullscreen></iframe>

これでJavaScriptでModを開発する準備が出来ました。

## Hello World

ではプレイヤーが接続した際にメッセージを出力するModを作ってみます。
Modは<code>scriptcraft/plugins/</code>配下にjsファイルを作成して開発します。

今回は<code>scriptcraft/plugins/helloworld.js</code>を作成し、次のように記述します。

```JavaScript
function onJoin( event ) {
  echo( event.player, 'Hello World');
}
events.connection( onJoin );
```

CanaryModを再度起動し、クライントから再接続します。

<iframe width="420" height="315" src="https://www.youtube.com/embed/hSR4B1XKvBg" frameborder="0" allowfullscreen></iframe>

動きました！

あとはCanaryModのAPIを使ってコマンドを追加したりロジックを追加したりと自由にできます。
ScriptCraftに同梱されたサンプルを見ると色々な例があるので参考にしましょう。

[https://github.com/walterhiggins/ScriptCraft/tree/master/src/main/js/plugins](https://github.com/walterhiggins/ScriptCraft/tree/master/src/main/js/plugins)
