# Insider Replays

RePlayOS v2 includes experimental input recording and playback for authenticated Insiders. A replay stores an initial save state and the game's input sequence; it is not a video capture. A compatible core must support reliable save states.

## Record a game

1. Start a supported game and open its in-game menu.
2. Select `Record`. RePlay closes the menu and begins recording from the current game state.
3. Play normally. Opening the in-game menu again stops the recording. RePlay finishes saving it in the background before it becomes available for playback.

Saved files use the `.rplm` extension under `replays/<system>/` on the selected data location. The `replays` folder is created for an authenticated Insider. If `DATA LOCATION` is set to `LOCAL SD`, recordings remain on the SD card even when ROMs are on another storage unit.

## Play a recording

Open `Replays` from the main system list, choose the system, and select a recording. RePlay loads the referenced game and restores its initial state before replaying input. `REPLAY OPTIONS > VISIBILITY > SHOW REPLAYS` controls whether this list is shown. Playback needs the original game path and matching core options; RePlay refuses playback when the recorded and current core options differ.

## Restrictions

- Recording and playback are unavailable while RetroAchievements is active or a Link Play peer is connected.
- Some cores have unreliable or incomplete save states and are excluded. RePlay reports when recording is unsupported for the running game.
- Recordings are written to disk through a bounded memory queue. If storage cannot keep up or a write fails, RePlay stops the recording and reports the error.
- This experimental feature requires a valid Insider token. The `Replays` browser and `Record` command are hidden without one.
