---
sidebar_position: 13
title: Interactable
hide_title: true
sidebar-label: 'Interactable'
---

<br></br>

## Interactable

**Associated namespace:** [sm.interactable](/lua/Game-Script-Environment/Static-Functions/sm.interactable)

A userdata object representing an <strong>interactable shape</strong> in the game.

<strong>Values:</strong>

- <code>active</code> [<strong> bool </strong>] <br></br>

	- <code>Get</code>: The interactable's logic output signal.
	- <code>Set</code>: (Server-Only) Sets the interactable's logic output signal.


- <code>body</code> [<strong> body </strong>] <br></br>

	- <code>Get</code>: The interactable shape's body.


- <code>id</code> [<strong> int </strong>] <br></br>

	- <code>Get</code>: The interactable's id.


- <code>power</code> [<strong> number </strong>] <br></br>

	- <code>Get</code>: The interactable's power output signal.
	- <code>Set</code>: (Server-Only) Sets the interactable's power output signal.


- <code>publicData</code> [<strong> table </strong>] <br></br>

	- <code>Get</code>: (Server-only) The interactable's server public data.
	- <code>Set</code>: (Server-Only) Sets the interactable's server public data.


- <code>shape</code> [<strong> shape </strong>] <br></br>

	- <code>Get</code>: The interactable's shape.


- <code>type</code> [<strong> string </strong>] <br></br>

	- <code>Get</code>: The interactable's type.

	
<strong>Operations:</strong>

| Operation   | Description |
| ----------- | ----------- |
| <code>Interactable</code> == <code>Interactable</code> | Checks if two instances of <code>Interactable</code> refer to the same <code>Interactable</code>. |

## Functions

### addContainer

```lua
interactable:addContainer( index, size, stackSize )
```
<code>Server-Only</code> <br></br>

Creates and stores a container in the given index inside the controller.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>index</code> [<strong> int </strong>]: The index of the container (0 - 15).
- <code>size</code> [<strong> int </strong>]: The number of slots in the container.
- <code>stackSize</code> [<strong> int </strong>]: The stack size. Defaults to max stack size (65535).

<strong>Returns:</strong> <br></br>

- [<strong> container </strong>]: The created container.

---

### connect

```lua
interactable:connect( child )
```
<code>Server-Only</code> <br></br>

Connects the interactable to another compatible interactable. Similar to using the Connect Tool.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>child</code> [<strong> interactable </strong>]: The child (receiving) interactable.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the connection was successful or not.

---

### connectToJoint

```lua
interactable:connectToJoint( child )
```
<code>Server-Only</code> <br></br>

Connects the interactable to a compatible joint.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>child</code> [<strong> joint </strong>]: The child (receiving) joint.

---

### disconnect

```lua
interactable:disconnect( child )
```
<code>Server-Only</code> <br></br>

Disconnects the interactable from another interactable. Similar to using the Connect Tool.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>child</code> [<strong> interactable </strong>]: The child interactable.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the disconnection was successful or not.

---

### getAnimDuration

```lua
interactable:getAnimDuration( name )
```
<code>Client-Only</code> <br></br>

Returns animation duration in seconds.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>name</code> [<strong> string </strong>]: The name of the animation.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The animation duration.

---

### getBearings

```lua
interactable:getBearings()
```

Returns a table of [bearings](/lua/Game-Script-Environment/Userdata/Joint) that the interactable is connected to.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> table </strong>]: The table of connected bearings.

---

### getBody

```lua
interactable:getBody()
```

Returns the [body](/lua/Game-Script-Environment/Userdata/Body) of the interactable's [shape](/lua/Game-Script-Environment/Userdata/Shape).

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> body </strong>]: The body.

---

### getChildren

```lua
interactable:getChildren( connectionType )
```

Returns a table of child interactables that the interactable is connected to. <br></br>
The children listen to the interactable's output.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>connectionType</code> [<strong> int </strong>]: Connection type filter. Defaults to all types except <code>bearing</code> (for backwards compatibility). 

