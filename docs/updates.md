# Software Updates

RePlayOS v2 uses signed OTA packages. Updates are coordinated across the frontend, cores, system files, drivers, kernel, and updater so the installed components remain compatible.

The OTA repository is intentionally `NotAutomatic`; ordinary `apt upgrade` does not install a RePlayOS release.

## Update from the RePlay menu

1. Open `REPLAY OPTIONS > UPDATES`.
2. Choose `STABLE` for normal releases or `TESTING` for pre-release builds.
3. Select **CHECK FOR UPDATES**.
4. When an update is available, select **INSTALL UPDATE AND REBOOT**.

The check and download run in the background. The update is not installed while the frontend is running: RePlay reboots into a dedicated offline update environment, installs the cached packages, and then boots normally. Do not remove power during the update or reboot.

Update actions are unavailable while another update operation or a scheduled transaction is active. If an interrupted installation needs recovery, RePlayOS keeps the frontend stopped and exposes the recovery state so it can be diagnosed over SSH.

## Advanced terminal workflow

The same signed updater can be used from an SSH session as `root`:

```sh
replay-updater check
replay-updater status
replay-updater prepare
replay-updater apply
```

`prepare` validates the release, downloads the exact package set, and schedules the offline transaction. `apply` only requests the reboot; package installation happens during the offline boot.

For a one-time upgrade from updater version 2.0.7 or older, use `replay-updater prepare --reboot`, or run `systemctl reboot` after `prepare`. Do not use the old client's `apply` command for that migration because it can install packages while the system is live.

## Back up first

OTA updates preserve the separate `replay` data partition, but updates are not a backup. Keep a copy of important ROMs, BIOS files, saves, captures, skins, and configuration before updating.
