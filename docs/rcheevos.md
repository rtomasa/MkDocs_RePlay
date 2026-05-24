# RetroAchievements

RePlay includes RetroAchievements support for compatible libretro cores and games. When enabled, RePlay can identify supported games, log in to your RetroAchievements account, unlock achievements in Softcore, show achievement and leaderboard activity in the in-game overlay, browse achievements and leaderboards from the running-game menu, and keep routine communication with the RetroAchievements servers while you play.

Hardcore mode is not supported in the current public build.

## Abbreviations

- `RA`: RetroAchievements
- `LB`: Leaderboard
- `PTS`: Points

## Requirements

- An active internet connection.
- A RetroAchievements account.
- A supported system, core, and game image recognized by RetroAchievements.
- Correct game files. If a game is not recognized by RetroAchievements, achievements and leaderboards will not be available for that game.

## Setup

RetroAchievements is configured from RePlay's `ACHIVEMENTS` settings and account fields:

| Setting | Description |
| --- | --- |
| `RETROACHIEVEMENTS` | Enables or disables RetroAchievements support. |
| `RA ENCORE` | Allows already-earned achievements to trigger again locally. |
| `RA SPECTATOR` | Loads RetroAchievements data without submitting unlocks or leaderboard scores. |

The RetroAchievements username and password are file-only settings. Add them manually to `replay.cfg` using these entries:

```cfg
rcheevos_username  = "your_username"
rcheevos_password  = "your_password"
```

The configuration file is located at `/media/sd/config/replay.cfg`. If you are editing over SSH, stop RePlay before modifying the file:

```sh
systemctl stop replay.service
```

If you are editing the SD card from a PC, open the **replay** partition and edit `config\replay.cfg`.

Mode changes should be made before loading a game. `RETROACHIEVEMENTS`, `RA ENCORE`, and `RA SPECTATOR` are applied when a game is loaded, so restart the game after changing them.

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
- Softcore achievement unlocks.
- Encore mode.
- Spectator mode.
- Achievement unlock notifications.
- Challenge, measured-progress, and leaderboard runtime indicators.
- Game mastered and subset completed notifications.
- User avatar, game badge, and achievement badge images in the RetroAchievements overlay when image downloads are available.
- Dedicated achievements browsing in the in-game UI.
- Dedicated leaderboards browsing in the in-game UI.
- Leaderboard list and detail browsing with online score fetching.
- Leaderboard result notifications when the RetroAchievements runtime reports a submitted score result.
- RetroAchievements server error, offline, reconnect, login, and memory-load notifications.
- Multi-disc or multi-media validation when the core exposes the new media path.
- Save-state progress pairing for Softcore play.

RePlay currently does not support Hardcore mode. Unofficial achievements are disabled.

## Achievements And Leaderboards UI

When a supported game is running, the game menu includes separate `ACHIEVEMENTS` and `LEADERBOARDS` entries. These are separate views.

### Achievements View

The achievements browser shows a dedicated achievements list and detail view for the current game.

- The main view shows the unlocked count, total points, Softcore status, and the achievement list.
- The list shows status, point value, and short flags for measured and trigger achievements.
- The bottom info line shows selected achievement status, points, flags, progress, or subset information when available.
- The detail view shows status, points, achievement type, Softcore status, flags, progress, subset name, and description.
- Measured progress updates while the achievements menu is open.
- Unlocks refresh the achievements list so totals, status, and ordering stay current.
- The selected achievement is preserved when the list refreshes.
- The achievements list is built from data already loaded by the RetroAchievements client, so moving through it is typically fast.

### Leaderboards View

The leaderboards browser is a dedicated UI for the running game's RetroAchievements leaderboards.

