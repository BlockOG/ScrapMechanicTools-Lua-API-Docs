---
sidebar_position: 3
title: Constants
hide_title: true
sidebar-label: 'Constants'
---

<br></br>

## Class Constants

### ShapeClass

Listed below are <code>ShapeClass</code> constants that can be set like this:

```lua
MyShape = class()

MyShape.colorHighlight = sm.color.new( "#ff0000" )
MyShape.colorNormal = sm.color.new( "#00ff00" )
--etc. etc.
```

<strong>colorHighlight</strong> <br></br>
Sets the connection-point highlight color. <br></br>
The connection-point is shown when using the Connect Tool and selecting the interactable. <br></br>
Defaults to white.

- <code>highlightColor</code> [<strong> color </strong>]: The connection-point's highlight color.

---

<strong>colorNormal</strong> <br></br>
Sets the connection-point normal color. <br></br>
The connection-point is shown when using the Connect Tool. <br></br>
Defaults to gray.

- <code>normalColor</code> [<strong> color </strong>]: The connection-point's normal color.

---

<strong>connectionInput</strong> <br></br>
Sets the input connection type. <br></br>

See [sm.interactable.connectionType](/lua/Game-Script-Environment/Constants#sminteractableconnectiontype) for details. <br></br>
Defaults to 0, no input.

- <code>connectionType</code> [<strong> int </strong>]: The input connection type.

---

<strong>connectionOutput</strong> <br></br>
Sets the output connection type. <br></br>

See [sm.interactable.connectionType](/lua/Game-Script-Environment/Constants#sminteractableconnectiontype) for details. <br></br>
Defaults to 0, no output.

- <code>connectionType</code> [<strong> int </strong>]: The output connection type.

---

<strong>maxParentCount</strong> <br></br>
Sets the maximum number of allowed parent connections - the number of input connections. <br></br>
Defaults to 0, no allowed parent connections.

:::info note
Implement [client_getAvailableParentConnectionCount](/Game-Script-Environment/Classes/ShapeClass#getavailableparentconnectioncount) to control specific types.
:::

- <code>maxParents</code> [<strong> int </strong>]: The maximum amount of input connections.

---

<strong>maxChildCount</strong> <br></br>
Sets the maximum number of allowed child connections - the number of output connections. <br></br>
Defaults to 0, no allowed child connections.

:::info note
Implement [client_getAvailableChildConnectionCount](/Game-Script-Environment/Classes/ShapeClass#getavailablechildconnectioncount) to control specific types.
:::

- <code>maxChildren</code> [<strong> int </strong>]: The maximum amount of output connections.

---

<strong>poseWeightCount</strong> <br></br>
Sets the number of animation poses the shape's model is able to use. <br></br>

Value are integers 0-3 (Defaults to 0, no poses).

A value greater that 0 indicates that the renderable's mesh is set up to blend into <code>pose0</code>, <code>pose1</code>, <code>pose2</code>. <br></br>

This is, for example, used to move the lever on the engine.

- <code>poseWeightCount</code> [<strong> int </strong>]: The number of animation poses.

---

### UnitClass

<strong>isSaveObject</strong> <br></br>
Enables or disables saving of this unit. (Defaults to true) <br></br>

If enabled, the [Unit](/lua/Game-Script-Environment/Userdata/Unit) will be recreated when loading a game. Otherwise, the [Unit](/lua/Game-Script-Environment/Userdata/Unit) is considered a temporary object.

:::info note
If disabled, <code>self.storage</code> can not be used.
:::

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether saving the unit is enabled or not.

---

### GameClass

<strong>defaultInventorySize</strong> <br></br>
Sets default player inventory size. <br></br>
Defaults to 40.

- <code>size</code> [<strong> int </strong>]: The inventory size.

---

<strong>enableAggro</strong> <br></br>
Enables or disables enemy aggression. <br></br>
Defaults to true.

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether enemy aggression is enabled or not.

---

<strong>enableAmmoConsumption</strong> <br></br>
Enables or disables ammo consumption. <br></br>
Defaults to false.

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether ammo consumption is enabled or not.

---

<strong>enableFuelConsumption</strong> <br></br>
Enables or disables fuel consumption. <br></br>
Defaults to false.

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether fuel consumption is enabled or not.

---

<strong>enableLimitedInventory</strong> <br></br>
Enables or disables limited inventory. <br></br>
Defaults to false.

When limited in inventory is on, items have a limited amount. <br></br>
When off, the player has access to all items. (Except for items with json value "hidden": true)

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether the inventory is limited or not.

---

<strong>enableRestrictions</strong> <br></br>
Enables or disables build restrictions. <br></br>
Defaults to false.

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether building is restricted or not.

---

<strong>enableUpgrade</strong> <br></br>
Enables or disables interactable part upgrade. <br></br>
Defaults to false.

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether part upgrades are enabled or not.

---

### HarvestableClass

<strong>poseWeightCount</strong> <br></br>
Sets the number of animation poses the harvestable's model is able to use. <br></br>

Value are integers 0-3 (Defaults to 0, no poses).

A value greater that 0 indicates that the renderable's mesh is set up to blend into <code>pose0</code>, <code>pose1</code>, <code>pose2</code>. <br></br>

- <code>highlightColor</code> [<strong> color </strong>]: The connection-point's normal color.

---

### WorldClass

<strong>cellMaxX</strong> <br></br>
Terrain generation maximum cell position in X axis. <br></br>
Default = 0

- <code>maxX</code> [<strong> int </strong>]: The maximum X cell position.

---

<strong>cellMaxY</strong> <br></br>
Terrain generation maximum cell position in Y axis. <br></br>
Default = 0

- <code>maxY</code> [<strong> int </strong>]: The maximum Y cell position.

---

<strong>cellMinX</strong> <br></br>
Terrain generation minimum cell position in X axis. <br></br>
Default = 0

- <code>minX</code> [<strong> int </strong>]: The minimum X cell position.

---

<strong>cellMinY</strong> <br></br>
Terrain generation minimum cell position in Y axis. <br></br>
Default = 0

- <code>minY</code> [<strong> int </strong>]: The minimum Y cell position.

---

<strong>enableAssets</strong> <br></br>
Enables or disables terrain assets for this world. <br></br>
Default = true

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether terrain assets are enabled or not.

---

<strong>enableClutter</strong> <br></br>
Enables or disables terrain clutter for this world. <br></br>
Default = true

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether terrain clutter is enabled or not.

---

<strong>enableCreations</strong> <br></br>
Enables or disables creations for this world. <br></br>
Default = true

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether creations are enabled or not.

---

<strong>enableHarvestables</strong> <br></br>
Enables or disables terrain harvestables for this world. <br></br>
Default = true

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether terrain harvestables are enabled or not.

---

<strong>enableKinematics</strong> <br></br>
Enables or disables terrain kinematics for this world. <br></br>
Default = true

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether terrain kinematics are enabled or not.

---

<strong>enableNodes</strong> <br></br>
Enables or disables nodes for this world. <br></br>
Default = true

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether nodes are enabled or not.

---

<strong>enableSurface</strong> <br></br>
Enables or disables terrain surface for this world. <br></br>
Default = true

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether the terrain surface is enabled or not.

---

<strong>groundMaterialSet</strong> <br></br>
Sets the ground material set used by the terrain. <br></br>
Default = "$GAME_DATA/Terrain/Materials/gnd_standard_materialset.json"

- <code>materialSet</code> [<strong> string </strong>]: The full <code>$-</code> file path to the material set.

---

<strong>isIndoor</strong> <br></br>
Enables or disables indoor mode. <br></br>
Default = false

Indoor worlds have only one terrain cell, at <code>0, 0</code>

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether indoor mode is enabled or not.

---

<strong>renderMode</strong> <br></br>
Sets the render mode for this world. <br></br>
Default = "outdoor"

Valid = "outdoor", "challenge", "warehouse"

- <code>renderMode</code> [<strong> string </strong>]: The render mode.

---

<strong>terrainScript</strong> <br></br>
Sets the script used to generate terrain. <br></br>

- <code>script</code> [<strong> string </strong>]: The full <code>$-</code> file path to the terrain generation script.

---

<strong>worldBorder</strong> <br></br>
Adds borders to the world to prevent objects from falling through the ground. <br></br>
Defaults to true.

- <code>enable</code> [<strong> bool </strong>]: Whether world borders are enabled or not.

---

### ScriptableObjectClass

<strong>isSaveObject</strong> <br></br>
Enables or disables saving of this scriptable object. <br></br>
Default = false

If enabled, the [ScriptableObject](/lua/Game-Script-Environment/Userdata/ScriptableObject) will be recreated when loading a game. <br></br>
Otherwise, the [ScriptableObject](/lua/Game-Script-Environment/Userdata/ScriptableObject) is considered a temporary object. <br></br>

:::info note
If disabled, self.storage can not be used.
:::

- <code>enable</code> [<strong> bool </strong>]: A boolean indicating whether saving this object is enabled or not.

---

## Namespace Constants

### sm

- <code>sm.isHost</code> [<strong> bool </strong>]: Whether the game is currently running on the hosting player's computer.

- <code>sm.version</code> [<strong> string </strong>]: The current version of the game as a string.

---

### sm.areaTrigger.filter
	
Filters are used to specify what object types an area trigger is able to detect. <br></br>
If an area trigger is created with a filter, it will only react to objects of that type. <br></br>
Filters can be combined by adding them. <br></br>

```lua title="Table Contents"
{
	dynamicBody = 1,
	staticBody = 2,
	character = 4,
	areatrigger = 8,
	harvestable = 512,
	lift = 1024,
	voxelTerrain = 32768,
	all = 34319
}
```

---

### sm.audio.soundList
	
A table containing all sounds that can be played using [sm.audio.play](/lua/Game-Script-Environment/Static-Functions/sm.audio#play)

```lua title="Table Contents"
{   
    "Ambient - Birds",
    "Ambient - Challenge",
    "Ambient - Field",
    "Blueprint - Build",
    "Blueprint - Camera",
    "Blueprint - Close",
    "Blueprint - Delete",
    "Blueprint - Open",
    "Blueprint - Save",
    "Blueprint - Select",
    "Blueprint - Share",
    "Brake",
    "Button off",
    "Button on",
    "Challenge - Fall",
    "Challenge - Start",
    "Challenge - Supervisor generic",
    "Character crouch",
    "Character get up",
    "Character hit",
    "Character jump",
    "Character land",
    "Character movement",
    "Character movement crouched",
    "Character wind",
    "Collision - Debris",
    "Collision - Multiple",
    "Collision - Rolling",
    "Collision - Single",
    "Collision - Sliding",
    "Collision - Vehicle",
    "ConnectTool",
    "ConnectTool - Equip",
    "ConnectTool - Idle",
    "ConnectTool - Released",
    "ConnectTool - Rotate",
    "ConnectTool - Selected",
    "ConnectTool - Unequip",
    "Construction - Block attached to joint",
    "Construction - Block placed",
    "Construction - Resize",
    "Dancebass",
    "Dancedrum",
    "Dancepad",
    "Dancevoice",
    "Destruction - Block destroyed",
    "Destruction - Resize",
    "ElectricEngine",
    "GUI Backpack closed",
    "GUI Backpack opened",
    "GUI Inventory highlight",
    "GUI Item drag",
    "GUI Item released",
    "GUI Quickbar highlight",
    "GUI Shape rotate",
    "Gas Explosion",
    "Gas Leak",
    "GasEngine",
    "Handbook - Close",
    "Handbook - Equip",
    "Handbook - Highlight",
    "Handbook - Open",
    "Handbook - Turn page",
    "Handbook - Unequip",
    "Horn",
    "Lever off",
    "Lever on",
    "Lift - Pickup object",
    "Lift placed",
    "Lift usage",
    "Music",
    "PaintTool - Close",
    "PaintTool - ColorPick",
    "PaintTool - Equip",
    "PaintTool - Erase",
    "PaintTool - Open",
    "PaintTool - Paint",
    "PaintTool - Reload",
    "PaintTool - Unequip",
    "Phaser",
    "Piston",
    "PotatoRifle - Equip",
    "PotatoRifle - NoAmmo",
    "PotatoRifle - Reload",
    "PotatoRifle - Shoot",
    "PotatoRifle - Unequip",
    "Radio",
    "RaftShark",
    "Retrobass",
    "Retrodrum",
    "Retrofmblip",
    "Retrovoice",
    "Retrowildblip",
    "Reverb - Challenge",
    "Reverb - Field",
    "Seat seated",
    "Seat unseated",
    "Sensor off",
    "Sensor on",
    "SequenceController",
    "SequenceController change rotation",
    "Sledgehammer - Equip",
    "Sledgehammer - Swing",
    "Sledgehammer - Unequip",
    "Suspension",
    "Thruster",
    "Thruster dust",
    "Toilet seated",
    "Toilet unseated",
    "Weapon - Hit",
    "WeldTool - Case 1",
    "WeldTool - Case 2",
    "WeldTool - Equip",
    "WeldTool - Error",
    "WeldTool - Sparks",
    "WeldTool - Unequip",
    "WeldTool - Weld"
}
```

---

### sm.camera.state
	
Camera states are used to specify how the camera will view the world. <br></br>
The default state is meant for normal gameplay and the first-person and third-person states are meant to be used in cutcenes.

```lua title="Table Contents"
{   
    default = 1,
    cutsceneFP = 2,
    cutsceneTP = 3,
    forcedTP = 4,
    gyroSeatFP = 5,
    gyroSeatTP = 6
}
```

---

### sm.construction.constants
	
Constants used by the construction system.

- subdivideRatio - The physical size of one block.
- subdivideRatio_2 - The physical size of one block divided by two.
- subdivisions - 1 dividided by subdivideRatio.
- shapeSpacing - Bias value.

```lua title="Table Contents"
{   
    subdivideRatio = 0.25,
    subdivideRatio_2 = 0.125,
    subdivisions = 4,
    shapeSpacing = 0.004 
}
```

---

### sm.interactable.types
	
The table of types that an interactable can be.

```lua title="Table Contents"
{
    "electricEngine",
    "gasEngine",
    "steering",
    "seat",
    "controller",
    "button",
    "lever",
    "sensor",
    "thruster",
    "radio",
    "horn",
    "tone",
    "logic",
    "timer",
    "particlePreview",
    "spring",
    "pointLight",
    "spotLight",
    "chest",
    "itemStack",
    "scripted",
    "piston", 
    "simpleInteractive",
    "camera",
    "waypoint",
    "survivalThruster",
    "survivalPiston",
    "survivalSpring",
    "survivalSequence",
    "survivalSensor"
}
```

---

### sm.interactable.actions
	
A table containing all key actions that can be received by an interactable's <code>client_onAction</code> callback.

```lua title="Table Contents"
{
    none = 0,
    left = 1,
    right = 2,
    forward = 3,
    backward = 4,
    item0 = 5,
    item1 = 6,
    item2 = 7,
    item3 = 8,
    item4 = 9,
    item5 = 10,
    item6 = 11,
    item8 = 13,
    item7 = 12,
    item9 = 14,
    use = 15,
    jump = 16,
    exit = 17,
    attack = 18,
    create = 19,
    zoomIn = 20,
    zoomOut = 21
}
```

---

### sm.interactable.connectionType
	
A table containing all available connection types for interactables.

```lua title="Table Contents"
{
    none = 0,
    logic = 1,
    power = 2,
    bearing = 4,
    seated = 8,
    piston = 16,
    gasoline = 256,
    electricity = 512,
    water = 1024,
    ammo = 2048
}
```

---

### sm.interactable.steering
	
Flags used with the steering component.

```lua title="Table Contents"
{
    left = 1,
    right = 2,
    forward = 4,
    backward = 8
}
```

---

### sm.interactable.steering
	
A table of available interactable types.

```lua title="Table Contents"
{
"electricEngine",
"gasEngine",
"steering",
"seat",
"controller",
"button",
"lever",
"sensor",
"thruster",
"radio",
"horn",
"tone",
"logic",
"timer",
"particlePreview",
"spring",
"pointLight",
"spotLight",
"chest",
"scripted",
"piston",
"simpleInteractive",
}
```

---

### sm.joint.types
	
A table of joint types.

```lua title="Table Contents"
{
    "bearing",
    "piston"
}
```

---

### sm.pathfinder.conditionProperty
	
A table of condition link types.

```lua title="Table Contents"
{
    height = 0,
    target = 1,
    none = 2
}
```

---

### sm.physics.filter
	
A table of physics filter types used for things like [raycasts](/lua/Game-Script-Environment/Static-Functions/sm.physics#raycast).

```lua title="Table Contents"
{
    all = -1,
    dynamicBody = 1,
    staticBody = 2,
    character = 4,
    areaTrigger = 8,
    terrainSurface = 128,
    terrainAsset = 256,
    harvestable = 512,
    joints = 4096,
    static = 34690,
    default = 38791,
    voxelTerrain = 32768,
}
```

---

### sm.physics.types
	
Physics types are used to define an object's characteristics is in the physics world. <br></br>
Upon a raycast or collision detection, these types are used to find out what object was intersected.

```lua title="Table Contents"
{
    "invalid",          --No object.
    "terrainSurface",   --The ground.
    "terrainAsset",     --Trees and boulders.
    "lift",             --A Lift.
    "body",             --A Body.
    "character",        --A Character.
    "joint",            --A Joint.
    "harvestable",      --A Harvestable.
    "vision"            --A collision area used by sensors.
}
```

---

### sm.tool.interactState
	
The interact state describe what kind of interaction is made. <br></br>
This is used to check whether a mouse button or key was just pressed, held, etc.

```lua title="Table Contents"
{
    null = 0,   --No interaction.
    start = 1,  --The key was just pressed.
    hold = 2,   --The key is held down.
    stop = 3    --The key was just released.
}
```

---

### sm.world.ids
	
Predefined special world ids.

```lua title="Table Contents"
{
    anyWorld = 65535,
    noWorld = 65534
}
```

---