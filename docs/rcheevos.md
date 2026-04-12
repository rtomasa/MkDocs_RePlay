# RetroAchievements

RePlay includes RetroAchievements support for compatible libretro cores and games. When enabled, RePlay can identify supported games, log in to your RetroAchievements account, unlock achievements, process Hardcore mode, submit leaderboard scores, browse achievements and leaderboards in the in-game UI, and keep routine communication with the RetroAchievements servers while you play.

## Requirements

- An active internet connection.
- A RetroAchievements account.
- A supported system, core, and game image recognized by RetroAchievements.
- Correct game files. If a game is not recognized by RetroAchievements, achievements and leaderboards will not be available for that game.

## Setup

RetroAchievements is configured from RePlay's `ONLINE` settings and account fields:

| Setting | Description |
| --- | --- |
| `RETROACHIEVEMENTS` | Enables or disables RetroAchievements support. |
| `RA USERNAME` | Your RetroAchievements username. |
| `RA PASSWORD` | Your RetroAchievements password. |
| `RA HARDCORE` | Enables Hardcore mode when a game is loaded. |
| `RA ENCORE` | Allows earning achievements again even if they were already unlocked. |
| `RA SPECTATOR` | Loads RetroAchievements data without submitting unlocks or leaderboard scores. |

The RetroAchievements username and password are file-only settings. Add them manually to `replay.cfg` using the `rcheevos_username` and `rcheevos_password` entries:

```cfg
rcheevos_username  = "your_username"
rcheevos_password  = "your_password"
```

The configuration file is located at `/media/sd/config/replay.cfg`. If you are editing over SSH, stop RePlay before modifying the file:

```sh
systemctl stop replay.service
```

If you are editing the SD card from a PC, open the **replay** partition and edit `config\replay.cfg`.

Mode changes should be made before loading a game. If a setting says it requires a restart or reload, restart the game before expecting the change to apply.

## Website Hi-Score Visibility

To show your RetroAchievements hi-scores on the RGB-Pi or RePlayOS websites, set your RetroAchievements user motto to one of these values:

- `RePlayOS`
- `RGB-Pi`

You can change it from the RetroAchievements website:

`Settings` > `Profile` > `User Motto`

## What RePlay Supports

RePlay currently supports:

- Game identification through RetroAchievements.
- Login using your RetroAchievements username and password.
- Official achievements.
- Softcore achievement unlocks when Hardcore is off.
- Hardcore achievement unlocks when Hardcore is on and allowed.
- Encore mode.
- Spectator mode.
- Achievement unlock notifications.
- Game mastered and subset completed notifications.
- Dedicated achievements browsing in the in-game UI.
- Dedicated leaderboards browsing in the in-game UI.
- Leaderboard score submission in Hardcore mode.
- Leaderboard result notifications showing score and rank.
- Leaderboard browsing with separate list and detail views.
- Current leaderboard tracker display in the leaderboard detail view.
- RetroAchievements server error, offline, and reconnect notifications.
- Multi-disc or multi-media validation when the core exposes the new media path.
- Save-state progress pairing for Softcore play.

Unofficial achievements are currently disabled.

## Achievements And Leaderboards UI

When a supported game is running, the game menu includes separate `ACHIEVEMENTS` and `LEADERBOARDS` entries. These are separate views. The leaderboard browser is not combined with the achievements browser.

### Achievements View

The achievements browser shows a dedicated achievements list and detail view for the current game.

- The main view shows the unlocked count, total points, Hardcore status, and the achievement list.
- The achievements list is built locally when the view opens, so moving through it is typically very fast.

### Leaderboards View

The leaderboards browser is a dedicated UI for the running game's RetroAchievements leaderboards.

