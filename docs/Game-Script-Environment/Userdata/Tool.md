---
sidebar_position: 26
title: Tool
hide_title: true
sidebar-label: 'Tool'
---

<br></br>

## Tool

**Associated namespace:** [sm.tool](/lua/Game-Script-Environment/Static-Functions/sm.tool)

A userdata object representing a <strong>handheld tool</strong> in the game.

<strong>Values:</strong>

- <code>id</code> [<strong> int </strong>] <br></br>

	- <code>Get</code>: The tool's id.


## Functions

### getAnimationInfo

```lua
tool:getAnimationInfo( name )
```
<code>Client-Only</code> <br></br>

Returns general information for a third person view animation.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>name</code> [<strong> string </strong>]: The animation name.

<strong>Returns:</strong> <br></br>

- [<strong> table </strong>]: A table containing information about the animation (see below).

<strong>Table Content:</strong> <br></br>

- <code>name</code> [<strong> string </strong>]: The animation's name.
- <code>duration</code> [<strong> number </strong>]: The animation's duration
- <code>looping</code> [<strong> bool </strong>]: Whether the animation is looping or not.

---

### getCameraWeights

```lua
tool:getCameraWeights()
```
<code>Client-Only</code> <br></br>

Returns the current weights for the tool's local camera settings.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The third-person weight.
- [<strong> number </strong>]: The first-person weight.

---

### getDirection

```lua
tool:getDirection()
```
<code>Client-Only</code> <br></br>

Returns the player's view/aim direction.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> vec3 </strong>]: The aim direction.

---

### getFpAnimationInfo

```lua
tool:getFpAnimationInfo()
```
<code>Client-Only</code> <br></br>

Returns general information for a first person view animation.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>name</code> [<strong> string </strong>]: The animation name.

<strong>Returns:</strong> <br></br>

- [<strong> table </strong>]: A table containing information about the animation (see below).

<strong>Table Content:</strong> <br></br>

- <code>name</code> [<strong> string </strong>]: The animation's name.
- <code>duration</code> [<strong> number </strong>]: The animation's duration
- <code>looping</code> [<strong> bool </strong>]: Whether the animation is looping or not.

---

### getFpBonePos

```lua
tool:getFpBonePos( joint )
```
<code>Client-Only</code> <br></br>

Returns the world position for a bone in the first person view animation skeleton.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>joint</code> [<strong> string </strong>]: The name of the joint.

<strong>Returns:</strong> <br></br>

- [<strong> vec3 </strong>]: The joint position.

---

### getId

```lua
tool:getId()
```

Returns the tool's id.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> int </strong>]: The tool's id.

---

### getMovementSpeedFraction

```lua
tool:getMovementSpeedFraction()
```
<code>Client-Only</code> <br></br>

Returns the fraction of the player's movement speed in proportion to its maximum. <br></br>
This is affected by sprinting, crouching, blocking, aiming, etc.

<code>sprinting</code> = 1.0 <br></br>
<code>blocking</code> = 0.5 <br></br>
<code>crouching</code> = 0.375 <br></br>
<code>aiming</code> = 0.3125 <br></br>

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The movement speed fraction.

---

### getMovementVelocity

```lua
tool:getMovementVelocity()
```
<code>Client-Only</code> <br></br>

Returns the movement velocity of the player.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> vec3 </strong>]: The player's velocity.

---

### getOwner

```lua
tool:getOwner()
```

Returns the player that owns the tool.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> player </strong>]: The tool's owner.

---

### getPosition

```lua
tool:getPosition()
```
<code>Client-Only</code> <br></br>

Returns the world position of the tool's owner.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> vec3 </strong>]: The owner's world position.

---

### getRelativeMoveDirection

```lua
tool:getRelativeMoveDirection()
```
<code>Client-Only</code> <br></br>

Returns the relative movement direction of the player. <br></br>
This is the direction the player wants to move based on movement input.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> vec3 </strong>]: The player's relative movement direction.

