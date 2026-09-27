# Replay Control

**Replay Control** is a companion web app for RePlayOS. It runs alongside RePlayOS on your Raspberry Pi and lets you use a phone, tablet, or computer to explore and control your collection over your local network.

!!! info "Project author"
    Replay Control was created by [Antonio Abad (lapastillaroja)](https://github.com/lapastillaroja){ target=_blank rel="noopener" }. It is not developed by the RePlayOS author.

<div class="companion-showcase">
  <div class="video">
    <iframe
      src="https://www.youtube.com/embed/jUIY4TUs3KE?si=gSX_hIrhXsY634fw"
      title="Replay Control showcase"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      referrerpolicy="strict-origin-when-cross-origin"
      loading="lazy"
      allowfullscreen>
    </iframe>
  </div>
</div>

<div class="companion-actions" markdown>
  [Visit the Replay Control website](https://lapastillaroja.github.io/replay-control/){ .md-button .md-button--primary target=_blank rel="noopener" }
  [View the source code](https://github.com/lapastillaroja/replay-control){ .md-button target=_blank rel="noopener" }
</div>

## What you can do

- Browse and search games across every system, with box art and metadata.
- Launch a game on the RePlayOS TV directly from your browser.
- Organize favorites and manage multi-disc games.
- View manuals, screenshots, related games, and personalized recommendations.
- Manage Wi-Fi, NFS, storage, themes, and selected RePlayOS settings.
- Install the web app on the home screen of a phone or tablet.

## Installation

For the easiest installation, use RePlayOS v1.8.0 or later. Open **EXTRAS** in RePlayOS and run the Replay Control installation script. A matching uninstallation script is available in the same place.

You can also install it through SSH. From a computer on the same network, connect to your Raspberry Pi and run the official installer:

``` sh
ssh root@replay.local
curl -fsSL https://raw.githubusercontent.com/lapastillaroja/replay-control/main/install.sh | bash
```

If `replay.local` cannot be resolved, replace it with the Raspberry Pi's IP address. The installer displays the local address to open when it finishes.

For additional installation modes and troubleshooting, see the [official Replay Control documentation](https://lapastillaroja.github.io/replay-control/){ target=_blank rel="noopener" }.

## First connection

1. Open the address shown by the installer in a modern browser on the same local network.
2. Complete the first-time setup shown by Replay Control.
3. On the RePlayOS TV, open `SYSTEM > OPTIONS` and enable `NET CONTROL`.
4. Open `SYSTEM > INFORMATION` and note the `NET CONTROL CODE`.
5. Enter that code in Replay Control to connect as a normal user.

The Net Control connection enables game launching, Now Playing information, player controls, and favorites. Administrative actions require the RePlayOS device password.

!!! note
    Replay Control uses local HTTPS by default. Your browser may show a certificate warning the first time you open it because the certificate is generated locally for your device.
