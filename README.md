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

![Show Reel](images/titleScreen.png?raw=true)

<details>
  <summary>Show Reel</summary>
  
  <p align='center'>
  <a href="https://www.youtube.com/channel/UCVmjxCnecANeiA-qFCO5DaA">
    <img src="https://img.shields.io/badge/SHOWREEL-%230077B5.svg?&style=for-the-badge&logo=youtube&logoColor=white" />       
  </a>&nbsp;&nbsp;
</p>


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
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.ParticleSpring.java</p>
<p><b>Fields:</b></p>
<ol><li><p>dampingConstant (<i>float</i>): </p></li><li><p>springConstant (<i>float</i>): </p></li><li><p>restLength (<i>float</i>): </p></li></ol>
<h2>Pickable (Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Pickable.java</p>
<p><b>Fields:</b></p>
<ol><li><p>active (<i>boolean</i>): </p></li></ol>
<h2>List (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.List.java</p>
<p><b>Fields:</b></p>
<ol><li><p>spacerZ (<i>float</i>): space each object is from the next one in the z axis</p></li><li><p>indentZ (<i>float</i>): indent of a sub list in the z axis</p></li><li><p>spacerY (<i>float</i>): space each object is from the next one in the y axis</p></li><li><p>indentY (<i>float</i>): indent of a sub list in the y axis</p></li></ol>
<h2>Button (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Button.java</p>
<p><b>Fields:</b></p>
<ol><li><p>functionName (<i>String</i>): this will be the name of what function is activated when this button is pressed</p></li><li><p>active (<i>boolean</i>): </p></li></ol>
<h2>Timer (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Timer.java</p>
<p><b>Fields:</b></p>
<ol><li><p>active (<i>boolean</i>): </p></li><li><p>timeoutFlag (<i>boolean</i>): </p></li><li><p>functionName (<i>String</i>): this will be the name of what function is ativated when this timer runs out</p></li><li><p>timeoutLength (<i>long</i>): </p></li><li><p>repeate (<i>boolean</i>): </p></li><li><p>startFrame (<i>long</i>): </p></li></ol>
<h2>MarchingCubeGeneration (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.MarchingCubeGeneration.java</p>
<p><b>Fields:</b></p>
<ol><li><p>materialID (<i>UUID</i>): </p></li><li><p>chunkSize (<i>int</i>): </p></li><li><p>generationRange (<i>int</i>): </p></li></ol>
<h2>SelectedItems (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.SelectedItems.java</p>
<p><b>Fields:</b></p>
<ol><li><p>pickingHappened (<i>boolean</i>): Flag to tell selection system that a picking event occured and selection needs to clear and update</p></li></ol>
<h2>Mesh (Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Mesh.java</p>
<p><b>Fields:</b></p>
<ol><li><p>vertexPositions (<i>com.boc_dev.maths.objects.vector.Vec3f[]</i>): </p></li><li><p>materialID (<i>UUID</i>): </p></li><li><p>index (<i>com.boc_dev.maths.objects.vector.Vec3i</i>): </p></li></ol>
<h2>TerrainGeneration (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.TerrainGeneration.java</p>
<p><b>Fields:</b></p>
<ol><li><p>octaves (<i>int</i>): </p></li><li><p>segmentSize (<i>int</i>): </p></li><li><p>lacunarity (<i>float</i>): </p></li><li><p>materialID (<i>UUID</i>): </p></li><li><p>amplitude (<i>int</i>): </p></li><li><p>chunkSize (<i>int</i>): </p></li><li><p>cellSpace (<i>int</i>): </p></li><li><p>generationRange (<i>int</i>): </p></li></ol>
<h2>Light (Renderable)</h2>
<p><b>Description:</b> Component that gets affected by the rigid body system. It must be under a transform, and thats the one that gets transformed.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Light.java</p>
<p><b>Fields:</b></p>
<ol><li><p>attenuationExponent (<i>float</i>): </p></li><li><p>coneAngle (<i>float</i>): </p></li><li><p>attenuationLinear (<i>float</i>): </p></li><li><p>attenuationConstant (<i>float</i>): </p></li><li><p>colour (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p></li><li><p>lightingType (<i>LightingType</i>): light type</p></li><li><p>direction (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p></li><li><p>intensity (<i>float</i>): </p></li></ol>
<h2>NormalMap (Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.NormalMap.java</p>
<p><b>Fields:</b></p>
<ol><li><p>path (<i>String</i>): </p></li></ol>
<h2>Collision (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Collision.java</p>
<p><b>Fields:</b></p>
<ol><li><p>collisionRestitution (<i>float</i>): </p></li></ol>
<h2>Transform (Not Renderable)</h2>
<p><b>Description:</b> Transform of an object. Will affect the objects underneath it.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Transform.java</p>
<p><b>Fields:</b></p>
<ol><li><p>scale (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): scale component of transform</p></li><li><p>position (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): positon component of transform</p></li><li><p>rotation (<i>com.boc_dev.maths.objects.QuaternionF</i>): rotation component of transform</p></li></ol>
<h2>ViscousDrag (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.ViscousDrag.java</p>
<p><b>Fields:</b></p>
<ol><li><p>coefficientOfDrag (<i>float</i>): </p></li></ol>
<h2>RigidBody (Not Renderable)</h2>
<p><b>Description:</b> Component that gets affected by the rigid body system. It must be under a transform, and thats the one that gets transformed.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.RigidBody.java</p>
<p><b>Fields:</b></p>
<ol><li><p>mass (<i>double</i>): Mass in kg's of entity.</p></li><li><p>linearMomentum (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): linearMomentum of entity.</p></li><li><p>rigidBodyType (<i>RigidBodyObjectType</i>): Type of rigid body.</p></li><li><p>angularMomentum (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): angularMomentum of entity</p></li><li><p>dimensions (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): Dimensions of entity.</p></li></ol>
<h2>Texture (Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Texture.java</p>
<p><b>Fields:</b></p>
<ol><li><p>path (<i>String</i>): </p></li></ol>
<h2>SkyBox (Renderable)</h2>
<p><b>Description:</b> Skybox used in scene.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.SkyBox.java</p>
<p><b>Fields:</b></p>
<ol><li><p>skyboxType (<i>SkyboxType</i>): Type of geometry used to make sykbox. Can be CUBE or SPHERE</p></li><li><p>distance (<i>float</i>): Distance the skybox is rendered at</p></li><li><p>texture (<i>String</i>): Texture of the skybox</p></li></ol>
<h2>Controllable (Not Renderable)</h2>
<p><b>Description:</b> Object that enables user control to a transform it is under.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Controllable.java</p>
<p><b>Fields:</b></p>
<ol><li><p>sensitivity (<i>float</i>): rotation speed</p></li><li><p>enableLook (<i>boolean</i>): Can rotate object</p></li><li><p>speed (<i>float</i>): translate speed</p></li><li><p>enableMove (<i>boolean</i>): Can translate object</p></li></ol>
<h2>Script (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Script.java</p>
<p><b>Fields:</b></p>
<ol><li><p>script (<i>String</i>): Lua Script file. This is searched for within </p></li></ol>
<h2>ParticleBody (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.ParticleBody.java</p>
<p><b>Fields:</b></p>
<ol><li><p>mass (<i>float</i>): </p></li><li><p>velocity (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): </p></li></ol>
<h2>TerrainChunk (Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.TerrainChunk.java</p>
<p><b>Fields:</b></p>
<ol><li><p>materialID (<i>UUID</i>): </p></li><li><p>origin (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p></li><li><p>grid (<i>float[][]</i>): </p></li><li><p>cellSpace (<i>double</i>): </p></li><li><p>index (<i>com.boc_dev.maths.objects.vector.Vec2i</i>): </p></li></ol>
<h2>Selectable (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Selectable.java</p>
<p><b>Fields:</b></p>
<ol><li><p>selectedMaterialUUID (<i>UUID</i>): </p></li><li><p>selected (<i>boolean</i>): </p></li><li><p>unselectedMaterialUUID (<i>UUID</i>): </p></li></ol>
<h2>WaterGeneration (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.WaterGeneration.java</p>
<p><b>Fields:</b></p>
<ol><li><p>chunkSize (<i>int</i>): </p></li><li><p>cellSpace (<i>int</i>): </p></li><li><p>height (<i>int</i>): </p></li></ol>
<h2>Impulse (Not Renderable)</h2>
<p><b>Description:</b> Impulse given from player.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Impulse.java</p>
<p><b>Fields:</b></p>
<ol><li><p>linearVelocityImpulse (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): linear velocity impulse of entity</p></li><li><p>angularVelocityImpulse (<i>com.boc_dev.maths.objects.vector.Vec3d</i>): angular velocity impulse of entity</p></li></ol>
<h2>Camera (Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Camera.java</p>
<p><b>Fields:</b></p>
<ol><li><p>width (<i>int</i>): </p></li><li><p>cameraObjectType (<i>CameraObjectType</i>): </p></li><li><p>far (<i>float</i>): </p></li><li><p>near (<i>float</i>): </p></li><li><p>CameraProjectionType (<i>CameraProjectionType</i>): </p></li><li><p>height (<i>int</i>): </p></li><li><p>fov (<i>float</i>): </p></li></ol>
<h2>Geometry (Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Geometry.java</p>
<p><b>Fields:</b></p>
<ol><li><p>localTransformation (<i>com.boc_dev.maths.objects.matrix.Matrix4f</i>): </p></li><li><p>material (<i>UUID</i>): </p></li><li><p>modelFile (<i>String</i>): </p></li></ol>
<h2>WaterChunk (Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.WaterChunk.java</p>
<p><b>Fields:</b></p>
<ol><li><p>cellSpace (<i>int</i>): </p></li><li><p>grid (<i>float[][]</i>): </p></li></ol>
<h2>ImpulseControllable (Not Renderable)</h2>
<p><b>Description:</b> Object that enables user control to a transform it is under via linear and angular momentum impulses.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.ImpulseControllable.java</p>
<p><b>Fields:</b></p>
<ol><li><p>angularSpeed (<i>float</i>): Rotation speed.</p></li><li><p>enableRotate (<i>boolean</i>): Can rotate object.</p></li><li><p>linearSpeed (<i>float</i>): Translate speed.</p></li><li><p>enableMove (<i>boolean</i>): Can translate object.</p></li></ol>
<h2>Gravity (Not Renderable)</h2>
<p><b>Description:</b> Component to enable gravity on transform object above.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Gravity.java</p>
<p><b>Fields:</b></p>
<ol><li><p>simple (<i>boolean</i>): If simple gravity is true, each object is accelerated towards negative z axis. If false, it uses universal law of gravitation</p></li><li><p>G (<i>float</i>): Gravitational</p></li></ol>
<h2>Material (Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Material.java</p>
<p><b>Fields:</b></p>
<ol><li><p>specularColour (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p></li><li><p>diffuseColour (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p></li><li><p>reflectance (<i>float</i>): </p></li><li><p>shininess (<i>float</i>): </p></li></ol>
<h2>Boid (Not Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Boid.java</p>
<p><b>Fields:</b></p>
<ol><li><p>velocity (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p></li><li><p>minSpeed (<i>float</i>): </p></li><li><p>lengthAwayGroupSquared (<i>float</i>): </p></li><li><p>lengthAwayMinSquared (<i>float</i>): </p></li><li><p>antiCollideScale (<i>float</i>): </p></li><li><p>perceivedCenterScale (<i>float</i>): </p></li><li><p>velocityMatchScale (<i>float</i>): </p></li><li><p>boundScale (<i>float</i>): </p></li><li><p>speed (<i>float</i>): </p></li><li><p>radius (<i>float</i>): </p></li><li><p>goal (<i>com.boc_dev.maths.objects.vector.Vec3f</i>): </p></li></ol>
<h2>Text (Renderable)</h2>
<p><b>Description:</b> </i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.components.Text.java</p>
<p><b>Fields:</b></p>
<ol><li><p>fontAlignment (<i>FontAlignment</i>): </p></li><li><p>fontSize (<i>float</i>): </p></li><li><p>fontName (<i>String</i>): </p></li><li><p>text (<i>String</i>): </p></li></ol>
</details>
<details><summary>Enumerations</summary><h2>SkyboxType</h2><p><b>Description:</b> Type of object used for the skybox.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.enums.SkyboxType.java</p>
<p><b>Values:</b></p>
<ol><p><li>SPHERE</li><li>CUBE</li></ol><h2>RigidBodyObjectType</h2><p><b>Description:</b> Type of rigid body created, used in rigid body sim to generate the moment of inertia tensor.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.enums.RigidBodyObjectType.java</p>
<p><b>Values:</b></p>
<ol><p><li>CUBOID</li><li>SPHERE</li><li>SPHERE_INNER</li><li>NONE</li></ol><h2>CameraObjectType</h2><p><b>Description:</b> Camera type. Primary is the one used as the main camera. FBO is a secondary camera that can be used to create textures to be rendered to an object.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.enums.CameraObjectType.java</p>
<p><b>Values:</b></p>
<ol><p><li>PRIMARY</li><li>FBO</li></ol><h2>CameraProjectionType</h2><p><b>Description:</b> Type of projection matrix used for camera. Perspective produces a normal 3D camera view, orthographic produces a 2D view.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.enums.CameraProjectionType.java</p>
<p><b>Values:</b></p>
<ol><p><li>PERSPECTIVE</li><li>ORTHOGRAPHIC</li></ol><h2>Orientation</h2><p><b>Description:</b> Direction in which a list positions the objects within it.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.enums.Orientation.java</p>
<p><b>Values:</b></p>
<ol><p><li>HORIZONTAL</li><li>VERTICLE</li></ol><h2>LightingType</h2><p><b>Description:</b> Type of light create in the graphics engine.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.enums.LightingType.java</p>
<p><b>Values:</b></p>
<ol><p><li>POINT</li><li>SPOT</li><li>DIRECTIONAL</li></ol><h2>FontAlignment</h2><p><b>Description:</b> Used to set allignment of text.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.enums.FontAlignment.java</p>
<p><b>Values:</b></p>
<ol><p><li>BEGIN</li><li>END</li><li>CENTER</li></ol><h2>CollisionShape</h2><p><b>Description:</b> Shape used to define how it responds to a collision with another collision shape.</i></p>
<p><b>Class:</b> com.boc_dev.lge_model.generated.enums.CollisionShape.java</p>
<p><b>Values:</b></p>
<ol><p><li>SPEHER</li><li>CUBOID</li></ol></details>

  
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