<strong>Returns:</strong> <br></br>

- [<strong> table </strong>]: The table of connected child interactables.

---

### getColorHighlight

```lua
interactable:getColorHighlight()
```

Returns the connection-point highlight color of the interactable. <br></br>
This point color is shown when aiming at the shape with the Connect Tool.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> color </strong>]: The highlight color.

---

### getColorNormal

```lua
interactable:getColorNormal()
```

Returns the connection-point color of the interactable. <br></br>
This point color is shown when the Connect Tool is equipped.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> color </strong>]: The color.

---

### getConnectionInputType

```lua
interactable:getConnectionInputType()
```

Returns the interactable's input connection type.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> int </strong>]: The connection type.

---

### getConnectionOutputType

```lua
interactable:getConnectionOutputType()
```

Returns the interactable's output connection type.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> int </strong>]: The connection type.

---

### getContainer

```lua
interactable:getContainer( index )
```

Returns the container stored at the given index inside the controller.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>index</code> [<strong> int </strong>]: The index (default 0).

<strong>Returns:</strong> <br></br>

- [<strong> container </strong>]: The container.

---

### getGlowMultiplier

```lua
interactable:getGlowMultiplier()
```
<code>Client-Only</code> <br></br>

Returns the interactable's glow multiplier.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The glow multiplier (0.0 - 1.0).

---

### getId

```lua
interactable:getId()
```

Returns the interactable's id.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> int </strong>]: The id.

---

### getJoints

```lua
interactable:getJoints()
```

Returns a table of all [joints](/lua/Game-Script-Environment/Userdata/Joint) that an interactable is connected to. <br></br>
Joints include <strong>bearings</strong> and <strong>pistons</strong>.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> table </strong>]: The table of connected joints.

---

### getLocalBonePosition

```lua
interactable:getLocalBonePosition( name )
```

Returns the local position of a bone.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>name</code> [<strong> string </strong>]: The bone name.

<strong>Returns:</strong> <br></br>

- [<strong> vec3 </strong>]: The position.

---

### getMaxChildCount

```lua
interactable:getMaxChildCount()
```

Returns the maximum number of allowed child connections of the interactable - the number of outgoing connections.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> int </strong>]: The max child connection count.

---

### getMaxParentCount

```lua
interactable:getMaxParentCount()
```

Returns the maximum number of allowed parent connections of the interactable - the number of incoming connections.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> int </strong>]: The max parent connection count.

---

### getParents

```lua
interactable:getParents( connectionType )
```

Returns a table of parent interactables that are connected to the interactable. <br></br>
The parents act as the interactable's input.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>connectionType</code> [<strong> int </strong>]: Connection type filter. Defaults to all types.

<strong>Returns:</strong> <br></br>

- [<strong> table </strong>]: The table of connected parent interactables.

---

### getPistons

```lua
interactable:getPistons()
```

Returns a table of [pistons](/lua/Game-Script-Environment/Userdata/Joint) that the interactable is connected to.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> table </strong>]: The table of connected pistons.

---

### getPoseWeight

```lua
interactable:getPoseWeight( index )
```
<code>Client-Only</code> <br></br>

Returns the pose weight of the pose in the given index.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>index</code> [<strong> int </strong>]: The index.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The pose weight.

---

### getPower

```lua
interactable:getPower()
```

Returns the power output signal of the interactable. <br></br>
This signal is usually a number between -1 to 1, where 1 is forward and -1 backward. <br></br>
However, it can also be used for other numbers.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The power output signal.

---

### getPublicData

```lua
interactable:getPublicData()
```
<code>Server-Only</code> <br></br>

Returns the interactable's server public data.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> table </strong>]: The public data.

---

### getSeatCharacter

```lua
interactable:getSeatCharacter()
```

Returns the [Character](/lua/Game-Script-Environment/Userdata/Character) that is currently seated in the interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> character </strong>]: The seated character.

