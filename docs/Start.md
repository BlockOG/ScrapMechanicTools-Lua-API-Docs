---
sidebar_position: 1
title: Introduction
hide_title: true
sidebar-label: 'Introduction'
slug: /
---

### Introduction

Welcome! <br></br>
This is an improved version of the Scrap Mechanic Lua API Reference at https://scrapmechanic.com/api/index.html. <br></br>

In this documentation, you will find details specific to Scrap Mechanic's Lua scripting. <br></br>
For more general information on how the Lua scripting language works, you can review the official Lua documentation. <br></br>

Scrap Mechanic uses Lua version 5.1. Check the official [Manual](https://www.lua.org/manual/5.1/) for more information. <br></br>

The documentation is also available as a [JSON](/files/api_json.zip) and as a [Lua documentation file](/files/api_lua.zip). <br></br>

:::info note
This documentation is for Scrap Mechanic Version <strong>0.6.0 or later</strong>.

The <strong>previous documentation</strong> for Scrap Mechanic Version <strong>0.5.1</strong> can be found [here](https://scrapmechanictools.com/archive/Lua_051/).

If you encounter any errors, malfunctions, broken links, missing or wrong information, please <br></br>
**[report them as soon as possible!](https://scrapmechanictools.com/report_issues.html)**
:::

### Console

It is recommended to start the game with the <code>-dev</code> launch option in steam to get access to the <br></br>
Debug Console and enable the script hot-reload feature. <br></br>
Use [print](/lua/Game-Script-Environment/Static-Functions/Global#print) to print data to the console. <br></br>

### Classes

Classes act as the entry point from the game to the world of Lua. <br></br>
A script class is for example a buildable part with a "scripted" json object:
```json
"scripted": {
	"filename": "$CONTENT_DATA/Scripts/MyShape.lua",
	"classname": "MyShape",
	"data": {
		"hello": "Hello world!"
	}
},
```
<strong>Lua Script:</strong>

```lua
-- MyShape.lua - Interactable part example script

-- Creates a new class
MyShape = class()

-- Sets ShapeClass constants
MyShape.maxParentCount = 1
MyShape.maxChildCount = 0
MyShape.connectionInput = sm.interactable.connectionType.none
MyShape.connectionOutput = sm.interactable.connectionType.logic
MyShape.colorNormal = sm.color.new( 0x777777ff )
MyShape.colorHighlight = sm.color.new( 0x888888ff )

-- Called on creation
function MyShape:server_onCreate()
	print( self.data.hello )
end

-- Called on creation
function MyShape:client_onCreate()
	self.cl = { time = 0 }
end

-- Called every tick
function MyShape:client_onFixedUpdate( timeStep )
	self.cl.time = self.cl.time + timeStep
end

-- Called on interact
function MyShape:client_onInteract( character, state )
	if state then
		print( "Pressed E" )
		self.network:sendToServer( "sv_n_toggle" )
	else
		print( "Released E" )
	end
	print( "Shape has existed for", self.cl.time, "seconds" )
end

function MyShape:sv_n_toggle() 
	-- Toggle on and off
	self.interactable.active = not self.interactable.active
end
```
### Static Functions

Static Functions can be called from Lua to do certain things in the game, <br></br>
such as creating a part using [sm.shape.createPart](/lua/Game-Script-Environment/Static-Functions/sm.shape#createpart). <br></br>

The createPart function will return a userdata object of type Shape which can be used to reference the part. <br></br>
This reference is valid as long as the part still exists in the game. <br></br>

### Userdata

Userdata is a Lua concept to define custom objects. <br></br>
Scrap Mechanic uses userdata to add game objects such as a [Shape](/lua/Game-Script-Environment/Userdata/Shape) and utility objects such as [Vec3](/lua/Game-Script-Environment/Userdata/Vec3). <br></br>
They are similar to [instances](https://en.wikipedia.org/wiki/Instance_(computer_science)) in [object-oriented programming](https://en.wikipedia.org/wiki/Object-oriented_programming). <br></br>
The userdata objects have a set of member values and functions. <br></br>

Here is an example where the member function [getColor](/lua/Game-Script-Environment/Userdata/Shape#getcolor) is called on the [Shape](/lua/Game-Script-Environment/Userdata/Shape) userdata:
```lua
local color = myShape.getColor( myShape ) -- All userdata functions require the object itself as first parameter.
```
Or with <code>:</code> syntactic sugar which adds the userdata itself as the first parameter:
```lua
local color = myShape:getColor()
```

Userdata can also be used as parameters to other functions. <br></br>
The color returned by [getColor](/lua/Game-Script-Environment/Userdata/Shape#getcolor) is another userdata type; [Color](/lua/Game-Script-Environment/Userdata/Color). That color can be used as a parameter to [setColor](/lua/Game-Script-Environment/Userdata/Shape#setcolor):

```lua
local color = myShape:getColor()
myOtherShape:setColor( color ) -- Copy the color from myShape to myOtherShape
```
Userdata can also have member values; which are actually convenience for calling a get or set member function. <br></br>
This does exactly the same thing as the above:
```lua
local color = myShape.color
myOtherShape.color = color -- Copy the color from myShape to myOtherShape
```

Another way to get a [Color](/lua/Game-Script-Environment/Userdata/Color) userdata object is to call [sm.color.new](/lua/Game-Script-Environment/Static-Functions/sm.color#new). <br></br>
Here is an example where the shape color is set to red:
```lua
local color = sm.color.new( 1.0, 0.0, 0.0 )
myShape.color = color -- Set shape to red
```

### Sandboxes
When Lua code is run by the game, they are run in a "sandbox". <br></br>
The sandbox makes sure no functions can be called that the sandbox does not allow in the current context. <br></br>
One reason for the sandbox to exist is to enforce a server/client structure, this is to help make sure the scripts work when playing multiplayer. <br></br>
The sandbox also makes sure no harmful code can be written in Lua by restricting file access and the ability to run executables. <br></br>

### Server
The <strong>server</strong> side simulates the game world and communicates with all clients that are currently playing, including the host itself. <br></br>
The server side is only running on the hosting player's computer. <br></br>

In a script class, <strong>serverCallback</strong> implies that the the code will run in server mode and can only access functions marked as <strong>server</strong> or <strong>server and client</strong>. <br></br>
To check if a script is running in server mode at runtime you can also use [sm.isServerMode](/lua/Game-Script-Environment/Static-Functions/sm#isservermode). <br></br>

### Client
The <strong>client</strong> is the part of Scrap Mechanic that a player sees and interacts with (e.g. graphics, audio, player input, etc.). <br></br>
A client is running on every player's computer, including the host. <br></br>

In a script class, <strong>clientCallback</strong> implies that the the code will run in server mode and can only access functions marked as <strong>client</strong> or <strong>server and client</strong>. <br></br>


