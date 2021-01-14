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
<h1 align='center'>Game Model</h1>
<details><summary>Components</summary>
<h2>ParticleSpring (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>dampingConstant (<i>float</i>): </p><p>springConstant (<i>float</i>): </p><p>restLength (<i>float</i>): </p><h2>Pickable (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>active (<i>boolean</i>): </p><h2>List (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>spacerZ (<i>float</i>): space each object is from the next one in the z axis</p><p>indentZ (<i>float</i>): indent of a sub list in the z axis</p><p>spacerY (<i>float</i>): space each object is from the next one in the y axis</p><p>indentY (<i>float</i>): indent of a sub list in the y axis</p><h2>Button (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>functionName (<i>String</i>): this will be the name of what function is activated when this button is pressed</p><p>active (<i>boolean</i>): </p><h2>Timer (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>active (<i>boolean</i>): </p><p>timeoutFlag (<i>boolean</i>): </p><p>functionName (<i>String</i>): this will be the name of what function is ativated when this timer runs out</p><p>timeoutLength (<i>long</i>): </p><p>repeate (<i>boolean</i>): </p><p>startFrame (<i>long</i>): </p><h2>MarchingCubeGeneration (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>materialID (<i>UUID</i>): </p><p>chunkSize (<i>int</i>): </p><p>generationRange (<i>int</i>): </p><h2>SelectedItems (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>pickingHappened (<i>boolean</i>): Flag to tell selection system that a picking event occured and selection needs to clear and update</p><h2>Mesh (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>vertexPositions (<i>com.boc_dev.maths.objects.vector.Vec3f[]</i>): </p><p>materialID (<i>UUID</i>): </p><p>index (<i>com.boc_dev.maths.objects.vector.Vec3i</i>): </p><h2>TerrainGeneration (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>octaves (<i>int</i>): </p><p>segmentSize (<i>int</i>): </p><p>lacunarity (<i>float</i>): </p><p>materialID (<i>UUID</i>): </p><p>amplitude (<i>int</i>): </p><p>chunkSize (<i>int</i>): </p><p>cellSpace (<i>int</i>): </p><p>generationRange (<i>int</i>): </p><h2>Light (Renderable)</h2>
<p>Component that gets affected by the rigid body system. It must be under a transform, and thats the one that gets transformed.</p>
<h3>Fields:</h3>
<p>attenuationExponent (<i>float</i>): </p><p>coneAngle (<i>float</i>): </p><p>attenuationLinear (<i>float</i>): </p><p>attenuationConstant (<i>float</i>): </p><p>colour (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p><p>lightingType (<i>LightingType</i>): light type</p><p>direction (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p><p>intensity (<i>float</i>): </p><h2>NormalMap (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>path (<i>String</i>): </p><h2>Collision (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>collisionRestitution (<i>float</i>): </p><h2>Transform (Not Renderable)</h2>
<p>Transform of an object. Will affect the objects underneath it.</p>
<h3>Fields:</h3>
<p>scale (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): scale component of transform</p><p>position (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): positon component of transform</p><p>rotation (<i>com.boc_dev.maths.objects.QuaternionF</i>): rotation component of transform</p><h2>ViscousDrag (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>coefficientOfDrag (<i>float</i>): </p><h2>RigidBody (Not Renderable)</h2>
<p>Component that gets affected by the rigid body system. It must be under a transform, and thats the one that gets transformed.</p>
<h3>Fields:</h3>
<p>mass (<i>double</i>): Mass in kg's of entity.</p><p>linearMomentum (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): linearMomentum of entity.</p><p>rigidBodyType (<i>RigidBodyObjectType</i>): Type of rigid body.</p><p>angularMomentum (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): angularMomentum of entity</p><p>dimensions (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): Dimensions of entity.</p><h2>Texture (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>path (<i>String</i>): </p><h2>SkyBox (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>skyboxType (<i>SkyboxType</i>): Type of geometry used to make sykbox. Can be CUBE or SPHERE</p><p>distance (<i>float</i>): Distance the skybox is rendered at</p><p>texture (<i>String</i>): Texture of the skybox</p><h2>Controllable (Not Renderable)</h2>
<p>Object that enables user control to a transform it is under.</p>
<h3>Fields:</h3>
<p>sensitivity (<i>float</i>): rotation speed</p><p>enableLook (<i>boolean</i>): Can rotate object</p><p>speed (<i>float</i>): translate speed</p><p>enableMove (<i>boolean</i>): Can translate object</p><h2>Script (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>script (<i>String</i>): Lua Script file. This is searched for within </p><h2>ParticleBody (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>mass (<i>float</i>): </p><p>velocity (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): </p><h2>TerrainChunk (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>materialID (<i>UUID</i>): </p><p>origin (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p><p>grid (<i>float[][]</i>): </p><p>cellSpace (<i>double</i>): </p><p>index (<i>com.boc_dev.maths.objects.vector.Vec2i</i>): </p><h2>Selectable (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>selectedMaterialUUID (<i>UUID</i>): </p><p>selected (<i>boolean</i>): </p><p>unselectedMaterialUUID (<i>UUID</i>): </p><h2>WaterGeneration (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>chunkSize (<i>int</i>): </p><p>cellSpace (<i>int</i>): </p><p>height (<i>int</i>): </p><h2>Impulse (Not Renderable)</h2>
<p>Impulse given from player.</p>
<h3>Fields:</h3>
<p>linearVelocityImpulse (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): linear velocity impulse of entity</p><p>angularVelocityImpulse (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): angular velocity impulse of entity</p><h2>Camera (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>width (<i>int</i>): </p><p>cameraObjectType (<i>CameraObjectType</i>): </p><p>far (<i>float</i>): </p><p>near (<i>float</i>): </p><p>CameraProjectionType (<i>CameraProjectionType</i>): </p><p>height (<i>int</i>): </p><p>fov (<i>float</i>): </p><h2>Geometry (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>localTransformation (<i>com.boc_dev.maths.objects.matrix.Matrix4f</i>): </p><p>material (<i>UUID</i>): </p><p>modelFile (<i>String</i>): </p><h2>WaterChunk (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>cellSpace (<i>int</i>): </p><p>grid (<i>float[][]</i>): </p><h2>ImpulseControllable (Not Renderable)</h2>
<p>Object that enables user control to a transform it is under via linear and angular momentum impulses.</p>
<h3>Fields:</h3>
<p>angularSpeed (<i>float</i>): Rotation speed.</p><p>enableRotate (<i>boolean</i>): Can rotate object.</p><p>linearSpeed (<i>float</i>): Translate speed.</p><p>enableMove (<i>boolean</i>): Can translate object.</p><h2>Gravity (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>simple (<i>boolean</i>): If simple gravity is true, each object is accelerated towards negative z axis. If false, it uses universal law of gravitation</p><p>G (<i>float</i>): Gravitational</p><h2>Material (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>specularColour (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p><p>diffuseColour (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p><p>reflectance (<i>float</i>): </p><p>shininess (<i>float</i>): </p><h2>Boid (Not Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>velocity (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p><p>minSpeed (<i>float</i>): </p><p>lengthAwayGroupSquared (<i>float</i>): </p><p>lengthAwayMinSquared (<i>float</i>): </p><p>antiCollideScale (<i>float</i>): </p><p>perceivedCenterScale (<i>float</i>): </p><p>velocityMatchScale (<i>float</i>): </p><p>boundScale (<i>float</i>): </p><p>speed (<i>float</i>): </p><p>radius (<i>float</i>): </p><p>goal (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p><h2>Text (Renderable)</h2>
<p></p>
<h3>Fields:</h3>
<p>fontAlignment (<i>FontAlignment</i>): </p><p>fontSize (<i>float</i>): </p><p>fontName (<i>String</i>): </p><p>text (<i>String</i>): </p></details>
<details><summary>Enumerations</summary><h2>CameraObjectType</h2><p>PRIMARY, FBO, </p><h2>LightingType</h2><p>POINT, SPOT, DIRECTIONAL, </p><h2>FontAlignment</h2><p>BEGIN, END, CENTER, </p><h2>CollisionShape</h2><p>SPEHER, CUBOID, </p><h2>SkyboxType</h2><p>SPHERE, CUBE, </p><h2>RigidBodyObjectType</h2><p>CUBOID, SPHERE, SPHERE_INNER, NONE, </p><h2>CameraProjectionType</h2><p>PERSPECTIVE, ORTHOGRAPHIC, </p><h2>Orientation</h2><p>HORIZONTAL, VERTICLE, </p><h2>TextureType</h2><p>VISUAL, NORMAL, </p></details>


  
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



