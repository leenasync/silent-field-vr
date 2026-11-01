# Landmine — VR Landmine Defusal Training

> A Virtual Reality training experience on Meta Quest where the trainee gears up, heads out to the desert, locates a buried landmine and defuses it step by step before time runs out. One wrong move ends in an explosion.

**Tuwaiq Academy, VR Bootcamp Graduation Project**

![Unity](https://img.shields.io/badge/Unity-6000.1-black?logo=unity)
![Meta Quest](https://img.shields.io/badge/Platform-Meta%20Quest%20VR-0467DF?logo=meta)
![XRI](https://img.shields.io/badge/XR-XR%20Interaction%20Toolkit%203-green)
![Tuwaiq](https://img.shields.io/badge/Tuwaiq%20Academy-Graduation%20Project-6A1B9A)

---

## Overview

The experience takes place across two scenes:

| Scene | Description |
|-------|-------------|
| 🏠 **Indoor preparation** (`RAHAF2025`) | The trainee starts inside, receives the mission briefing, and equips the gear: helmet, backpack and tools. A checklist confirms each item. |
| 🏜️ **Desert mission** (`hghgh`) | An open desert environment inspired by **AlUla**. The trainee searches for the mine with a metal detector and defuses it. |

## Mission Flow

1. **Gear up** indoors and complete the equipment checklist
2. **Travel to the desert** mission area
3. **Locate the landmine** with the metal detector. The beeps get faster as the trainee gets closer.
4. **Defuse it** by following the correct sequence: open the cover, remove the parts in order, and avoid the wrong move
5. **Beat the clock.** A wrong step or running out of time triggers an explosion.

## Features

- 💣 **Interactive landmine** built from 3D assets, with removable and resettable parts
- 🧩 **Ordered defuse sequence:** each step must be done in the right order
- ⏱️ **Countdown timer** with ticking sound effects
- 💥 **Win and lose feedback:** explosion VFX, post-processing volumes, and success or fail sounds
- 📡 **Metal detector** with proximity-based beeping
- ⌨️ **In-headset virtual keyboard** for entering the player name
- 🎒 **Equipment checklist** using XR sockets
- 🔊 **Ambient desert audio:** wind and birds

## Tech Stack

- **Engine:** Unity 6 (6000.1.14f1), URP
- **XR:** Meta XR SDK Core, OpenXR, XR Interaction Toolkit 3.1, XR Hands
- **Device:** Meta Quest
- **Language:** C#

### Main scripts

| Script | Responsibility |
|--------|----------------|
| `GameLogic` | Mission run: start, timer, defuse, explode |
| `DefuseSequence` / `DefuseStepTrigger` | Ordered defuse steps and fail on a wrong step |
| `SequentialDisassembly` / `CoverOpener` / `ResettablePart` | Interactive bomb parts |
| `TimerUI` / `TimerSFX` | Countdown display and ticking |
| `WinFXController` / `LoseFXController` / `AutoExplosion` | Win and lose effects |
| `TaskChecklist` / `EquipHandler` | Equipment check before the mission |
| `UI_Manager` / `GamePanelUI` / `VirtualKeyboard` | In-game UI and player name input |

## Getting Started

1. Open the project in **Unity 6000.1.14f1** with Android Build Support.
2. Open `Assets/Scenes/RAHAF2025.unity`. It is the first scene in the build list.
3. Connect a Meta Quest headset with Developer Mode enabled.
4. **File → Build Profiles → Android → Build And Run**.

## My Role

**Idea Owner & Lead Developer of the Bomb Experience**

- 💡 **Concept:** came up with the idea of the project
- 💣 **Complete bomb experience:** built the full landmine from 3D assets, set it up and made it interactive
- 🧠 **Full game logic:** designed and programmed the game logic, including the defuse sequence, timer, win and lose conditions, explosion and mission flow
- 🏠 **Indoor scene:** built the indoor preparation scene
- 🏜️ **Desert (AlUla) scene:** built the full outdoor desert environment, including its layout, shapes and composition

> This was a team project. Other parts of the experience were built by my teammates.

## Demo

<!-- ✏️ Add your demo link here -->
- 🎥 Video demo: _coming soon_

## Credits

Third-party assets are the property of their respective authors and are used under their licenses, including Hovl Studio, SkySeries Freebie, SnowyCocoon, Unity Technologies samples, and 3D models from Sketchfab and CGTrader.

## Author

**Leena** · [github.com/leenasync](https://github.com/leenasync)