- The main view shows the leaderboard list for the current game.
- The main view header shows `YOUR POSITION` and `YOUR SCORE` for the selected leaderboard when available.
- The list shows each leaderboard state and title.
- The bottom info line shows the selected leaderboard state and live tracker value when available.
- The detail view shows state, score order, live tracker value, your position, your score, the leaderboard description, and the top scores list.
- The detail score list is limited to the top 100 ranks for the selected leaderboard.
- The detail score list is paged at 7 scores per page.
- `UP` and `DOWN` change the selected leaderboard.
- Page controls move by list page in the main leaderboard view and by score page in the detail view.

Because `YOUR POSITION`, `YOUR SCORE`, and the paged score list require RetroAchievements server data, moving between leaderboards or score pages can briefly pause while the request completes.

### Menu Reopen Behavior

The achievements and leaderboards views behave like the other running-game menus when the UI is hidden and reopened.

- Closing the UI while inside achievements or leaderboards resumes gameplay.
- Reopening the UI returns to the same achievements or leaderboards view.
- Selection and detail state are preserved for that hide and reopen path.
- Normal back or cancel navigation returns to the game options menu and resets the submenu path.

## On-Screen Overlay

RePlay uses a dedicated RetroAchievements overlay instead of the standard small info message area for RA activity. The overlay can show a login summary, notice queue, active challenge icons, active leaderboard trackers, and badge images when they are available.

Common overlay notices include:

| Notice | Meaning |
| --- | --- |
| `Welcome back <user>` | Login and game summary after loading RetroAchievements data. |
| `Achievement Unlocked` | An achievement was unlocked. |
| `Achievement Progress` | A measured achievement reported progress. |
| `Challenge Failed` | A challenge achievement failed or was hidden before unlocking. |
| `Game Mastered` | All core achievements for the game were earned. |
| `Subset Completed` | All achievements in a subset were earned. |
| `Leaderboard Started` | A leaderboard attempt started. |
| `Leaderboard Failed` | A leaderboard attempt failed. |
| `Leaderboard Submitted` | A leaderboard score was submitted. |
| `Leaderboard Best` | The submitted score is now the best returned score. |
| `Leaderboard Rank` | A submitted score returned rank information. |
| `RA OFFLINE` | A request could not be completed and is pending. |
| `RA RECONNECTED` | Pending requests were completed. |
| `RA LOGIN FAILED` | Login failed. Check your account details. |
| `RA NOT AVAILABLE` | The loaded game was not recognized or has no usable RA data. |
| `RA MEMORY FAILED` | The core did not expose usable memory for RetroAchievements after the retry window. |
| `RA MEDIA FAILED` | RetroAchievements could not validate changed media. |
| `RA LB NOT AVAILABLE` | No leaderboards are available for the current game. |
| `RA LB LOAD FAILED` | Leaderboard score data could not be loaded. |

Notices stay visible for at least 6 seconds. The overlay tracks up to 4 active challenges, 4 active leaderboard trackers, 4 active measured-progress achievements, and 5 queued notices. When the notice queue is full, older notices can be dropped to keep newer activity visible.

The overlay uses a compact info font and can resize or change its notice layout based on the active screen area so achievement names, leaderboard names, and tracker values remain readable.

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
| Normal Softcore play | Off | Off | Standard Softcore RetroAchievements behavior. New achievements can unlock normally on the server. |
| Replay already-earned achievements | On | Off | Previously earned achievements can trigger locally again. New achievements can still unlock normally on the server. |
| Safe test mode | Off | On | Local-only testing. No achievement unlocks or leaderboard entries are submitted. |
| Repeat local testing of earned achievements | On | On | Best for repeated local testing. Nothing is submitted to the server, and previously earned achievements may trigger again locally depending on the runtime state loaded for the session. |

## Hardcore Mode

Hardcore mode is currently disabled in RePlay's public build.

- The `RA HARDCORE` option is hidden from the `ACHIVEMENTS` menu.
- `rcheevos_hardcore` is ignored if it is manually added to `replay.cfg`.
- RePlay reports RetroAchievements sessions as Softcore.
- Loading save states is not blocked by RetroAchievements because Hardcore never becomes active.
- Hardcore-only leaderboard behavior should not be expected.

