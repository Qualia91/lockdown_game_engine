<h1 align='center'>
  LOCKDOWN GAME ENGINE
</h1>

<p align='center'>
  <img src="https://github.com/qualia91/lockdown_game_engine/workflows/Lockdown%20Game%20Engine/badge.svg"/>
  <img src="https://img.shields.io/badge/License-MIT-blue.svg"/>
  <img src="https://img.shields.io/github/release/qualia91/lockdown_game_engine.svg"/>
  <img src="https://img.shields.io/github/downloads/qualia91/lockdown_game_engine/total.svg"/>
  <img src="https://badgen.net/badge/Open%20Source%20%3F/Yes%21/blue?icon=github)](https://github.com/Naereen/badges/"/>
</p>

<p align='center'>
  <img src="https://img.shields.io/badge/Java-00ADD8?logo=java&logoColor=white" />
  <img src="https://img.shields.io/badge/Lua-00ADD8?logo=lua&logoColor=white" />
</p>

<details>
  <summary>Show Reel</summary>
  
  <p align='center'>
  <a href="https://www.youtube.com/channel/UCVmjxCnecANeiA-qFCO5DaA">
    <img src="https://img.shields.io/badge/SHOWREEL-%230077B5.svg?&style=for-the-badge&logo=youtube&logoColor=white" />       
  </a>&nbsp;&nbsp;
</p>

![Show Reel](images/titleScreen.png?raw=true)
![Show Reel](images/progress2thumbnail.png?raw=true)
![Infinite Terrain Generation](images/boidsStill.png?raw=true)
![Infinite Terrain Generation](images/instanceStill.png?raw=true)

</details>


<details>
  <summary>How to use release</summary>
  
The release is a runnable jar file that takes in one input, a lua file to be run.

A framework example is provided in:

git clone https://github.com/qualia91/com.boc_dev.lge_lua_front_end

The file in this repo called game_scene.lua is the one that can be provided as a command line input, like:

```
java -jar .\lockdown_game_engine-1.0.0.jar <PATH_TO_REPO>/com.boc_dev.lge_lua_front_end/game_scene.lua
```
  
</details>

<details>
  <summary>How to develop</summary>
  
<h2>Dependancies</h2>
You will need all the following repo's to get the game engine working:

com.nick.wood.game_engine.core: https://github.com/Qualia91/com.boc_dev.lge_core

com.nick.wood.game_engine.event_bus: https://github.com/Qualia91/com.boc_dev.event_bus

com.nick.wood.game_engine.examples: https://github.com/Qualia91/com.boc_dev.lge_examples

com.nick.wood.game_engine.gcs_model: https://github.com/Qualia91/com.boc_dev.lge_model

com.nick.wood.game_engine.systems: https://github.com/Qualia91/com.boc_dev.lge_systems

com.nick.wood.lge_scripting: https://github.com/Qualia91/com.boc_dev.lge_scripting

com.nick.wood.graphics_library: https://github.com/Qualia91/com.boc_dev.graphics_library

com.nick.wood.maths: https://github.com/Qualia91/com.boc_dev.maths

com.nick.wood.physics_library: https://github.com/Qualia91/com.boc_dev.physics_library

com.nick.wood.lge_scripts: https://github.com/Qualia91/com.boc_dev.lge_scripts

com.nick.wood.lge_lua_front_end: https://github.com/Qualia91/com.boc_dev.lge_lua_front_end

game_engine_build: https://github.com/Qualia91/lockdown_game_engine

<h2>Clone Script</h2>
Clone script below should do the trick:

git clone https://github.com/qualia91/com.boc_dev.lge_core

git clone https://github.com/qualia91/com.boc_dev.event_bus

git clone https://github.com/qualia91/com.boc_dev.lge_examples

git clone https://github.com/qualia91/com.boc_dev.lge_model

git clone https://github.com/qualia91/com.boc_dev.lge_systems

git clone https://github.com/qualia91/com.boc_dev.lge_scripting

git clone https://github.com/qualia91/com.boc_dev.graphics_library

git clone https://github.com/qualia91/com.boc_dev.maths

git clone https://github.com/qualia91/com.boc_dev.physics_library

git clone https://github.com/qualia91/lockdown_game_engine

git clone https://github.com/qualia91/com.boc_dev.lge_scripts

git clone https://github.com/qualia91/com.boc_dev.lge_lua_front_end

then you will need to navigate to com.boc_dev.lge_model\def and run generation.lua in lua to generate the java classes that define the model. 

Lua Scripting Update:
Due to the maven dist of lua not being compatible with java modules, i have included a module ready dist of lua in  com.boc_dev.lge_scripting/lib.
To add this to your local maven repo, simple double click the maven_repo_builder.cmd file in that dir.

Then look to com.boc_dev.lge_examples for how to use it!

If you are using IDEA with this game engine, you may struggle with it not finding some dll's. this seems to be a bug with idea and maven, and i have no idea how to fix it other than downloading the necessary dlls from the lwjgl website and putting them in AppData\Local\Temp\lwjgl\3.2.3-build-13

If anyone knows more about this, please let me know!
  
</details>



