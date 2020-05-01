# G-HUB Mouse Gestures
Lua script to use mouse gestures in macOS using g-hub

## Installation:
In G-HUB select the profile you want to use these gestures in. Click on "scripting". Click on "create a new lua script". (optional) Give the script a name and description. Click on "edit script". Copy the code from this script and paste it in the script editor that just opened. Click "script>save" or press Command+S to save the script. The script should now be working :)

## How to use:
You perform the gestures by pressing the designated button, moving the mouse in the direction of the funtion that you want to use and then releasing the button.

## Gestures for button 4:
Direction | Function  | Buttons | Default
---- | ------- | ----------- | -------
Up | Mission Control | Control+Up-Arrow | Enabled
Down | Application Windows | Control+Down-Arrow | Enabled
Left | Move right a Space | Control+Right-Arrow | Enabled
Right | Move left a Space | Control+Left-Arrow | Enabled

## Gestures for button 5:
Direction | Function  | Buttons | Default
---- | ------- | ----------- | -------
Up | none | n/a | n/a
Down | none | n/a | n/a
Left | Next page | Command+Right-Bracket | Enabled
Right | Previous page | Command+Left-Bracket | Enabled

## Editing the script
If you want to map the gestures to another button assign another button number to gestureButtonNumber
The same goes for browser navigation, in that case assign another button number to navigationButtonNumber

If you want the gesture to happen with more of less movement of your mouse change the value of minimalHorizontalMovement and/or minimalVerticalMovement.

If you want to disable some of the features change the value of missionControlEnabled/ applicationWindowsEnabled/ moveBetweenSpacesEnabled/ browserNavigationEnabled to false

If you want to switch functions just switch the function calls around, it's pretty modular.
If you want to add functions (for example to the two open spots) create a new function, add the keys that bind to the action you want to perform. Call the function from the prefferd "mouseMoved..." function for the preferred buttonNumber.

If you have trouble with understanding what calls get made in what order you can set debuggingEnabeld to true. This will display messages in the console of the editor about what is happening.

If you have trouble with for example finding the names of buttons then in the editor click "Help>Scripting API". This will show you the documentation of scripting with the g-series lua api.
