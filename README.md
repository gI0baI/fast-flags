> [!WARNING]
> In the near future, Roblox is planning to [patch](https://i.redd.it/4c5u68gczbkc1.jpeg) [local Fast Flag modification](https://github.com/pizzaboxer/bloxstrap/issues/1321) by utilizing the [ClientSettings API](https://clientsettings.roblox.com/docs/index.html) for fetching the `ClientSettings.json` file. ~~Probably the same reason why you can't change material textures locally now~~. As of 07/04/2024, Roblox has not yet forced the update through the [Live channel](https://clientsettings.roblox.com/v2/client-version/WindowsPlayer/channel/Live).

# Tutorial

> [!TIP]
> [Bloxstrap](https://github.com/pizzaboxer/bloxstrap) is highly recommended for modifying the Roblox client.

## For Those Who Want to Use the [Bloxstrap](https://github.com/pizzaboxer/bloxstrap) Flags Menu
1. Press [⊞+r]
2. Type `%localappdata%/Bloxstrap/Bloxstrap.exe -menu`
3. Click on FastFlags
4. Click on FastFlag Editor
5. Use common sense

> [!NOTE]
> When adding Flags, it's best to remove the quotation marks around the Flag and value.

## For Those Who Want to Modify the JSON Flags File

### For [Bloxstrap](https://github.com/pizzaboxer/bloxstrap) Users
1. Press [⊞+r]
2. Type `%localappdata%/Bloxstrap/Modifications/ClientSettings/ClientAppSettings.json`

### For Roblox Users
1. Press [⊞+r]
2. Type `%localappdata%/Roblox/Versions/ClientSettings/ClientAppSettings.json`

> [!NOTE]
> For every installation and update, Roblox clears the `ClientSettings` folder. It's best to keep a backup of your `ClientAppSettings.json` file. You may install [Bloxstrap](https://github.com/pizzaboxer/bloxstrap) for automatic changes.

### Modifying the JSON Flags File
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

May this list serve as an in-depth explanation to different Flags you may have heard of but not familiar with its functionality. You may fork and send a pull request if you have any corrections / suggestions that deserves to be in this list.

- [Graphics](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#graphics)
- [Physics](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#physics)
- [Render](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#render)
- [User Interface](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#user-interface)
- [Others](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#others)
- [Credits](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#credits)

## Graphics

### Network Interpolation Visualizer
`false` Highlights physically moving parts by pressing [ctrl+f8][ctrl+i].

> [!CAUTION]
> This Flag is exploitable.

```json
{
	"DFFlagDebugEnableInterpolationVisualizer": true
}
```

### Quality Scale Fix
`false` Fixes blurry quality when your display scale is greater than 100%.

```json
{
	"DFFlagDisableDPIScale": true
}
```

### Set FPS Cap
`0` Allows you to set your max FPS limit. However, unlike [RFU](https://github.com/axstin/rbxfpsunlocker)'s memory write mode, the set FPS limit cannot be changed later during the game.

> [!NOTE]
> A more advanced [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#set-fps-cap-1) is available.

```json
{
	"DFIntTaskSchedulerTargetFps": 144
}
```

### Player Billboard
`false` Adds a black billboard and a red circle above and below every player, respectively.

> [!CAUTION] 
> This Flag is exploitable.

```json
{
	"FFlagDebugAvatarChatVisualization": true
}
```

### Display FPS
`false` Displays your FPS without pressing [shift+f5] and showing other details with the expense of not being able to toggle it.

```json
{
	"FFlagDebugDisplayFPS": true
}
```

### Exclusive Fullscreen
`true` Allows you to enter exclusive fullscreen mode by pressing [alt+enter]. Significantly improves performance, lowers input latency, with the expense of screen tearing.

> [!NOTE]
> V-sync will be disabled upon entering exclusive fullscreen.

```json
{
	"FFlagHandleAltEnterFullscreenManually": false
}
```

## Physics

### Noclip
`30` Allows you to clip through thin walls / floors. The lower the number, the more the thickness of parts you can clip through.

> [!CAUTION]
> This Flag is exploitable.

```json
{
	"DFIntAssemblyExtentsExpansionStudHundredth": -30
}
```

### Set Physics FPS Cap
`16` Allows you to set the max physics limit, however it only goes above 15 and below 60 to literally prevent speed hacking. Setting it to `9223372036854776000` prevents the physics FPS from going below 60, useful to prevent slow-downs during FPS drops.

```json
{
	"DFIntMaxMissedWorldStepsRemembered": 9223372036854776000
}
```

### Fake Lag
`15` Simulates high latency / desync as you will appear behind in the server than what it looks in the client.

```json
{
	"DFIntS2PhysicsSenderRate": 1
}
```

### Wall speeding
`1` Controllable speed hack by gliding on long walls.

> [!CAUTION]
> This Flag is exploitable.

```json
{
	"DFIntUnstickForceAttackInTenths": -4
}
```

## Render

### Shadowmap [Lighting Technology](https://create.roblox.com/docs/environment/lighting#technology)
`false` Forces future shadows but voxel lighting.

```json
{
	"FFlagDebugForceFutureIsBrightPhase2": true
}
```

### Future [Lighting Technology](https://create.roblox.com/docs/environment/lighting#technology)
`false` Forces future shadows and lighting.

```json
{
	"FFlagDebugForceFutureIsBrightPhase3": true
}
```

### Voxel [Lighting Technology](https://create.roblox.com/docs/environment/lighting#technology)
`false` Forces voxel shadows and lighting.

```json
{
	"DFFlagDebugRenderForceTechnologyVoxel": true
}
```

### Disable Direct3D 11
`false` Disables Direct3D 11 so you can use other 3D APIs.

```json
{
	"FFlagDebugGraphicsDisableDirect3D11": true
}
```

### Direct3D 10
`false` The client will use Direct3D 10 as the 3D rendering API.

> [!IMPORTANT]
> Requires the Direct3D 11 [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#disable-direct3d-11) to be disabled.

```json
{
	"FFlagDebugGraphicsPreferD3D11FL10": true
}
```

### Direct3D 11
`false` The client will use Direct3D 11 as the 3D rendering API.

```json
{
	"FFlagDebugGraphicsPreferD3D11": true
}
```

### OpenGL API
`false` The client will use OpenGL as the 3D rendering API.

> [!IMPORTANT]
> Requires the Direct3D 11 [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#disable-direct3d-11) to be disabled.

```json
{
	"FFlagDebugGraphicsPreferOpenGL": true
}
```

### Vulkan API
`false` The client will use Vulkan as the 3D rendering API.

> [!IMPORTANT]
> Requires the Direct3D 11 [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#disable-direct3d-11) to be disabled.

```json
{
	"FFlagDebugGraphicsPreferVulkan": true
}
```

### Fix / Force Blurry Textures
`false` `3` Do you have a sh*tty PC? Is Roblox forcing textures to look all slushy and distorted? No problem, this Flag controls all that! It allows you to set the quality of textures from `0` to `3`, where `0` and `3` are the lowest and highest quality, respectively.

```json
{
	"DFFlagTextureQualityOverrideEnabled": true,
	"DFIntTextureQualityOverride": 3
}
```

### Low Mesh and Union Detail
`250` `500` `2000` `3000` Unions and meshes are composed of small polygons like triangles with the help of [constructive solid geometry](https://devforum.roblox.com/t/quick-guide-into-csg-increasing-performance-of-unions-meshes/627677) or CSG. This Flag lowers the detail and quality of CSG parts by reducing the amount of polygons rendered.

```json
{
	"DFIntCSGLevelOfDetailSwitchingDistance": 0,
	"DFIntCSGLevelOfDetailSwitchingDistanceL12": 0,
	"DFIntCSGLevelOfDetailSwitchingDistanceL23": 0,
	"DFIntCSGLevelOfDetailSwitchingDistanceL34": 0
}
```

### No Player Textures
`8` Stops rendering every player's clothing, making them appear grey.

```json
{
	"DFIntTextureCompositorActiveJobs": 0
}
```

### Anti-aliasing
`0` Sets the intensity of anti-aliasing by `0` (Default), `1`, `2`, `4`, or `8`. The higher the number, the more it may impact performance.

```json
{
	"FIntDebugForceMSAASamples": 1
}
```

### Set Light Updates <sub>by [catb0x](https://github.com/catb0x/roblox-potato-fflags)</sub>
`8` `2` Limits light updates.

```json
{
	"FIntRenderLocalLightUpdatesMax": 1,
	"FIntRenderLocalLightUpdatesMin": 1
}
```

### No Shadows
`75` Disables part and player shadows.

```json
{
	"FIntRenderShadowIntensity": 0
}
```

### No Post-Processing Effects
`false` Disables all [post-processing effects](https://create.roblox.com/docs/environment/post-processing-effects) like blur and depth-of-field.

```json
{
	"FFlagDisablePostFx": true
}
```

## User Interface

### Hide Guis
`4358041` Allows you to hide game Guis [ctrl+⇧+c], core Guis [ctrl+⇧+g], billboards [ctrl+⇧+b], and player names [ctrl+⇧+n].

> [!IMPORTANT]
> Requires you to be in a [group](https://www.roblox.com/groups/32380007).

> [!TIP]
> Use with the Gui toggle [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#hide-guis-1) for best experience.

```json
{
	"DFIntCanHideGuiGroupId": 32380007
}
```

### No Chat
`false` Helps you focus on the game rather than having to deal with salty kids.

```json
{
	"FFlagDebugForceChatDisabled": true
}
```

### No Sound Drivers
`false` Disables Roblox from detecting audio output devices.

```json
{
	"FFlagDebugRomarkMockingAudioDevices": true
}
```

### 2015 Gui
`false` `false` `false` The client will use the classic v1 Gui.

> [!IMPORTANT]
> Requires the 2024 Chrome Gui [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#no-2024-gui) to be disabled.

```json
{
	"FFlagDisableNewIGMinDUA": true,
	"FFlagEnableInGameMenuControls": false,
	"FFlagEnableInGameMenuModernization": false
}
```

### 2020 Gui
`false` `false` `false` The client will use the v2 side bar Gui.

> [!IMPORTANT]
> Requires the 2024 Chrome Gui [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#no-2024-gui) to be disabled.

> [!NOTE]
> Why is there no 2022 v3 Gui? Basically, v2 and v3 are the same Guis, it's just that the files Roblox used for handling the v3 Gui have been removed.

```json
{
	"FFlagDisableNewIGMinDUA": false,
	"FFlagEnableInGameMenuControls": false,
	"FFlagEnableInGameMenuModernization": false
}
```

### 2023 Gui
`false` `false` `false` The client will use the modern v4 Gui.

> [!IMPORTANT]
> Requires the 2024 Chrome Gui [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#no-2024-gui) to be disabled.

```json
{
	"FFlagDisableNewIGMinDUA": true,
	"FFlagEnableInGameMenuControls": true,
	"FFlagEnableInGameMenuModernization": true
}
```

### No 2024 Gui
`true` `true` Roblox has since forced players to use the new Chrome Gui; these Flags disables it.

```json
{
	"FFlagEnableInGameMenuChromeABTest2": false,
	"FFlagEnableReportAbuseMenuRoactABTest2": false
}
```

### Advanced Graphics Quality
`false` Adds more quality bars from 10 to 21 bars.

```json
{
	"FFlagFixGraphicsQuality": true
}
```

### Set FPS Cap
`false` Allows you to set your max FPS limit in the Roblox settings by 30, 60, 144, or 240.

> [!IMPORTANT]
> Requires the target fps [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#set-fps-cap) to be set to 0 (Default).

```json
{
	"FFlagGameBasicSettingsFramerateCap": true
}
```

### Hide Guis
`false` `false` Allows you to toggle game Guis in the Roblox settings.

```json
{
	"FFlagUserShowGuiHideToggles": true,
	"GuiHidingApiSupport2": true
}
```

### Set Camera Zoom Limit
`400` Allows you to set your camera's max zoom limit. Does not work on games with customized zoom limits.

```json
{
	"FIntCameraMaxZoomDistance": 16384
}
```

### No Roblox Blur Overlay
`24` Disables the blur you see in loading and disconnection screens.

```json
{
	"FIntRobloxGuiBlurIntensity": 0
}
```

### Set Start Graphics Quality
`-1` Allows you to set the graphics quality Roblox will always start with. Up to 10 by default, and up to 21 if the quality [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#advanced-graphics-quality) is enabled.

```json
{
	"FIntRomarkStartWithGraphicQualityLevel": 1
}
```

## Others

### Not What You're Looking For
`false` *What are you doing?*

```json
{
	"DFFlagNotWhatYoureLookingFor": true
}
```

### No Purchase Pop-up
`false` Disables in-game purchases.

```json
{
	"DFFlagOrder66": true
}
```

### No Ads
`true` Disables in-game ads and ad portals.

```json
{
	"FFlagAdServiceEnabled": false
}
```

### Force Lottery Win
`false` *Makes you win every Roblox's lottery event.*

```json
{
	"FFlagDebugAnalyticsForceLotteryWin": true
}
```

### Inhibit Roblox Data Collection
`false` `false` `false` `false` `false` `false` `false` Does not fully disable Roblox's telemetry system but stops most collection of user data.

```json
{
	"FFlagDebugDisableTelemetryEphemeralCounter": true,
	"FFlagDebugDisableTelemetryEphemeralStat": true,
	"FFlagDebugDisableTelemetryEventIngest": true,
	"FFlagDebugDisableTelemetryPoint": true,
	"FFlagDebugDisableTelemetryV2Counter": true,
	"FFlagDebugDisableTelemetryV2Event": true,
	"FFlagDebugDisableTelemetryV2Stat": true
}
```

### [Bloxstrap](https://github.com/pizzaboxer/bloxstrap) Activity Tracking ([Bloxstrap](https://github.com/pizzaboxer/bloxstrap) Only)
`undefined` Allows [Bloxstrap](https://github.com/pizzaboxer/bloxstrap) to display information about the games you play, as well as enabling [Discord Rich Presence](https://discord.com/developers/docs/rich-presence/how-to) for your profile.

```json
{
	"FLogNetwork": 7
}
```

# Credits
- [Bloxstrap Discord](https://discord.gg/nKjV3mGq6R)
- [Epic Fast Flags List](https://github.com/devstacking/Epic-Fast-Flags-List)
- [Fast Flags Collection](https://github.com/GoingCrazyDude/fastflags-collection/)
- [Fast Flags Collective](https://github.com/FastFlags/FastFlags-Collective) :3
- [Potato Flags](https://github.com/catb0x/roblox-potato-fflags)
- [Roblox FFlag Tracker](https://github.com/MaximumADHD/Roblox-FFlag-Tracker)
