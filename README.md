## Tutorial

### For Bloxstrap Users
1. [⊞+r]
2. `%localappdata%/Bloxstrap/Modifications/ClientSettings/ClientAppSettings.json`

### For Roblox Users
1. [⊞+r]
2. `%localappdata%/Roblox/Versions/ClientSettings/ClientAppSettings.json`

### Format
3. Follow this format:

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

```json
"DFFlagDebugEnableInterpolationVisualizer": true
```

### Set FPS Cap
Allows you to set your max FPS limit; however, unlike [RFU](https://github.com/axstin/rbxfpsunlocker)'s memory write mode, the set FPS limit cannot be changed later during the game; a more advanced [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#set-fps-cap-1) is available

```json
"DFIntTaskSchedulerTargetFps": "144"
```

### Player Billboard
Adds a grey billboard and a red circle above and below every player, respectively

```json
"FFlagDebugAvatarChatVisualization": true
```

### Display FPS
Displays your FPS without pressing [shift+f5] and other details with the expense of toggling

```json
"FFlagDebugDisplayFPS": true
```

### Advanced Graphics Quality
Adds more quality bars from 10 to 21 bars

```json
"FFlagFixGraphicsQuality": true
```

## Physics

### Noclip
Allows you to clip through thin walls / floors; the lower the number, the more the thickness of parts you can clip through

```json
"DFFlagAssemblyExtentsExpansionStudHundredth": "-30"
```

### Fake Lag
Simulates high latency / desync as you will appear late in the server than the client

```json
"DFIntS2PhysicsSenderRate": "1"
```

### Wall speeding
Controllable speed hack by gliding on long walls

```json
"DFIntUnstickForceAttackInTenths": -4
```

## User Interface

### Set FPS Cap
Allows you to set your max FPS limit in the Roblox settings by 30, 60, 144, and 240; requires the target fps [Flag](https://github.com/gI0baI/fast-flags/?tab=readme-ov-file#set-fps-cap) to Default (0)

```json
"FFlagGameBasicSettingsFramerateCap": true,
```
