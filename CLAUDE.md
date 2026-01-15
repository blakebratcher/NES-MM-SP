# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an Adventure Game Studio (AGS) 3.6.x project - "NES-MM-SP" (NES Maniac Mansion Starterpack). It's a game template/starterpack providing a SCUMM-style interface inspired by Day of the Tentacle, featuring the Edison Mansion from the NES version of Maniac Mansion.

## Build and Run

Open `Game.agf` in the AGS Editor to build and run. The project targets Windows and Linux platforms. Resolution is 320x200 in TrueColor.

## Code Architecture

### Script Modules (loaded in order)
- **GlobalScript.asc/.ash** - Main game logic, SCUMM-style verb interface, player movement, interaction handlers. Based on Proskrito's template, modified by Rulaman for AGS 3.x
- **Doors.asc/.ash** - Door state management system with `DoorType` struct and `Door[]` array. Doors have states: `eDoorOpen`, `eDoorClosed`, `eDoorLocked`
- **CharacterChange.asc/.ash** - Multi-character switching system (like original Maniac Mansion). Functions like `SetPlayer()`, `AddChangePlayer()`, `SetPlayers()`
- **Flashlight.asc/.ash** - Dynamic lighting/flashlight effect module (v2.0, requires AGS 3.1.2+)
- **Mansion.asc/.ash** - Edison family detection helpers (`IsEdison()`, `SayIfIsEdison()`, etc.)
- **Credits.asc/.ash** - Scrolling credits module by SSH

### Room Scripts
Room scripts are `room*.asc` files (room1-room43). Each room follows this pattern:
- `room_FirstLoad()` - One-time initialization
- `room_Load()` - Called each time room loads, typically initializes doors via `Door[eDoorNum*].Init()`
- `room_RepExec()` - Repeatedly execute for timers/animations
- `h*_AnyClick()` / `o*_AnyClick()` - Hotspot/object interaction handlers

### Action System
Uses enum `eAction` for verb interactions:
- `eActWalkTo`, `eActLookAt`, `eActTalkTo`, `eActGiveTo`, `eActPickUp`, `eActUse`, `eActOpen`, `eActClose`, `eActPush`, `eActPull`
- Check current action with `UsedAction(eAction)`
- Call `Unhandled()` for default responses

### Door System
Doors are managed via `Door[]` array indexed by `eDoorNum*` enum. Key functions:
- `Door[n].Init(object, hotspot)` - Initialize door in room_Load
- `Door[n].Click()` / `Door[n].ClickSpecial()` - Handle door interactions
- `Door[n].SetStrings()` - Set look/locked/wrong-item messages

### Game Configuration
`v_GameSettingsSet()` in GlobalScript.asc contains game state flags (German comments):
- `gb_*` booleans for game state (swimming pool, doors, plant growth, etc.)
- `gi_*` integers for room options
- `gl_*` for light states (0=off, 1=on, 2=broken)

## Language

Code comments and string literals are primarily in German. Translation files exist: `english.trs`, `espanol.trs`, `francais.trs`.

## MIDI Setup

MIDI requires Timidity patches. See `midi.txt` for setup instructions. Patches go in `timidity/` folder, configured via `timidity.cfg`.
