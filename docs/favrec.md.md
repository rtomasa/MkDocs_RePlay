# Favorites & Recents

The RePLay frontend provides a powerful and intuitive system to manage your favorite and recently played games, enhancing your gaming experience by allowing quick access to your most frequently enjoyed titles.

## Favorites

### Capabilities and Features

* **Extensions**: Favorites and Recent Games use specific extensions (`.fav`, `.rec`) to differentiate them within the file system.
* **Quick Access**: Easily bookmark your most-loved games to access them quickly from the dedicated Favorites section.
* **Cross-System Support**: Favorites can include games from any supported system within the RePLay frontend, providing a seamless user experience.
* **Customizable Entries**: Users can manually add or remove games from their Favorites, making the list truly personalized.
* **Persistent Storage**: Favorite entries are stored persistently, ensuring that your selections remain available across sessions.

### Management Options

* **Adding to Favorites**: Select a game and mark it as favorite to include it in your personalized list.
* **Removing Favorites**: Effortlessly remove games from your Favorites if your preferences change.
* **Automatic File Management**: Each favorite game is represented as a special `.fav` file, simplifying backend management and maintenance.
* **Customizable Structure**: RePLay allows users to organize their games into personalized folder structures.
* **Nested Folders**: Supports multi-level nested folders, enabling deep customization.
* **Creating and Deleting Folders**: Users can effortlessly create new folders to categorize games and delete unnecessary ones.
* **Drag-and-Drop Management**: Easily move games into and between folders to reorganize your collection swiftly.

## Recent Games

### Capabilities and Features

* **Dynamic Tracking**: Automatically records games you've recently played, providing a convenient way to revisit your latest sessions.
* **Automatic Updates**: The Recent Games list dynamically updates based on your gaming activity.
* **Ordered by Last Played**: Recent entries are sorted by last access time, making it easy to pick up right where you left off.
* **Cross-System Compatibility**: Similar to Favorites, Recent Games span across all supported systems.

### Management Options

* **Automated Entries**: Recent games are automatically added upon game launch, requiring no manual intervention.
* **Update Timestamp**: Automatically updates timestamps when revisiting games, ensuring the most recent plays appear first.
* **Pruning and Organization**: Users can manually remove entries from their Recent Games list to keep it relevant and concise.

## Folder Structure Overview

The RePLay frontend uses two special folders:

* `_favorites`
* `_recent`

These folders are stored at the root of your ROM directory, providing easy and quick access to selected games.

### `_favorites` Folder

The `_favorites` folder contains `.fav` files. Each file represents a favorite game and includes a path pointing to the game's original location. The file naming convention typically includes the system prefix followed by the game name.

**Example Structure:**

```
/_favorites/
  ├── arcade_mame@pacman.fav
  ├── nintendo_snes@super_mario_world.fav
  └── sega_smd@sonic_the_hedgehog.fav
```

### Custom Folder Organization for Favorites

You can further customize your `_favorites` by creating subfolders to organize your games into specific categories.

**Example Custom Structure:**

```
/_favorites/
  ├── Classics/
  │   ├── arcade_mame@pacman.fav
  │   └── sega_smd@sonic_the_hedgehog.fav
  └── Platformers/
      └── nintendo_snes@super_mario_world.fav
```

### `_recent` Folder

The `_recent` folder contains `.rec` files. These represent recently played games and follow a similar format to favorites, storing paths to the game's original location.

**Example Structure:**

```
/_recent/
  ├── sega_cd@sonic_cd.rec
  ├── sony_psx@crash_bandicoot.rec
  └── nintendo_gba@pokemon_emerald.rec
```

In this example, each `.rec` file indicates the game’s location and tracks the timestamp of your last play session, automatically updating its sorting position based on recent activity.