---

### getSmoothDirection

```lua
tool:getSmoothDirection()
```
<code>Client-Only</code> <br></br>

Provides a smoother way of getting the direction of the player <br></br>
holding the tool while playing in multiplayer.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> Vec3 </strong>]: The player's direction.

---

### getTpBoneDir

```lua
tool:getTpBoneDir( bone )
```
<code>Client-Only</code> <br></br>

Returns the world direction for a bone in the third person view animation skeleton.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>bone</code> [<strong> string </strong>]: The bone name.

<strong>Returns:</strong> <br></br>

- [<strong> vec3 </strong>]: The bone direction.

---

### getTpBonePos

```lua
tool:getTpBonePos( bone )
```
<code>Client-Only</code> <br></br>

Returns the world position for a bone in the third person view animation skeleton.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>bone</code> [<strong> string </strong>]: The bone name.

<strong>Returns:</strong> <br></br>

- [<strong> vec3 </strong>]: The bone position.

---

### isCrouching

```lua
tool:isCrouching()
```
<code>Client-Only</code> <br></br>

Returns whether the tool's owner is currently crouching.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the owner is crouching or not.

---

### isEquipped

```lua
tool:isEquipped()
```
<code>Client-Only</code> <br></br>

Returns whether the tool is equipped.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the tool is equipped or not.

---

### isInFirstPersonView

```lua
tool:isInFirstPersonView()
```
<code>Client-Only</code> <br></br>

Returns whether the player is in first person view where the viewpoint is rendered from the player's perspective. <br></br>
Otherwise, the player is in third person view where the camera is behind the player.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the tool in first person view or not.

---

### isLocal

```lua
tool:isLocal()
```
<code>Client-Only</code> <br></br>

Returns whether the player holding the tool is the same as the [Local Player](/lua/Game-Script-Environment/Static-Functions/sm.localPlayer)

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether tool is local or not.

---

### isOnGround

```lua
tool:isOnGround()
```
<code>Client-Only</code> <br></br>

Returns whether the tool's owner is currently standing on the ground.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the owner is on the ground or not.

---

### isSprinting

```lua
tool:isSprinting()
```
<code>Client-Only</code> <br></br>

Returns whether the tool's owner is currently sprinting.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the owner is sprinting or not.

---

### setBlockSprint

```lua
tool:setBlockSprint( state )
```
<code>Client-Only</code> <br></br>

Sets whether the player is unable to sprint. <br></br>
Sprinting is normally blocked when the player is attacking, blocking, aiming, etc.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>state</code> [<strong> bool </strong>]: Whether sprinting is blocked or not.

---

### setCrossHairAlpha

```lua
tool:setCrossHairAlpha( alpha )
```
<code>Client-Only</code> <br></br>

Sets the opacity of the crosshair. <br></br>
An alpha value of 0 makes the crosshair transparent.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>alpha</code> [<strong> number </strong>]: The alpha value.

---

### setDispersionFraction

```lua
tool:setDispersionFraction( fraction )
```
<code>Client-Only</code> <br></br>

Sets the tool's dispersion fraction. <br></br>
This represents the accuracy of the tool, and affects the size of the player's crosshair.

A dispersion value of 0 is perfect accuracy, whereas 1 is the worst.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>fraction</code> [<strong> number </strong>]: The dispersion fraction.

---

### setFpColor

```lua
tool:setFpColor( color )
```
<code>Client-Only</code> <br></br>

Sets the tool's color in first person view.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>color</code> [<strong> color </strong>]: The color.

---

### setFpRenderables

```lua
tool:setFpRenderables( renderables )
```
<code>Client-Only</code> <br></br>

Sets the renderables (files containing model data) to be used for the character in first person view.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>renderables</code> [<strong> table </strong>]: The table containing the renderable filepaths.

---

### setInteractionTextSuppressed

```lua
tool:setInteractionTextSuppressed( state )
```
<code>Client-Only</code> <br></br>