Some Hardcore safety checks remain in the code path for future use, including disallowed core option checks, pause checks, and media-change validation responses. They do not enable Hardcore in the current public build.

## Save States And Progress

RePlay saves RetroAchievements runtime progress with save states during Softcore play. When loading a save state, RePlay restores the matching RetroAchievements progress when available. If matching progress is missing, the RetroAchievements runtime is reset to avoid carrying invalid progress forward.

Because Hardcore is disabled, save-state loading is allowed.

## Cheats And Core Options

RePlay does not provide a frontend cheat system, rewind, slowdown, frame advance, debugger windows, or recorded input playback.

Some libretro cores expose their own cheat or hack options. RePlay keeps checks for the RetroAchievements libretro disallowed setting list and known cheat or gameplay-altering options, including MAME cheat settings and Reicast widescreen cheat or hack settings. These checks are retained for Hardcore support but do not make Hardcore available in the current public build.

Upscaling and normal video output changes are not treated as cheats by RePlay.

## Pause Behavior

When RePlay's menu actually pauses the running game, RePlay stops calling the RetroAchievements frame processor and calls the RetroAchievements idle processor instead. This keeps the player listed as active and allows pending communication with the server to continue.

Hardcore pause-spam restrictions are not active because Hardcore is disabled.

## Leaderboards

Leaderboards are processed by the RetroAchievements runtime while gameplay is running, and RePlay provides a dedicated `LEADERBOARDS` browser in the running game's menu.

In the current RePlay implementation:

- Spectator mode does not submit leaderboard scores.
- RePlay can display submitted score and rank information when the runtime returns a leaderboard scoreboard event.
- Runtime notifications are shown for leaderboard start, fail, submit, tracker, and scoreboard states.
- The detail browser is capped to the top 100 ranks, shown 7 scores per page.
- Some leaderboard browser fields are fetched online on demand, so changing leaderboards or score pages can briefly pause.
- Hardcore-only leaderboard submission should not be expected while Hardcore support is disabled.

## Multi-Disc And Multi-Media Games

For systems that support changing discs or media, RePlay notifies RetroAchievements when media is changed, as long as the core exposes the new media path.

If the new media is recognized, play continues normally. If validation fails, RePlay shows `RA MEDIA FAILED`. If RetroAchievements reports that Hardcore was disabled during media validation, RePlay shows `RA HARDCORE OFF`, although Hardcore is not enabled in the current public build.

## Network Handling

Login, game loading, unlocks, pings, badge image downloads, and leaderboard requests use RePlay's RetroAchievements network path. Temporary connection failures can be retried by the RetroAchievements client. Server errors that cannot be retried are shown to the player.

If RePlay cannot initialize network support, RetroAchievements network calls are disabled for that run.

The achievements browser mainly uses data that is already loaded into the RetroAchievements client for the current game. The leaderboard browser also needs on-demand server requests for user rank, user score, and paged score entries, so it can feel less immediate when changing selection.

## Current Limitations

- Hardcore mode is not supported in the current public build.
- RetroAchievements requires internet access for login, game loading, unlock submission, badge image downloads, leaderboard browsing data, and any leaderboard submission handled by the runtime.
- Only official achievements are enabled.
- Leaderboard browsing is limited to the first 100 ranks of each leaderboard.
- Leaderboard detail pages show 7 scores at a time.
- Some leaderboard browser header fields are fetched online on selection changes, so short pauses are expected there.
- Gameplay overlay indicators are limited to 4 active challenges, 4 active leaderboard trackers, 4 active measured-progress achievements, and 5 queued notices.
- Rich Presence is processed by RetroAchievements when present, but RePlay does not currently show a dedicated Rich Presence panel.
- Media-change validation depends on the libretro core exposing the changed media path.
