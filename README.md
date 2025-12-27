# MinyCraft - 2D Minecraft Clone

[MinyCraft logo](assets/icon.png)

A 2D left-right view Minecraft clone built with Haxe, OpenFL, and HaxeFlixel.

## Features

### Core Gameplay

- **Survival Mode**: Mine blocks, gather resources, survive
- **Creative Mode**: Unlimited blocks, flying, no health/hunger
- **Inventory System**: 36-slot inventory with 9-slot hotbar
- **Crafting**: Basic crafting system (to be expanded)

### World Generation

- **Procedural Terrain**: Infinite world generation
- **Biomes**: Plains, mountains, deserts, forests, oceans
- **Caves**: Natural cave systems
- **Ores**: Coal, iron, gold, diamond
- **Trees**: Procedurally generated trees

### Graphics & UI

- **Title Screen**: With game options
- **World Manager**: Create, load, delete worlds
- **Options Menu**: Graphics, sound, controls
- **Hotbar**: Quick item selection
- **Health/Hunger System**: Survival mechanics

### Mod Support

- **Mod Loader**: Load mods from /mods folder
- **Block Registration**: Add custom blocks via JSON
- **API System**: Extensible modding API

## Controls

### Movement

- **W/A/S/D or Arrow Keys**: Move
- **Space**: Jump
- **Shift**: Sneak (in survival) / Fly down (in creative)

### Gameplay

- **Left Click**: Mine/attack
- **Right Click**: Place block/use item
- **1-9**: Select hotbar slot
- **Mouse Wheel**: Cycle hotbar
- **E**: Open inventory
- **G**: Toggle game mode (creative only)
- **ESC**: Pause menu

### UI

- **Enter**: Confirm/select
- **Tab**: Next field
- **ESC**: Back/cancel

## Installation

### Prerequisites

1. Install Haxe: https://haxe.org/download/
2. Install OpenFL: `haxelib install openfl`
3. Install HaxeFlixel: `haxelib install flixel`
4. Install additional libraries:

- `haxelib install flixel-addons`
- `haxelib install flixel-ui`
- `haxelib install hscript`

### Building

1. Clone this repository
2. Navigate to project directory
3. Build for your target:

- HTML5: `lime test html5`
- Windows: `lime test windows`
- Mac: `lime test mac`
- Linux: `lime test linux`

### Running

1. After building, find the executable in the `export` folder
2. Or run directly: `lime test [target]`

## Modding

### Creating a Mod

1. Create a folder in `/assets/mods/`
2. Add a `mod.json` file:

```json
{
  "id": "your_mod_id",
  "name": "Your Mod Name",
  "version": "1.0.0",
  "author": "Your Name",
  "description": "Mod description"
}
```

3. Add blocks in blocks.json:

```json
[
  {
    "id": "custom_block",
    "name": "Custom Block",
    "color": "#FF0000",
    "hardness": 1.5,
    "drops": ["your_mod_id:custom_block"],
    "transparent": false
  }
]
```

# Development

## Adding New Blocks

1. Add to BlockType enum in `world/Block.hx`

2. Define block properties in `loadBlockData()`

3. Add color in `getColor()`

## Adding New Features

1. Create new classes in appropriate directories

2. Update existing systems as needed

3. Test thoroughly

4. Known Issues & TODO

## Current Limitations

1. Simple graphics (colored blocks only)

2. Basic physics

3. Limited mobs/entities

4. Simple crafting system

## Planned Features

- Mobs and animals

- Day/night cycle

- Weather system

- Multiplayer support

- Advanced crafting

- Redstone-like mechanics

- Better graphics (textures)

- Sound effects

- Music system

- Achievement system

- World saving/loading

## Contributing

1. Fork the repository

2. Create a feature branch

3. Make your changes

4. Test thoroughly

5. Submit a pull request

## License

This project is licensed under the MIT License - see LICENSE file for details.

## Credits

Development: **Sheldi Pierre**

Inspired by: **Minecraft** (Mojang Studios)

Built with: **Haxe**, OpenFL, HaxeFlixel

## Support

For issues and feature requests, please use the GitHub Issues page.

> Enjoy MinyCraft!

## How to Run the Game

1. **Install the prerequisites** as mentioned in the README
2. **Create the project structure** with all the files
3. **Build the game**:
   ```bash
   lime test html5  # For web version
   lime test windows  # For Windows
   lime test mac  # For Mac
   lime test linux  # For Linux
   ```
   Run the game from the export folder or directly with `lime test`

## Key Features Implemented

Complete Game Flow: Title → World Manager → Game

2D Minecraft-like Gameplay: Mining, placing, inventory

Dual Game Modes: Survival and Creative

Procedural World Generation: Biomes, caves, ores, trees

Mod Support: Basic mod loading system

UI Systems: Hotbar, health/hunger, world management

Save/Load: World saving system

## Next Steps for Expansion

1. Add texture support for blocks

2. Implement more Minecraft features (crafting table, furnaces, etc.)

3. Add mobs and animals

4. Implement day/night cycle

5. Add multiplayer support

6. Create more advanced modding API

7. Add sound effects and music

8. Implement Redstone-like mechanics

> This is a fully functional foundation for a 2D Minecraft clone that you can expand upon. The architecture is modular and extensible, making it easy to add new features.
