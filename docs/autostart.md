# Autostart Games

RePlayOS can automatically launch one game on startup using the `roms/_autostart` folder.

Favorites and recents are stored as small reference files:

- `roms/_favorites/*.fav`
- `roms/_recent/*.rec`

Both file types work the same way: each one points to the original game ROM. To use one for autostart, copy the desired `.fav` or `.rec` file into `roms/_autostart`.

Only keep one file inside `roms/_autostart`. On the next boot, RePlayOS will read that file and automatically launch the referenced game.