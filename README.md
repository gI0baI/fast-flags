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

### Quality Scale Fix
Fixes blurry quality when your display scale is greater than 100%

```json
"DFFlagDisableDPIScale": true
```

### Set FPS Cap
Allows you to set your max FPS limit; however, unlike [RFU](https://github.com/axstin/rbxfpsunlocker)'s memory write mode, the set FPS limit cannot be changed later during the game;

> [!NOTE]
> A more advanced [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#set-fps-cap-1) is available

```json
"DFIntTaskSchedulerTargetFps": 144
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

### Exclusive Fullscreen
Allows you to enter exclusive fullscreen mode by pressing [alt+enter]; significantly improves performance, lowers input latency, with the expense of screen tearing

> [!NOTE]
> V-sync will be disabled upon entering exclusive fullscreen

```json
"FFlagHandleAltEnterFullscreenManually": false
```

## Physics

### Noclip
Allows you to clip through thin walls / floors; the lower the number, the more the thickness of parts you can clip through

> [!CAUTION]
> This Flag is exploitable

```json
"DFFlagAssemblyExtentsExpansionStudHundredth": -30
```

### Fake Lag
Simulates high latency / desync as you will appear behind in the server than what it looks in the client

```json
"DFIntS2PhysicsSenderRate": 1
```

### Wall speeding
Controllable speed hack by gliding on long walls

> [!CAUTION]
> This Flag is exploitable

```json
"DFIntUnstickForceAttackInTenths": -4
```

## Render

### Shadowmap [Lighting Technology](https://create.roblox.com/docs/environment/lighting#technology)
Forces future shadows but voxel lighting

```json
"FFlagDebugForceFutureIsBrightPhase2": true
```

### Future [Lighting Technology](https://create.roblox.com/docs/environment/lighting#technology)
Forces future shadows and lighting

```json
"FFlagDebugForceFutureIsBrightPhase3": true
```

### Voxel [Lighting Technology](https://create.roblox.com/docs/environment/lighting#technology)
Forces voxel shadows and lighting

```json
"DFFlagDebugRenderForceTechnologyVoxel": true
```

### Fix / Force Blurry Textures
Do you have a sh*tty PC? Is Roblox forcing textures to look all slushy and distorted? No problem, this Flag controls all that! Allows you to set the quality of textures from 0 to 3, where 0 and 3 are the lowest and highest quality, respectively

```json
"DFFlagTextureQualityOverrideEnabled": true,
"DFIntTextureQualityOverride": 3
```

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

### Anti-aliasing
Sets the intensity of anti-aliasing by 0 (Default), 1, 2, 4, or 8; the higher the number, the more it may affect performance

```json
"FIntDebugForceMSAASamples": 1,
```

## User Interface

### Hide Guis
Allows you to hide game Guis [ctrl+⇧+c], core Guis [ctrl+⇧+g], billboards [ctrl+⇧+b], and player names [ctrl+⇧+n]

> [!IMPORTANT]
> Requires you to be in a group

```json
"DFIntCanHideGuiGroupId": "GroupId"
```

### Disable Direct3D 11
Disables Direct3D 11 so you can use other 3D APIs

```json
"FFlagDebugGraphicsDisableDirect3D11": true
```

### Direct3D 10
The client will use Direct3D 10

> [!IMPORTANT]
> Requires the Direct3D 11 [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#disable-direct3d-11) to be disabled

```json
"FFlagDebugGraphicsPreferD3D11FL10": true
```

### Direct3D 11
The client will use Direct3D 11

```json
"FFlagDebugGraphicsPreferD3D11": true
```

### OpenGL API
The client will use OpenGL

> [!IMPORTANT]
> Requires the Direct3D 11 [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#disable-direct3d-11) to be disabled

```json
"FFlagDebugGraphicsPreferOpenGL": true
```

### Vulkan API
The client will use Vulkan

> [!IMPORTANT]
> Requires the Direct3D 11 [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#disable-direct3d-11) to be disabled

```json
"FFlagDebugGraphicsPreferVulkan": true
```

### 2015 Gui
The client will use the classic v1 Gui

> [!IMPORTANT]
> Requires the 2024 v4 Gui [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#no-2024-gui) to be disabled

```json
"FFlagDisableNewIGMinDUA": true,
"FFlagEnableInGameMenuControls": false,
"FFlagEnableInGameMenuModernization": false
```

### 2020 Gui
The client will use the v2 side Gui

> [!IMPORTANT]
> Requires the 2024 v4 Gui [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#no-2024-gui) to be disabled

```json
"FFlagDisableNewIGMinDUA": false,
"FFlagEnableInGameMenuControls": false,
"FFlagEnableInGameMenuModernization": false
```

### 2023 Gui
The client will use the modern v3 Gui

> [!IMPORTANT]
> Requires the 2024 v4 Gui [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#no-2024-gui) to be disabled

```json
"FFlagDisableNewIGMinDUA": true,
"FFlagEnableInGameMenuControls": true,
"FFlagEnableInGameMenuModernization": true
```

### No 2024 Gui
Roblox has since forced players to use the new Chrome v4 Gui; these Flags disables it

```json
"FFlagEnableInGameMenuChromeABTest2": false,
"FFlagEnableReportAbuseMenuRoactABTest2": false
```

### Advanced Graphics Quality
Adds more quality bars from 10 to 21 bars

```json
"FFlagFixGraphicsQuality": true
```

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
What are you doing?

```json
"DFFlagNotWhatYoureLookingFor": true
```

### No purchase pop-up
Disables in-game purchases

```json
"DFFlagOrder66": true
```

### No ads
Disables in-game ads and ad portals

```json
"FFlagAdServiceEnabled": false
```

### Force Lottery Win
Makes you win every Roblox's lottery event

```json
"FFlagDebugAnalyticsForceLotteryWin": true
```