- The main view shows the leaderboard list for the current game.
- The main view header also shows `YOUR POSITION` and `YOUR SCORE` for the currently selected leaderboard when available.
- The detail view shows the leaderboard state, score order, live tracker value, your position, your score, the leaderboard description, and the top scores list.
- The detail score list is currently limited to the top 100 ranks for the selected leaderboard.
- The detail score list is paged at 7 scores per page.
- `UP` and `DOWN` change the selected leaderboard.
- In detail view, `LEFT` and `RIGHT` page through the selected leaderboard's scores.

Because `YOUR POSITION`, `YOUR SCORE`, and the paged score list require RetroAchievements server data, moving between leaderboards or score pages can briefly pause while the request completes.

## On-Screen Messages

RePlay displays short messages for the most important RetroAchievements events:

| Message | Meaning |
| --- | --- |
| `RA x/y \| PTS x/y` | Game summary after loading RetroAchievements data. |
| Achievement title | An achievement was unlocked. |
| `GAME MASTERED` | All achievements for the game were earned. |
| `SUBSET COMPLETED` | All achievements in a subset were earned. |
| `RA LB <score> #<rank>/<total>` | A leaderboard score was submitted and ranked. |
| `RA LB BEST <score> #<rank>/<total>` | The submitted score is now your best returned score. |
| `RA OFFLINE` | A request could not be completed and is pending. |
| `RA RECONNECTED` | Pending requests were completed. |
| `RA LOGIN FAILED` | Login failed. Check your account details. |
| `RA HARDCORE OFF` | Hardcore was disabled for safety or validation reasons. |
| `RA MEDIA FAILED` | RetroAchievements could not validate changed media. |

Abbreviations:

- `RA`: RetroAchievements
- `LB`: Leaderboard
- `PTS`: Points

## Encore Mode

`RA ENCORE` reactivates achievements that you have already earned, allowing them to trigger again locally during play.

When Encore mode is on:

- Previously earned achievements can show notifications again.
- Replaying a game can feel like earning the set again.
- The same achievement is not granted again on the RetroAchievements website.
- Points are not awarded again for achievements already earned.

Encore mode is not an offline test mode by itself. If `RA SPECTATOR` is off, achievements you have never earned before can still be submitted normally.

In RePlay, Encore mode is applied when the game is loaded. After changing `RA ENCORE`, reload the game.

## Spectator Mode

`RA SPECTATOR` keeps RetroAchievements processing active locally without submitting unlocks or leaderboard entries to the RetroAchievements server.

When Spectator mode is on:

- Achievement logic still runs locally.
- Local notifications can still appear.
- Achievement unlocks are not submitted to the server.
- Leaderboard entries are not submitted to the server.

Spectator mode is useful for safe testing, repeated checks, and verifying notifications or runtime behavior without affecting your account.

In RePlay, Spectator mode is applied when the game is loaded. After changing `RA SPECTATOR`, reload the game.

## Mode Combinations

| Use case | `RA ENCORE` | `RA SPECTATOR` | Behavior |
| --- | --- | --- | --- |
| Normal play | Off | Off | Standard RetroAchievements behavior. New achievements can unlock normally on the server. |
| Replay already-earned achievements | On | Off | Previously earned achievements can trigger locally again. New achievements can still unlock normally on the server. |
| Safe test mode | Off | On | Local-only testing. No achievement unlocks or leaderboard entries are submitted. |
| Repeat local testing of earned achievements | On | On | Best for repeated local testing. Nothing is submitted to the server, and previously earned achievements may trigger again locally depending on the runtime state loaded for the session. |

## Hardcore Mode

Hardcore mode follows the RetroAchievements restrictions expected by the official runtime.

When Hardcore mode is active:

- Loading save states is blocked.
- Saving save states is allowed.
- Leaderboard scores can be submitted.
- Pause spam is restricted.
- Disallowed core options, cheats, or gameplay-altering hacks can disable Hardcore.

If you try to load a save state while Hardcore is active, RePlay shows `DISABLE RA HARDCORE` and does not load the state.

Saving a state is still allowed. RePlay also saves RetroAchievements runtime progress with the save state. When loading a save state outside Hardcore mode, RePlay restores the matching RetroAchievements progress when available. If matching progress is missing, the RetroAchievements runtime is reset to avoid carrying invalid progress forward.