---

### getSeatInteractables

```lua
interactable:getSeatInteractables()
```

Returns a table of interactables that are connected to the seat.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> table </strong>]: The table of seat interactables.

---

### getShape

```lua
interactable:getShape()
```

Returns the interactable's [Shape](/lua/Game-Script-Environment/Userdata/Shape).

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> shape </strong>]: The interactable's host shape.

---

### getSingleParent

```lua
interactable:getSingleParent()
```

Returns the interactable's parent interactable. <br></br>
The parent act as the interactable's input.

:::caution warning
This method is <strong>not</strong> allowed for an interactable that allows more than one parent connection.
:::

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> interactable </strong>]: The parent interactable.

---

### getSteeringAngle

```lua
interactable:getSteeringAngle()
```

Returns the steering angle of the steering interactable.

The value ranges from -1 to +1, where -1 represents steering right <br></br>
and +1 represents steering left.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The steering angle.

---

### getSteeringJointLeftAngleLimit

```lua
interactable:getSteeringJointLeftAngleLimit( joint )
```

Returns the left angle limit of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The left angle limit.

---

### getSteeringJointLeftAngleSpeed

```lua
interactable:getSteeringJointLeftAngleSpeed( joint )
```

Returns the left angle speed of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The left angle speed.

---

### getSteeringJointRightAngleLimit

```lua
interactable:getSteeringJointRightAngleLimit( joint )
```

Returns the right angle limit of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The right angle limit.

---

### getSteeringJointRightAngleSpeed

```lua
interactable:getSteeringJointRightAngleSpeed( joint )
```

Returns the right angle speed of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The right angle speed.

---

### getSteeringJointSettings

```lua
interactable:getSteeringJointSettings( joint )
```

Returns the settings of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The left angle speed.
- [<strong> number </strong>]: The right angle speed.
- [<strong> number </strong>]: The left angle limit.
- [<strong> number </strong>]: The right angle limit.
- [<strong> bool </strong>]: Whether the joint is unlocked or not.

---

### getSteeringJointUnlocked

```lua
interactable:getSteeringJointUnlocked( joint )
```

Returns the lock state of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the joint is unlocked or not.

---

### getSteeringPower

```lua
interactable:getSteeringPower()
```

Returns the steering power of the steering interactable.

The value ranges from -1 to +1, where +1 represents pressing "forward" <br></br>
and -1 represents pressing "backwards".

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> number </strong>]: The steering power.

---

### getType

```lua
interactable:getType()
```

Returns the interactable's type.

See [sm.interactable.types](/lua/Game-Script-Environment/Constants) for details.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> string </strong>]: The type.

---

### getUvFrameIndex

```lua
interactable:getUvFrameIndex()
```
<code>Client-Only</code> <br></br>

Returns the index of the current UV animation frame.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> int </strong>]: The UV frame.

---

### getWorldBonePosition

```lua
interactable:getWorldBonePosition( name )
```

Returns the world position of a bone.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>name</code> [<strong> string </strong>]: The bone name.

<strong>Returns:</strong> <br></br>

- [<strong> vec3 </strong>]: The world position.

---

### hasAnim

```lua
interactable:hasAnim( name )
```
<code>Client-Only</code> <br></br>

Returns whether an animation exists.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>name</code> [<strong> string </strong>]: The animation name.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the animation exists or not.

---

### hasOutputType

```lua
interactable:hasOutputType( type )
```

Returns whether the interactable has the specified output connection type.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>type</code> [<strong> int </strong>]: The connection type.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the interactable has the connection type or not.

---

### hasSeat

```lua
interactable:hasSeat()
```

Returns whether the interactable has a seat component.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the interactable has a seat component or not.

---

### hasSteering

```lua
interactable:hasSteering()
```

Returns whether the interactable has a steering component.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the interactable has a steering component or not.

---


### isActive

```lua
interactable:isActive()
```

