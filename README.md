![Build](https://github.com/qualia91/com.boc_dev.lockdown_game_engine/workflows/Lockdown%20Game%20Engine/badge.svg)

![Show Reel](images/titleScreen.png?raw=true)
![Show Reel](images/progress2thumbnail.png?raw=true)

## Boids Simulation
![Infinite Terrain Generation](images/boidsStill.png?raw=true)
## Instanced Rendering
![Infinite Terrain Generation](images/instanceStill.png?raw=true)
## Infinite Terrain Generation
![Infinite Terrain Generation](images/teraainGenOverview.png?raw=true)

For a Show Reel of the game engine, check out my youtube:
https://www.youtube.com/channel/UCVmjxCnecANeiA-qFCO5DaA

## Setup
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

# Clone script below should do the trick:

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
Due to the maven dist of lua not being compatible with java modules, i have includedd a module ready dist of lua in  com.boc_dev.lge_scripting/lib.
To add this to your local maven repo, simple double click the maven_repo_builder.cmd file in that dir.

Then look to com.boc_dev.lge_examples for how to use it!

If you are using IDEA with this game engine, you may struggle with it not finding some dll's. this seems to be a bug with idea and maven, and i have no idea how to fix it other than downloading the necessary dlls from the lwjgl website and putting them in AppData\Local\Temp\lwjgl\3.2.3-build-13

If anyone knows more about this, please let me know!

