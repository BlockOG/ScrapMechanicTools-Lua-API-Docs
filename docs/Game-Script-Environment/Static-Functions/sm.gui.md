---
sidebar_position: 22
title: sm.gui
hide_title: true
sidebar-label: 'sm.gui'
---

<br></br>

## sm.gui

The <strong>gui</strong> library contains various utility functions for handling user interfaces. <br></br>
This library can only be used on the [client](/lua/#client).

## Functions

### chatMessage

```lua
sm.gui.chatMessage( message )
```

Sends a message in chat.

:::info note
The message is not sent to other players.
:::

<strong>Arguments:</strong> <br></br>

- <code>message</code> [<strong> string </strong>]: The message.

---

### createAmmunitionContainerGui

```lua
sm.gui.createAmmunitionContainerGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates an ammunition container GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createBagIconGui

```lua
sm.gui.createBagIconGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a bag icon GUI.

:::caution warning
This function is deprecated. Do not use!

Use [createWorldIconGui](#createworldicongui) instead.
:::

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createBatteryContainerGui

```lua
sm.gui.createBatteryContainerGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a battery container GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createBeaconIconGui

```lua
sm.gui.createBeaconIconGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a beacon icon GUI.

:::caution warning
This function is deprecated. Do not use!

Use [createWorldIconGui](#createworldicongui) instead.
:::

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createChallengeHUDGui

```lua
sm.gui.createChallengeHUDGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a challenge HUD GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createChallengeMessageGui

```lua
sm.gui.createChallengeMessageGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a challenge message GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createCharacterCustomizationGui

```lua
sm.gui.createCharacterCustomizationGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a character customization GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createChemicalContainerGui

```lua
sm.gui.createChemicalContainerGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a chemical container GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createContainerGui

```lua
sm.gui.createContainerGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a container GUI, for showing two containers.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createCraftBotGui

```lua
sm.gui.createCraftBotGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a craftbot GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createDressBotGui

```lua
sm.gui.createDressBotGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a dressbot GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createEngineGui

```lua
sm.gui.createEngineGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates an engine GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createFertilizerContainerGui

```lua
sm.gui.createFertilizerContainerGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a fertilizer container GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createGasContainerGui

```lua
sm.gui.createGasContainerGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a gas container GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createGuiFromLayout

```lua
sm.gui.createGuiFromLayout( layout, destroyOnClose, settings )
```
<code>Client-Only</code> <br></br>

Creates a custom GUI from a layout file.

<strong>Arguments:</strong> <br></br>

- <code>layout</code> [<strong> string </strong>]: The file path to the gui layout file.
- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.
- <code>settings</code> [<strong> table </strong>]: Table with GUI settings, see table structure below.

```lua title="'settings' Table Structure"
{
	isHud = false,			--Whether the GUI is a HUD GUI or not.
	isInteractive = false,	--?
	needsCursor = false,	--?
	hidesHotbar = false,	--?
	isOverlapped = false,	--?
	backgroundAlpha = 1.0,	--?
}
```

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createHideoutGui

```lua
sm.gui.createHideoutGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a hideout GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createLogbookGui

```lua
sm.gui.createLogbookGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a logbook GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createMechanicStationGui

```lua
sm.gui.createMechanicStationGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a mechanic station GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createNameTagGui

```lua
sm.gui.createNameTagGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a name tag GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createQuestTrackerGui

```lua
sm.gui.createQuestTrackerGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a quest tracker GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createSeatGui

```lua
sm.gui.createSeatGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a seat GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createSeatUpgradeGui

```lua
sm.gui.createSeatUpgradeGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a seat upgrade GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createSeedContainerGui

```lua
sm.gui.createSeedContainerGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a seed container GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createSteeringBearingGui

```lua
sm.gui.createSteeringBearingGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a steering bearing GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createSurvivalHudGui

```lua
sm.gui.createSurvivalHudGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a survival HUD GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createWaterContainerGui

```lua
sm.gui.createWaterContainerGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a water container GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createWaypointIconGui

```lua
sm.gui.createWaypointIconGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a waypoint icon GUI.

:::caution warning
This function is deprecated. Do not use!

Use [createWorldIconGui](#createworldicongui) instead.
:::

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createWidget

```lua
sm.gui.createWidget()
```

:::caution warning
This function is removed and does nothing. Do not use!

Use [createGuiFromLayout](#createGuiFromLayout) instead.
:::

---

### createWorkbenchGui

```lua
sm.gui.createWorkbenchGui( destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a workbench GUI.

<strong>Arguments:</strong> <br></br>

- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### createWorldIconGui

```lua
sm.gui.createWorldIconGui( width, height, layout, destroyOnClose )
```
<code>Client-Only</code> <br></br>

Creates a world icon GUI from a layout file.

<strong>Arguments:</strong> <br></br>

- <code>width</code> [<strong> int </strong>]: The width.
- <code>height</code> [<strong> int </strong>]: The height.
- <code>layout</code> [<strong> string </strong>]: The path to the layout file. Defaults to <code>$GAME_DATA/Gui/Layouts/Hud/Hud_WorldIcon.layout</code>.
- <code>destroyOnClose</code> [<strong> bool </strong>]: Whether the guiInterface is destroyed when closed or not. Defaults to false.

<strong>Returns:</strong> <br></br>

- [<strong> guiInterface </strong>]: The created guiInterface.

---

### displayAlertText

```lua
sm.gui.displayAlertText( text, time )
```
<code>Client-Only</code> <br></br>

Displays an alert message at the top of the screen for a set duration.

<strong>Arguments:</strong> <br></br>

- <code>text</code> [<strong> string </strong>]: The alert text.
- <code>time</code> [<strong> number </strong>]: The time in seconds for which the message is shown. Defaults to 4 seconds.

---

### endFadeToBlack

```lua
sm.gui.endFadeToBlack( duration )
```
<code>Client-Only</code> <br></br>

Fades the screen back from a fade to black.

<strong>Arguments:</strong> <br></br>

- <code>duration</code> [<strong> number </strong>]: The animation duration.

---

### exitToMenu

```lua
sm.gui.exitToMenu()
```
<code>Client-Only</code> <br></br>

Exits the current game and returns to the main menu.

:::info note
Can only be used in the Challenge game mode.
:::

---

### getCurrentLanguage

```lua
sm.gui.getCurrentLanguage()
```
<code>Client-Only</code> <br></br>

Returns the user's current language setting.

<strong>Returns:</strong> <br></br>

- [<strong> string </strong>]: The language setting, e.g. "English".

---

### getKeyBinding

```lua
sm.gui.getKeyBinding( action, hypertext )
```
<code>Client-Only</code> <br></br>

Returns the set binding for an action as a string. <br></br>
If <code>hypertext</code> is enabled, the function returns a formatted string <br></br>
that, if given to [setInteractionText](#setinteractiontext), will put the text in a highlight box <br></br>
or display a certain image, depending on the action.

<strong>Arguments:</strong> <br></br>

- <code>action</code> [<strong> string </strong>]: The action.
- <code>hypertext</code> [<strong> bool </strong>]: Whether the string should be hypertext formatted or not.

<strong>Returns:</strong> <br></br>

- [<strong> string </strong>]: The key bound to the action.

---

### translateLocalizationTags

```lua
sm.gui.translateLocalizationTags( text )
```
<code>Client-Only</code> <br></br>

Translates all localization tags in a text using the current language.

<strong>Arguments:</strong> <br></br>

- <code>text</code> [<strong> string </strong>]: The text containing the tags.

<strong>Returns:</strong> <br></br>

- [<strong> string </strong>]: The translated text.

---

### getScreenSize

```lua
sm.gui.getScreenSize()
```
<code>Client-Only</code> <br></br>

Returns the size of the screen.

<strong>Returns:</strong> <br></br>

- [<strong> int </strong>]: The screen width.
- [<strong> int </strong>]: The screen height.

---

### hideGui

```lua
sm.gui.hideGui( state )
```
<code>Client-Only</code> <br></br>

Sets GUI visibility.

<strong>Arguments:</strong> <br></br>

- <code>state</code> [<strong> bool </strong>]: Whether the GUI is hidden or not.

---

### setCenterIcon

```lua
sm.gui.setCenterIcon( name )
```
<code>Client-Only</code> <br></br>

Set the icon displayed at the center.

<strong>Arguments:</strong> <br></br>

- <code>name</code> [<strong> string </strong>]: The icon name.

---

### setCharacterDebugText

```lua
sm.gui.setCharacterDebugText( character, text, clear )
```
<code>Client-Only</code> <br></br>

Set a text for the character that will be displayed above its head.

<strong>Arguments:</strong> <br></br>

- <code>character</code> [<strong> character </strong>]: The character.
- <code>text</code> [<strong> string </strong>]: The text to display.
- <code>clear</code> [<strong> bool </strong>]: Whether the previous text should be overwritten or not.

---

### setInteractionText

```lua
sm.gui.setInteractionText( text1, binding1, text2, binding2, text3 )
```
<code>Client-Only</code> <br></br>

Set the binding text displayed at the center. <br></br>

Using hypertext formatting (see [getKeyBinding](#getkeybinding)), you can highlight the text in a box or display an image. <br></br>
This hypertext can be customized to some extent, see the examples below.

:::info note
You can display **two lines** of text by calling this function twice. <br></br>
When doing so, you need to set a **different** text in each call! <br></br>
If the text in both calls is the same, only one line will be displayed.
:::

<strong>Arguments:</strong> <br></br>

- <code>text1</code> [<strong> string </strong>]: The leftmost segment.
- <code>binding1</code> [<strong> string </strong>]: The left white segment. Optional.
- <code>text2</code> [<strong> string </strong>]: The mid or end segment. Optional.
- <code>binding2</code> [<strong> string </strong>]: The right white segment. Optional.
- <code>text3</code> [<strong> string </strong>]: The rightmost segment. Optional.

```lua title="Example hypertext highlighting"
MyShape = class()

function MyShape.client_onUpdate( self, dt )
	--This string will display the letter 'E' inside an orange highlight box
	local string = "<p textShadow='false' bg='gui_keybinds_bg_orange' color='#66440C' spacing='9'>E</p>"
	--[[
		Parameters:
		'textShadow' - Whether the text should have a shadow applied or not.
		'bg' - The highlight box to be used. Valid are: 'gui_keybinds_bg', 'gui_keybinds_bg_orange' and 'gui_keybinds_bg_white'.
		'color' - The color of the text inside the highlight box.
		'spacing' - The space between the ends of the text and the ends of the highlight box.
		'E' - The text to display inside the box.
	]]
	sm.gui.setInteractionText( string )
end
```
```lua title="Example hypertext image"
MyShape = class()

function MyShape.client_onUpdate( self, dt )
	--This string will display an arrow pointing down.
	local string = "<img bg='gui_keybinds_bg' spacing='0'>icon_keybinds_arrow_down.png</img>"
	--[[
		Parameters:
		'bg' - The background box to be used. Valid are: 'gui_keybinds_bg', 'gui_keybinds_bg_orange' and 'gui_keybinds_bg_white'.
		'spacing' - The space between the edges of the image and the edges of the background box.
		'icon_keybinds_arrow_down.png' - The image to display. A custom image can be set using '$CONTENT_DATA/path/to/image.png'
	]]
	sm.gui.setInteractionText( string )
end
```

---

### setProgressFraction

```lua
sm.gui.setProgressFraction( progress )
```
<code>Client-Only</code> <br></br>

Set the progress fraction filling the circle icon displayed at the center.

<strong>Arguments:</strong> <br></br>

- <code>progress</code> [<strong> number </strong>]: The number that determines how much of the circle is filled.

---

### startFadeToBlack

```lua
sm.gui.startFadeToBlack( duration, timeout )
```
<code>Client-Only</code> <br></br>

Fades the screen to black and back after timeout.

<strong>Arguments:</strong> <br></br>

- <code>duration</code> [<strong> number </strong>]: The animation duration.
- <code>timeout</code> [<strong> number </strong>]: Time in seconds until the screen fades back.

---

### ticksToTimeString

```lua
sm.gui.ticksToTimeString( ticks )
```
<code>Client-Only</code> <br></br>

Converts ticks to a HH:MM:SS string representation.

<strong>Arguments:</strong> <br></br>

- <code>ticks</code> [<strong> int </strong>]: The ticks.

<strong>Returns:</strong> <br></br>

- [<strong> string </strong>]: The human time formatted string.

---































































