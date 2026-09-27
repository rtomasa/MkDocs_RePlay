# Gamepad Configuration

RePlay is designed to work without manual gamepad configuration. It includes the official SDL controller database with profiles for more than **700** controllers. Most XInput-compatible USB and 2.4 GHz controllers should work immediately, although rumble support depends on the controller and driver.

RePlay handles input in three separate layers:

- **Physical mapping** tells SDL which physical control is South, East, L1, R3, a stick axis, and so on. This is normally supplied by the built-in database.
- **Player assignment** connects a particular controller to `PLAYER 1`–`PLAYER 6`.
- **Game mapping** decides what each assigned player's controls do in the running system or game.

Game mappings never change the controls used to navigate the RePlay UI.

## Player Assignment

Connected controllers are automatically placed in the first available player slots. View or change them under `REPLAY OPTIONS > INPUT`.

To assign a controller manually:

1. Open the required `PLAYER` slot.
2. Select `ASSIGN CONTROLLER`.
3. Press a button on the controller you want in that slot.

Assignments are saved automatically. RePlay identifies distinguishable controllers independently of Raspberry Pi USB numbering, so swapping USB sockets or restarting should not swap players. If the destination slot is occupied, that controller moves to the first free slot. Disconnecting one controller does not renumber the others, and a newly connected controller uses the first available unreserved slot.

Identical controllers without unique serial numbers may need to use their physical USB connection to distinguish them. Select `RESET PLAYER ASSIGNMENTS` to forget all saved assignments and place currently connected controllers in connection order again.

Each Player menu also provides `PHYSICAL MAPPING`, `TEST CONTROLLER`, and `TEST RUMBLE`. See [Physical Controller Mapping](mappings.md) before changing a physical mapping.

RePlayOS includes a custom `ps3-usb-autopair` driver preinstalled. To pair a genuine PS3 Sixaxis or DualShock 3 controller, connect it to the Raspberry with a USB data cable. After pairing, disconnect USB and press the PS button to reconnect wirelessly.

## Mapping Controls for a System or Game

Open the running game's menu and select `INPUT`, then open a Player entry. Each Player provides:

- **Device type** selects the emulated controller type supported by the system.
- **Game port** selects which in-game player that input port controls. Values are shown as `P1`–`P6`; this also supports special layouts such as forwarding a second stick to Player 1.
- **Control mappings** assign the system's named inputs to SDL buttons or axes. Select a value from the list, or choose `PRESS A BUTTON` and operate the required control on that Player's assigned controller.

Changes apply immediately to the running game. `PRESS A BUTTON` waits for the initiating button to be released, ignores other controllers, and returns to the Player menu after capturing the new input.

## Saving Game Mappings

An unsaved mapping remains active until another game is opened. Save it from the same `INPUT` menu at the required scope:

- `SAVE SYSTEM INPUT` applies to every game in the current system.
- `SAVE FOLDER INPUT` applies to games in the current ROM subfolder and its subfolders. It is available only when the game is inside a subfolder.
- `SAVE GAME INPUT` applies only to the current game.

RePlay loads one complete input profile using this priority: **Game → nearest Folder → System → Default**. The `INPUT MAPPING` row shows which scope is active. The matching `REMOVE ... INPUT` commands remove saved profiles.

Each profile stores the mappings for all six Player ports together. It does not depend on having the same controllers connected later, so disconnecting one controller does not reset mappings for the remaining players. LCD and CRT input profiles are stored separately.

**Bluetooth controllers are not supported out of the box, except for the PS3 controllers described above.** USB or 2.4 GHz controllers are recommended; an 8BitDo Bluetooth adapter can be used when Bluetooth support is required.

## Default UI Button Mapping

| Button                                  | Description    |
| --------------------------------------- | -------------- |
| <kbd>Up</kbd> <kbd>Down</kbd>           | Used for moving up and down through the menus |
| <kbd>Left</kbd> <kbd>Right</kbd>        | Used for jumping forward and backward through the menu pages |
| <kbd>L</kbd> <kbd>R</kbd>               | Used for jumping forward and backward to the next letter through the menu pages |
| <kbd>North</kbd>                        | Used for adding favorites |
| <kbd>South</kbd>                        | Used to navigate to the previous menu or screen |
| <kbd>East</kbd>                         | Used for starting games, choosing options, and accessing menus |
| <kbd>West</kbd>                         | Used for displaying game captures (when available) |
| <kbd>Select</kbd>                       | Used for removing favorites and recents |