Sets whether interaction texts are suppressed for the player. <br></br>
This means the player won't be able to see <code>Press E to use</code> and similar texts when looking at an interactable.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>state</code> [<strong> bool </strong>]: Whether the text is suppressed or not.

---

### setMovementAnimation

```lua
tool:setMovementAnimation( name, animation )
```
<code>Client-Only</code> <br></br>

Sets the current third person view movement animation to be used by the tool.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>name</code> [<strong> string </strong>]: The name.
- <code>animation</code> [<strong> string </strong>]: The animation.

---

### setMovementSlowDown

```lua
tool:setMovementSlowDown( slowdown )
```
<code>Client-Only</code> <br></br>

Sets whether the player is slowed down. <br></br>
This is similar to crouching and normally occurs when the player is aiming.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>slowdown</code> [<strong> bool </strong>]: Whether the player is slowed down or not.

---

### setTpColor

```lua
tool:setTpColor( color )
```
<code>Client-Only</code> <br></br>

Sets the tool's color in third person view.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>color</code> [<strong> color </strong>]: The color.

---

### setTpRenderables

```lua
tool:setTpRenderables( renderables )
```
<code>Client-Only</code> <br></br>

Sets the renderables (files containing model data) to be used for the character in third person view.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>renderables</code> [<strong> table </strong>]: The table containing the renderable filepaths.

---

### updateAnimation

```lua
tool:updateAnimation( name, time, weight )
```
<code>Client-Only</code> <br></br>

Updates a third person view animation.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>name</code> [<strong> string </strong>]: The animation name.
- <code>time</code> [<strong> number </strong>]: The time.
- <code>weight</code> [<strong> number </strong>]: The weight.

---

### updateCamera

```lua
tool:updateCamera( distance, fov, offset, weight )
```
<code>Client-Only</code> <br></br>

Updates the third person view camera for the tool.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>distance</code> [<strong> number </strong>]: The distance.
- <code>fov</code> [<strong> number </strong>]: The FOV.
- <code>offset</code> [<strong> vec3 </strong>]: The offset position.
- <code>weight</code> [<strong> number </strong>]: The weight.

---

### updateFpAnimation

```lua
tool:updateFpAnimation( name, time, weight=-1.0, looping )
```
<code>Client-Only</code> <br></br>

Updates a first person view animation.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>name</code> [<strong> string </strong>]: The animation name.
- <code>time</code> [<strong> number </strong>]: The time.
- <code>weight</code> [<strong> number </strong>]: The weight.
- <code>looping</code> [<strong> looping </strong>]: Whether the animation is looping or not.

---

### updateFpCamera

```lua
tool:updateFpCamera( fov, offset, weight, bobbing )
```
<code>Client-Only</code> <br></br>

Updates the first person view camera for the tool.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>fov</code> [<strong> number </strong>]: The FOV.
- <code>offset</code> [<strong> vec3 </strong>]: The offset position.
- <code>weight</code> [<strong> number </strong>]: The weight.
- <code>bobbing</code> [<strong> number </strong>]: The bobbing.

---

### updateJoint

```lua
tool:updateJoint( name, rotation, weight )
```
<code>Client-Only</code> <br></br>

Sets the rotation and weight for a bone in the animation skeleton.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>name</code> [<strong> string </strong>]: The name.
- <code>rotation</code> [<strong> vec3 </strong>]: The rotation.
- <code>weight</code> [<strong> number </strong>]: The weight.

---

### updateMovementAnimation

```lua
tool:updateMovementAnimation( time, weight )
```
<code>Client-Only</code> <br></br>

Updates the currently set third person view movement animation for the tool.

<strong>Arguments:</strong> <br></br>

- <code>tool</code> [<strong> tool </strong>]: The tool.
- <code>time</code> [<strong> number </strong>]: The time.
- <code>weight</code> [<strong> number </strong>]: The weight.

---