## Automatic Hardcore Disable

RePlay can automatically disable Hardcore in these cases:

- The loaded game has no RetroAchievements functionality, meaning no achievements, no leaderboards, and no rich presence.
- A core option is detected that RetroAchievements marks as disallowed for Hardcore.
- A known cheat or widescreen hack option is enabled.
- Changed disc or media cannot be recognized by RetroAchievements while Hardcore is active.

When Hardcore is automatically disabled because the loaded game has no RetroAchievements functionality, RePlay restores the configured Hardcore setting when the game is unloaded or before the next game is loaded.

## Cheats And Core Options

RePlay does not provide a frontend cheat system, rewind, slowdown, frame advance, debugger windows, or recorded input playback.

Some libretro cores expose their own cheat or hack options. RePlay checks the RetroAchievements libretro disallowed setting list and also blocks known cheat or gameplay-altering options, including MAME cheat settings and Reicast widescreen cheat or hack settings. If one of these settings is enabled while Hardcore is requested, Hardcore is disabled and RePlay shows `RA HARDCORE OFF`.

Upscaling and normal video output changes are not treated as cheats by RePlay.

## Pause Behavior

When RePlay's menu actually pauses the running game, RePlay stops calling the RetroAchievements frame processor and calls the RetroAchievements idle processor instead. This keeps the player listed as active and allows pending communication with the server to continue.

In Hardcore mode, RePlay asks RetroAchievements whether pausing is currently allowed. If the pause happens too soon after the previous pause, RePlay refuses the pause and shows `RA PAUSE WAIT` or `RA PAUSE WAIT <seconds>S`.

## Leaderboards

Leaderboards are processed automatically while gameplay is running. No separate user action is needed to submit a valid score.

In the current RePlay implementation:

- Leaderboard scores submit only in Hardcore mode.
- Spectator mode does not submit leaderboard scores.
- RePlay displays the submitted score and rank after the server returns the leaderboard result.
- RePlay provides a dedicated `LEADERBOARDS` browser in the running game's menu.
- The leaderboard browser has a list view and a separate detail view.
- The detail view shows the live tracker value when the leaderboard is actively tracking.
- The detail browser is currently capped to the top 100 ranks, shown 7 scores per page.
- Some leaderboard browser fields are fetched online on demand, so changing leaderboards or score pages can briefly pause.

## Multi-Disc And Multi-Media Games

For systems that support changing discs or media, RePlay notifies RetroAchievements when media is changed, as long as the core exposes the new media path.

If the new media is recognized, play continues normally. If the media is not recognized while Hardcore is active, Hardcore is disabled. If validation fails for another reason, RePlay shows `RA MEDIA FAILED`.

## Network Handling

Unlocks, pings, and leaderboard submissions are sent through RePlay's RetroAchievements network path. Temporary connection failures can be retried by the RetroAchievements client. Server errors that cannot be retried are shown to the player.

If RePlay cannot initialize its network support, RetroAchievements network calls are disabled for that run.

The achievements browser mainly uses data that is already loaded into the RetroAchievements client for the current game. The leaderboard browser also needs on-demand server requests for user rank, user score, and paged score entries, so it can feel less immediate when changing selection.

## Current Limitations

- RetroAchievements requires internet access for login, game loading, unlock submission, leaderboard submission, and some leaderboard browsing data.
- Only official achievements are enabled.
- Leaderboard browsing is limited to the first 100 ranks of each leaderboard.
- Leaderboard detail pages currently show 7 scores at a time.
- Some leaderboard browser header fields are fetched online on selection changes, so short pauses are expected there.
- Leaderboard tracker information is shown in the detail view, not as a gameplay overlay.
- Rich Presence is processed by RetroAchievements when present, but RePlay does not currently show a dedicated Rich Presence panel.
- Media-change validation depends on the libretro core exposing the changed media path.
