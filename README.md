# Tutorial

> [!TIP]
> [Bloxstrap](https://github.com/pizzaboxer/bloxstrap) is highly recommended for modifying the Roblox client

## For those who want to use the [Bloxstrap](https://github.com/pizzaboxer/bloxstrap) Flags menu
1. [⊞+r]
2. `%localappdata%/Bloxstrap/Bloxstrap.exe -menu`
3. Click on FastFlags
4. Click on FastFlag Editor
5. Use common sense

> [!NOTE]
> When adding Flags, it's best to remove the quotation marks around the Flag and value

## For those who want to modify the JSON Flags file

### For [Bloxstrap](https://github.com/pizzaboxer/bloxstrap) Users
1. [⊞+r]
2. `%localappdata%/Bloxstrap/Modifications/ClientSettings/ClientAppSettings.json`

### For Roblox Users
1. [⊞+r]
2. `%localappdata%/Roblox/Versions/ClientSettings/ClientAppSettings.json`

### Modifying the JSON Flags file
3. Open `ClientAppSettings.json` or create a new `.json` file with the name `ClientAppSettings`
4. Follow this format:

```json
{
	"Flag1": "Value1",
	"Flag2": "Value2"
}
```

###### More information about Flags [here](https://github.com/MaximumADHD/Roblox-FFlag-Tracker)

# Fast Flags

## Graphics

### Network Interpolation Visualizer
Highlights physically moving parts by pressing [ctrl+f8][ctrl+i]

> [!CAUTION]
> This Flag is exploitable

```json
"DFFlagDebugEnableInterpolationVisualizer": true
```

### Fix / Force Blurry Textures
Do you have a sh*tty PC? Is Roblox forcing textures to look all slushy and distorted? No problem, this Flag controls all that! Allows you to set the quality of textures from 0 to 3, where 0 and 3 are the lowest and highest quality, respectively

```json
"DFFlagTextureQualityOverrideEnabled": true,
"DFIntTextureQualityOverride": 3
```

### Set FPS Cap
Allows you to set your max FPS limit; however, unlike [RFU](https://github.com/axstin/rbxfpsunlocker)'s memory write mode, the set FPS limit cannot be changed later during the game;

> [!NOTE]
> A more advanced [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#set-fps-cap-1) is available

```json
"DFIntTaskSchedulerTargetFps": "144"
```

### Player Billboard
Adds a black billboard and a red circle above and below every player, respectively

> [!CAUTION] 
> This Flag is exploitable

```json
"FFlagDebugAvatarChatVisualization": true
```

### Display FPS
Displays your FPS without pressing [shift+f5] and showing other details with the expense of not being able to toggle it

```json
"FFlagDebugDisplayFPS": true
```

### Advanced Graphics Quality
Adds more quality bars from 10 to 21 bars

```json
"FFlagFixGraphicsQuality": true
```

### Anti-aliasing
Sets the intensity of anti-aliasing by 0 (Default), 1, 2, 4, or 8; the higher the number, the more it may impact the performance

```json
"FIntDebugForceMSAASamples": 1,
```

## Physics

### Noclip
Allows you to clip through thin walls / floors; the lower the number, the more the thickness of parts you can clip through

> [!CAUTION]
> This Flag is exploitable

```json
"DFFlagAssemblyExtentsExpansionStudHundredth": "-30"
```

### Fake Lag
Simulates high latency / desync as you will appear behind in the server than what it looks in the client

```json
"DFIntS2PhysicsSenderRate": "1"
```

### Wall speeding
Controllable speed hack by gliding on long walls

> [!CAUTION]
> This Flag is exploitable

```json
"DFIntUnstickForceAttackInTenths": -4
```

## Render

### Low Mesh and Union Detail
Unions and meshes are composed of [constructive solid geometry](https://devforum.roblox.com/t/quick-guide-into-csg-increasing-performance-of-unions-meshes/627677) or CSG, which enables Roblox to form complex shapes. This Flag lowers the detail and quality of CSG parts, effectively improving performance.

```json
"DFIntCSGLevelOfDetailSwitchingDistance": 0,
"DFIntCSGLevelOfDetailSwitchingDistanceL12": 0,
"DFIntCSGLevelOfDetailSwitchingDistanceL23": 0,
"DFIntCSGLevelOfDetailSwitchingDistanceL34": 0
```

### No Player Textures
Stop rendering every player's clothing, making them appear grey

```json
"DFIntTextureCompositorActiveJobs": 0
```

## User Interface

### Set FPS Cap
Allows you to set your max FPS limit in the Roblox settings by 30, 60, 144, and 240; requires the target fps [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#set-fps-cap) to be 0 (Default)

```json
"FFlagGameBasicSettingsFramerateCap": true
```

### Set Camera Zoom Limit
Allows you to set your camera's max zoom limit; does not work on games with customized zoom limits

```json
"FIntCameraMaxZoomDistance": 16384
```

## Others

### Not What You're Looking For
Disables [Byfron](https://devforum.roblox.com/t/welcoming-byfron-to-roblox/2018233)

> [!CAUTION]
> This Flag is exploitable

```json
"DFFlagNotWhatYoureLookingFor": true
```

### No purchase pop-up
Disables in-game purchases

```json
"DFFlagOrder66": true
```

### Force Lottery Win
Makes you win every Roblox's lottery event

```json
"FFlagDebugAnalyticsForceLotteryWin": true
```

### No ads
Disables in-game ads and ad portals

```json
"FFlagAdServiceEnabled": false
```
