# RPG Adventure: MeGa OKAN


This is a grid-based role-playing game developed using Python's Tkinter library. It features a turn-based combat system, map exploration, character progression, and interactive encounters such as riddles and mystery events.

## Features

* **Map Exploration:** Navigate a 15x15 randomized grid containing Forests, Grasslands, Mountains, Rivers, and Towns.
* **Cleared Area System:** Once a dangerous area (Forest or Grassland) is visited and survived, it becomes safe for future travel.
* **Visual Combat:** A dedicated window for turn-based battles with a combat log and graphical representation of the player and enemy.
* **Leveling System:** Earn XP from battles to increase Level, Max Health, and Attack Power.
* **Interactive Encounters:**
    * **Elders:** Solve riddles to gain permanent stat boosts.
    * **Mystery Spots:** Make risk-vs-reward decisions.
    * **Towns:** Rest to recover health or purchase potions.
* **Inventory System:** Manage health potions and gold.
* **Audio Support:** Background music integration using Pygame.

## Prerequisites

To play this game, you need Python installed on your system along with the following external libraries:

* **Python 3.x**
* **pygame** (for audio playback)
* **Pillow** (for image processing)

## Installation

1.  **Install the required libraries:**
    Open your terminal or command prompt and run the following command:
    
    ```bash
    pip install pygame pillow
    ```

2.  **Prepare the file structure:**
    Ensure all the following files are in the same directory:

    * `rpg_game.py` (The main game script)
    * `rambo_okan.png` (The player character image)
    * `background.jpg` (The window background image)
    * `game_music.mp3` (The background music file)

3.  **Run the game:**
    Execute the script via terminal:

    ```bash
    python rpg_game.py
    ```

## Controls

* **Arrow Up:** Move North
* **Arrow Down:** Move South
* **Arrow Left:** Move West
* **Arrow Right:** Move East
* **Keys 1, 2, 3:** Select options during dialogues (Towns, Riddles, Mystery Events)

## Game Mechanics

### Terrain Types
* **Forest / Grassland:** Standard terrain. Has a 25% chance to trigger a battle if not previously cleared.
* **Mountain:** Difficult terrain. Deals small damage to the player upon entry.
* **River:** Aesthetic terrain, no specific effect.
* **Town:** Safe zone. Allows resting (free full heal) and buying potions.
* **Elder's Hut:** Home of a wise NPC. Correctly answering a riddle grants rewards (Stats or Gold).
* **Mystery Spot:** An unknown event. Presents a choice that can lead to rewards or damage.
* **King's Castle:** The final destination. Reaching this tile completes the game.

### Combat System
* Battles occur in a separate window.
* **Attack:** Deals damage based on player Attack power + RNG.
* **Critical Hits:** Both player and enemies have a 20% chance to deal 1.5x damage.
* **Victory:** Grants Gold and XP.
* **Defeat:** If player Health reaches 0, the game ends.

### Difficulty Settings (Hard Mode Light)
* **Starting Health:** 90
* **Enemy Scaling:** Moderate scaling based on player level.
* **Potion Cost:** 25 Gold.
* **Battle Chance:** 25% on uncleared tiles.

## License

This project is open-source and available for educational purposes.
