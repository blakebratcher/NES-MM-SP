<div align="center">

# 🏚️ NES Maniac Mansion Starterpack

[![AGS Version](https://img.shields.io/badge/AGS-3.6.x-blue?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA4AAAAOCAYAAAAfSC3RAAAACXBIWXMAAAsTAAALEwEAmpwYAAAA00lEQVR4nGNgGAUwwIiNcP78+f8cHBwMJGlkZGRkuHDhAgMjIyMDXuP+//8PVwxWiE0xCGBTBAJYNYIAVo0ggFUjCGDVCAJYNYIAVo0ggFUjCBBrIwgQ1AgCBDViA1g1ggBWjSCAVSMIYNUIAlg1ggBWjSCAVSMIYNUIAkQ1ggBBjSBAUCMI4NsIA7g0wgAujTCASyMM4NIIA7g0wgAujTBAyEYYINZGGCCkEQaI1QgD+DTCALEaYQCfRhjApxEG8GmEAXwaYQCfRhjAp3EUDDYAABa3V/K7ADmkAAAAAElFTkSuQmCC)](https://www.adventuregamestudio.co.uk/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-lightgrey?style=for-the-badge&logo=windows)](https://github.com/blakebratcher/NES-MM-SP)
[![Resolution](https://img.shields.io/badge/Resolution-320x200-orange?style=for-the-badge)](https://github.com/blakebratcher/NES-MM-SP)
[![Language](https://img.shields.io/badge/Language-German%20%7C%20English-yellow?style=for-the-badge)](https://github.com/blakebratcher/NES-MM-SP)

[![Stars](https://img.shields.io/github/stars/blakebratcher/NES-MM-SP?style=for-the-badge&logo=github&color=gold)](https://github.com/blakebratcher/NES-MM-SP/stargazers)
[![Forks](https://img.shields.io/github/forks/blakebratcher/NES-MM-SP?style=for-the-badge&logo=github&color=silver)](https://github.com/blakebratcher/NES-MM-SP/network/members)
[![Issues](https://img.shields.io/github/issues/blakebratcher/NES-MM-SP?style=for-the-badge&logo=github&color=red)](https://github.com/blakebratcher/NES-MM-SP/issues)
[![Last Commit](https://img.shields.io/github/last-commit/blakebratcher/NES-MM-SP?style=for-the-badge&logo=github&color=blue)](https://github.com/blakebratcher/NES-MM-SP/commits/master)

<br>

**🎮 A complete Adventure Game Studio starterpack featuring the Edison Mansion from the NES version of Maniac Mansion with a Day of the Tentacle-inspired SCUMM interface**

<br>

[Getting Started](#-getting-started) •
[Features](#-features) •
[MIDI Setup](#-midi-setup) •
[Documentation](#-documentation) •
[Credits](#-credits)

<br>

---

</div>

## 📖 About

The **NES Maniac Mansion Starterpack** is a comprehensive template for creating point-and-click adventure games using [Adventure Game Studio](https://www.adventuregamestudio.co.uk/). It provides:

- 🏰 **Complete Edison Mansion** - All rooms from the NES version of Maniac Mansion
- 🎯 **SCUMM-style Interface** - Classic verb-based interaction system inspired by Day of the Tentacle
- 👥 **Multi-character System** - Switch between playable characters like the original game
- 🔦 **Dynamic Lighting** - Built-in flashlight module for atmospheric dark rooms
- 🚪 **Door Management System** - Fully featured door state handling (open/closed/locked)
- 🎬 **Credits Module** - Ready-to-use scrolling credits system

<div align="center">

```
┌─────────────────────────────────────────────────────────────┐
│  ╔═══════════════════════════════════════════════════════╗  │
│  ║           MANIAC MANSION - NES EDITION                ║  │
│  ║                                                       ║  │
│  ║    ┌─────────────────────────────────────────────┐    ║  │
│  ║    │            🏚️ EDISON MANSION 🏚️            │    ║  │
│  ║    │                                             │    ║  │
│  ║    │      "Don't be a tuna head!"               │    ║  │
│  ║    │                                             │    ║  │
│  ║    └─────────────────────────────────────────────┘    ║  │
│  ║                                                       ║  │
│  ║   [Walk to] [Look at] [Pick up] [Use] [Open] [Push]  ║  │
│  ╚═══════════════════════════════════════════════════════╝  │
└─────────────────────────────────────────────────────────────┘
```

</div>

## ✨ Features

<table>
<tr>
<td width="50%">

### 🎮 Gameplay Systems
- **9 Verb Actions** - Walk, Look, Talk, Give, Pick up, Use, Open, Close, Push, Pull
- **Character Switching** - Multiple playable characters
- **Inventory System** - Full inventory management with cursor items
- **Dialog System** - LucasArts-style speech system

</td>
<td width="50%">

### 🛠️ Technical Features
- **43 Rooms** - Complete mansion layout
- **Door System** - State-based door management
- **Flashlight Module** - Dynamic lighting effects
- **Save/Load System** - Built-in game state persistence
- **Multi-language** - German, English, Spanish, French

</td>
</tr>
</table>

## 🚀 Getting Started

### Prerequisites

- [Adventure Game Studio 3.6.x](https://www.adventuregamestudio.co.uk/site/ags/download/) or later

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/blakebratcher/NES-MM-SP.git
   ```

2. **Open in AGS Editor**
   ```
   Open Game.agf in Adventure Game Studio Editor
   ```

3. **Build and Run**
   ```
   Press F5 to compile and run the game
   ```

## 🎵 MIDI Setup

To enable MIDI music playback, you need to set up Timidity:

1. **Create the timidity folder** in your game's root directory

2. **Download patches** from [dgguspat.zip](http://www.gamers.org/pub/idgames/music/dgguspat.zip)

3. **Extract patches** to the `timidity/` folder

4. **Configure** - The `timidity.cfg` file is already included in this repository

<details>
<summary>📁 Expected folder structure</summary>

```
NES-MM-SP/
├── Game.agf
├── timidity.cfg
└── timidity/
    ├── acpiano.pat
    ├── britepno.pat
    ├── synpiano.pat
    └── ... (other .pat files)
```

</details>

## 📚 Documentation

### Project Structure

| File/Folder | Description |
|-------------|-------------|
| `Game.agf` | Main AGS project file |
| `GlobalScript.asc` | Core game logic and SCUMM interface |
| `Doors.asc` | Door management system |
| `CharacterChange.asc` | Multi-character switching |
| `Flashlight.asc` | Dynamic lighting module |
| `Credits.asc` | Scrolling credits system |
| `room*.asc` | Individual room scripts (1-43) |
| `*.trs` | Translation files |

### Action System

```
eActWalkTo    (0)  - Walk to location
eActLookAt    (1)  - Examine object
eActTalkTo    (2)  - Talk to character
eActGiveTo    (3)  - Give item to character
eActPickUp    (4)  - Pick up object
eActUse       (5)  - Use object/item
eActOpen      (6)  - Open door/container
eActClose     (7)  - Close door/container
eActPush      (8)  - Push object
eActPull      (9)  - Pull object
```

### Door States

```csharp
eDoorOpen   = 1  // Door is open
eDoorClosed = 0  // Door is closed
eDoorLocked = 2  // Door is locked
```

## 🎨 Customization

### Adding Your Episode Credits

Edit `room4.asc` to customize the credits for your episode:

```csharp
// Bitte erst ab hier ändern oder neues einfügen
Credits[0].AddTitle("]Diese Episode:~");
Credits[0].AddCredit("<Your Name Here>");
Credits[0].AddTitle(" [Idee:]");
Credits[0].AddCredit("<Your Name Here>");
```

## 🤝 Credits

<div align="center">

| Role | Contributor |
|------|-------------|
| **Original Starterpack** | hansa-export |
| **NES Version** | Kiwa |
| **AGS 3.0 Conversion** | Rulaman |
| **Original Template** | Proskrito |
| **Credits Module** | SSH |
| **Adventure Game Studio** | Chris Jones |

</div>

## 📜 License

This project is available for use in creating fan games and adventure game projects. Please credit the original contributors when using this starterpack.

## 🔗 Links

<div align="center">

[![AGS Forums](https://img.shields.io/badge/AGS-Forums-blue?style=for-the-badge)](https://www.adventuregamestudio.co.uk/forums/)
[![AGS Wiki](https://img.shields.io/badge/AGS-Wiki-green?style=for-the-badge)](https://adventuregamestudio.github.io/ags-manual/)
[![Maniac Mansion Mania](https://img.shields.io/badge/Maniac%20Mansion-Mania-purple?style=for-the-badge)](https://www.maniac-mansion-mania.com/)

</div>

---

<div align="center">

**Made with ❤️ for the Adventure Game Community**

<sub>This is a fan project and is not affiliated with LucasArts or Disney.</sub>

</div>
