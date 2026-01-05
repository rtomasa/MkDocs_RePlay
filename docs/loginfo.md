# Logging Information

You can use logs to view key events during RePlay execution and troubleshoot issues with any system core or a specific game.

Steps:
1. Go to `SYSTEM > LOG LEVEL` and set the desired value (for example, INFO).
2. Connect to your Raspberry Pi via SSH.
3. Stop the running process with `pkill replay`.
4. Go to the RePlay system folder: `cd /opt/replay`.
5. Start RePlay with `./replay`.

After doing the above steps, RePlay will run in the foreground and you will see log output in your SSH terminal. To stop it, press `Ctrl + C`.

**Note**: leaving logging enabled when it is not required can slightly impact performance and may briefly show white text on screen when using CRT modes.
