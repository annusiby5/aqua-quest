# AquaQuest

AquaQuest is a 18 hour Hackathon project, a **Ren'Py visual novel game** built to teach the next generation about the **importance of water conservation** and the real world impact of everyday water use. The game combines **interactive storytelling** with **creative mini games**, helping players learn techniques like:

- Conserving water
- Using collected resources wisely (e.g., rainwater)
- Keeping water sources clean (community cleanup)
- Addressing water loss (fixing leaking pipes)



## Features

- **Story driven gameplay**: Branching flow starting from `label start` in `game/script/script.rpy`.
- **Interactive map navigation**: Bisual map screen with clickable level points.
- **Mini games & learning activities**: Dedicated minigame scripts under `game/script/minigame/`
- **Custom Ren'Py UI**:
  - Styled dialogue boxes, fonts, buttons, and overlays
  - Speech bubble support
  - Animated transitions and UI effects
- **Game menu systems**:
  - Main menu, game menu, preferences, save/load, history, help/about
- **Accessibility friendly controls**: help screen explains keyboard/mouse/gamepad bindings.
- **Audio experience**:
  - Background music and sound effects
  - Character “type” audio (audio type sounds are stored in `game/audio/type/`)


## Technologies Used

- **Python** (Ren'Py scripts)
- **Ren'Py** (visual novel engine)
- **Audacity**
- **Photoshop**


## Project Structure

```
├─ .gitignore
├─ errors.txt
├─ log.txt
├─ README.md
├─ LICENSE
└─ game/
   ├─ gui.rpy
   ├─ options.rpy
   ├─ screens.rpy
   ├─ audio/
   │  ├─ *.mp3 / *.ogg
   │  └─ type/                # character typing/voice sound clips
   ├─ font/
   │  └─ Lonely Cake.ttf
   ├─ gui/                   # UI sprites (textbox, buttons, cursors, etc.)
   ├─ images/
   │  ├─ bg/                  # backgrounds
   │  ├─ chars/               # character images
   │  └─ transition/         # transition assets
   ├─ saves/                 # example saves and persistent data
   ├─ script/
   │  ├─ script.rpy
   │  ├─ script_fn.rpy
   │  ├─ chap*.rpy           # chapter scripts (where available)
   │  └─ minigame/
   │     ├─ water_buck.rpy
   │     └─ waste_pick.rpy
   └─ tl/                     # translations
```

Key files you may want to edit:

- `game/script/script.rpy`: main narrative labels (including `label start`)
- `game/gui.rpy`: GUI styling, screens (say/choice/menu), transitions, and custom UI logic
- `game/options.rpy`: game configuration (name/version, save dir, audio availability, etc.)
- `game/screens.rpy`: additional screen/UI definitions
- `game/script/minigame/*`: the learning mini-games


## Installation / Running

1. **Install Ren'Py**
   - Download and install from: https://www.renpy.org/
   - Ensure you have a supported Python version (Ren'Py typically bundles requirements).

2. **Open the project in Ren'Py**
   - Start Ren'Py and point it to the project folder.
   - The project uses the standard `game/` directory layout.

3. **Run the game**
   - Start the game from Ren'Py using the automatically detected entry.


## Gameplay Flow (High Level)

- The game begins with `label start` in `game/script/script.rpy`.
- Players choose a progression style (e.g., **progress through games** vs **story mode**).
- The project includes:
  - Story scenes (characters, dialogue, transitions)
  - Mini-game activities
  - Map-based navigation to levels


## Notes for Contributors

- Update **UI** in `game/gui.rpy` and any related assets under `game/gui/`.
- Update **game logic** and labels in `game/script/script.rpy` and `game/script/chap*.rpy`.
- Update or add **mini-games** inside `game/script/minigame/`.
- Audio assets should be placed under `game/audio/` and referenced accordingly.


## License

This project is open source and available under the MIT License