Returns the interactable's logic output signal. <br></br>
This signal is a boolean, <strong>on</strong> or <strong>off</strong>.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: The logic output signal.

---

### pressSeatInteractable

```lua
interactable:pressSeatInteractable( index )
```

Triggers a <strong>press</strong> interaction on an interactable connected to the seat.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>index</code> [<strong> int </strong>]: The index of the interactable.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the action was successful or not.

---

### releaseSeatInteractable

```lua
interactable:releaseSeatInteractable( index )
```

Triggers a <strong>release</strong> interaction on an interactable connected to the seat.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>index</code> [<strong> int </strong>]: The index of the interactable.

<strong>Returns:</strong> <br></br>

- [<strong> bool </strong>]: Whether the action was successful or not.

---

### removeContainer

```lua
interactable:removeContainer( index )
```
<code>Server-Only</code> <br></br>

Removes the container stored in the given index inside the controller.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>index</code> [<strong> int </strong>]: The index of the container.

---

### setActive

```lua
interactable:setActive( signal )
```
<code>Server-Only</code> <br></br>

Sets the logic output signal of an interactable. <br></br>
This signal is a boolean, <strong>on</strong> or <strong>off</strong>.

:::caution warning
Every time an interactable's logic output signal ("active state") changes, <br></br>
this change is transmitted over the network to every connected client.

This means, if a large amount of interactables update their states too often, this can have <br></br>
a significant impact on multiplayer performance, to the point of becoming almost unplayable.

To avoid causing such problems, change the interactable's "active state" only <br></br>
if neccessary (and make sure to <strong>not</strong> set it every tick, if possible).
:::

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>signal</code> [<strong> bool </strong>]: The logic output signal.

---

### setAnimEnabled

```lua
interactable:setAnimEnabled( name, enabled )
```
<code>Client-Only</code> <br></br>

Sets whether the animation with the given name should be applied to the mesh. <br></br>
True enables the animation and false disables it.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>name</code> [<strong> string </strong>]: The animation name.
- <code>enabled</code> [<strong> bool </strong>]: Whether the animation is enabled or not.

---

### setAnimProgress

```lua
interactable:setAnimProgress( name, progress )
```
<code>Client-Only</code> <br></br>

Sets the progress on the animation with the given name.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>name</code> [<strong> string </strong>]: The animation name.
- <code>progress</code> [<strong> number </strong>]: The progress (between 0 and 1).

---

### setGlowMultiplier

```lua
interactable:setGlowMultiplier( value )
```
<code>Client-Only</code> <br></br>

Sets a value to multiply the glow from asg texture with.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>value</code> [<strong> number </strong>]: The glow multiplier.

---

### setGyroDirection

```lua
interactable:setGyroDirection( direction )
```
<code>Client-Only</code> <br></br>

Sets the direction of the gyro.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>direction</code> [<strong> vec3 </strong>]: The gyro direction.

---

### setParams

```lua
interactable:setParams( data )
```

Sets the interactable's script param data.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>data</code> [<strong> any </strong>]: The param data.

---

### setPoseWeight

```lua
interactable:setPoseWeight( index, value )
```
<code>Client-Only</code> <br></br>

Set the pose weight of the pose in the given index.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>index</code> [<strong> int </strong>]: The index.
- <code>value</code> [<strong> number </strong>]: The pose weight.

---

### setPower

```lua
interactable:setPower( signal )
```
<code>Server-Only</code> <br></br>

Returns the power output signal of the interactable. <br></br>
This signal is usually a number between -1 to 1, where 1 is forward and -1 backward. <br></br>
However, it can also be used for other numbers.

:::caution warning
Every time an interactable's power output signal ("power") changes, <br></br>
this change is transmitted over the network to every connected client.

This means, if a large amount of interactables update their "power" too often, this can have <br></br>
a significant impact on multiplayer performance, to the point of becoming almost unplayable.

To avoid causing such problems, change the interactable's "power" only <br></br>
if neccessary (and make sure to <strong>not</strong> set it every tick, if possible).
:::

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>signal</code> [<strong> number </strong>]: The power output signal.

