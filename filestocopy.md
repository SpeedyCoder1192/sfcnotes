---
layout: default
title: Files to Copy Over
---

# Files to Copy to Main Game

## For Freecam+ to work:

### 1. ServerScriptService.ServerScriptService (entire folder)
- `Config` (ModuleScript with Freecam+ settings)
- `loader` (Script that loads Freecam+)

### 2. ReplicatedStorage.Icon (entire module)
- This is the TopBarPlus Icon module that Freecam+ uses for its button
- Includes: Types, VERSION, Reference, Attribute, Utility, Elements, Features, Packages

### 3. StarterPlayer.StarterPlayerScripts.StaterPlayerScripts.TopBarPlus (LocalScript)
- Handles positioning the Freecam+ button on the topbar

---

## For EXE V5 Custom Commands to work:

### 1. ServerScriptService.exe_manager (entire folder)
- `manager` (main script)
- `IDSAVING` (module)
- `ELEMENTS` (module)
- `exe_scripts` folder containing:
  - `filter_string_invoke`
  - `custom_command_handler`
  - `webhook_handler`
  - `events_handler`
  - `server_status` folder
  - `server_bans` folder

### 2. ReplicatedStorage.exe_storage (entire folder)
**Modules:**
- `exe_module`
- `filter_module`
- `notify_module`
- `slider_service`
- `transparency_module`
- `configuration`
- `custom_commands` (defines all custom commands)

**Folders:**
- `events` folder (all RemoteEvents/RemoteFunctions)
  - `custom_command_events` folder (critical for custom commands)
  - `banit_events` folder
  - `webhook_events` folder
  - Various RemoteFunctions for access, bans, etc.
- `tools` folder (Building Tools, Gravity Coil, Speed Coil, Fly, etc.)
- `objects` folder (bubble, jail, uptime, etc.)
- `effects` folder (Soul Fire, Rays, Auras, etc.)

### 3. StarterGui.exe (entire ScreenGui)
- `exe_main_module` (ModuleScript)
- `storage` folder
- `notification` (ImageButton)
- `announcement` (Frame)
- `frame` (ImageButton - main admin panel)
  - Contains all panels: dashboard_frame, main_frame, assets_panels, direct_action_panels, profile_panel, tools_panels, menu_frame, credits_frame, etc.

### 4. TextChatService chat commands
- `reset_exe` (TextChatCommand - `/resetexe`)
- `toggle_exe` (TextChatCommand - `/exe`)

---

## Summary Checklist

### Freecam+ (3 items):
- [ ] ServerScriptService.ServerScriptService folder
- [ ] ReplicatedStorage.Icon module
- [ ] StarterPlayer.StarterPlayerScripts.StaterPlayerScripts.TopBarPlus

### EXE V5 (4 items):
- [ ] ServerScriptService.exe_manager folder
- [ ] ReplicatedStorage.exe_storage folder
- [ ] StarterGui.exe ScreenGui
- [ ] TextChatService.reset_exe & toggle_exe commands