---

### setPublicData

```lua
interactable:setPublicData( data )
```
<code>Server-Only</code> <br></br>

Set the interactable's server public data.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>data</code> [<strong> table </strong>]: The data to set.

---

### setSeatCharacter

```lua
interactable:setSeatCharacter( character )
```

Requests to seat a [Character](/lua/Game-Script-Environment/Userdata/Character) in the Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>character</code> [<strong> character </strong>]: The character.

---

### setSteeringFlag

```lua
interactable:setSteeringFlag( flag )
```

Sets the steering flag for the steering interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>flag</code> [<strong> int </strong>]: The steering flag.

---

### setSteeringJointLeftAngleLimit

```lua
interactable:setSteeringJointLeftAngleLimit( joint, value )
```
<code>Client-Only</code> <br></br>

Sets the left angle limit settings of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.
- <code>value</code> [<strong> number </strong>]: The left angle limit.

---

### setSteeringJointLeftAngleSpeed

```lua
interactable:setSteeringJointLeftAngleSpeed( joint, value )
```
<code>Client-Only</code> <br></br>

Sets the left angle speed settings of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.
- <code>value</code> [<strong> number </strong>]: The left angle speed.

---

### setSteeringJointRightAngleLimit

```lua
interactable:setSteeringJointRightAngleLimit( joint, value )
```
<code>Client-Only</code> <br></br>

Sets the right angle limit settings of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.
- <code>value</code> [<strong> number </strong>]: The right angle limit.

---

### setSteeringJointRightAngleSpeed

```lua
interactable:setSteeringJointRightAngleSpeed( joint, value )
```
<code>Client-Only</code> <br></br>

Sets the right angle speed settings of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.
- <code>value</code> [<strong> number </strong>]: The right angle speed.

---

### setSteeringJointSettings

```lua
interactable:setSteeringJointSettings( joint, leftSpeed, rightSpeed, leftLimit, rightLimit, unlocked )
```
<code>Client-Only</code> <br></br>

Sets the right angle speed settings of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.
- <code>leftSpeed</code> [<strong> number </strong>]: The left angle speed.
- <code>rightSpeed</code> [<strong> number </strong>]: The right angle speed.
- <code>leftLimit</code> [<strong> number </strong>]: The left angle limit.
- <code>rightLimit</code> [<strong> number </strong>]: The right angle limit.
- <code>unlocked</code> [<strong> bool </strong>]: Whether the joint is unlocked or not.

---

### setSteeringJointUnlocked

```lua
interactable:setSteeringJointUnlocked( joint, value )
```
<code>Client-Only</code> <br></br>

Sets the lock state of a [Joint](/lua/Game-Script-Environment/Userdata/Joint) connected to the steering Interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>joint</code> [<strong> joint </strong>]: The joint.
- <code>value</code> [<strong> bool </strong>]: Whether the joint is unlocked or not.

---

### setSubMeshVisible

```lua
interactable:setSubMeshVisible( name, visible )
```
<code>Client-Only</code> <br></br>

Sets the visibility of a submesh.

:::info note
The maximum amount of submeshes for an interactable is **32**.
:::

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>name</code> [<strong> string </strong>]: The submesh name.
- <code>visible</code> [<strong> bool </strong>]: Whether the submesh is visible or not.

---

### setUvFrameIndex

```lua
interactable:setUvFrameIndex( index )
```
<code>Client-Only</code> <br></br>

Sets the UV animation frame with the given index.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>index</code> [<strong> int </strong>]: The index.

---

### unsetSteeringFlag

```lua
interactable:unsetSteeringFlag( flag )
```

Unsets the steering flag for a steering interactable.

<strong>Arguments:</strong> <br></br>

- <code>interactable</code> [<strong> interactable </strong>]: The interactable.
- <code>flag</code> [<strong> int </strong>]: The steering flag.

---