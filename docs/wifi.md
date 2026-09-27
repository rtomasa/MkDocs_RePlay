# Wi-Fi Configuration

RePlayOS v2 uses IWD with `systemd-networkd` and automatically detects the access point's WPA2, WPA3, or transition security mode. The old `wifi_mode` setting is no longer used.

## Configure from the RePlay menu

Open `REPLAY OPTIONS > INFORMATION` and edit the Wi-Fi fields, or use the configuration file method below. `REPLAY OPTIONS > SYSTEM > WI-FI` enables or disables the Wi-Fi adapter immediately and preserves that choice across restarts.

## Configure `replay.cfg`

Edit `/media/sd/config/replay.cfg` from a computer, or over SSH after stopping RePlay:

```cfg
wifi_name    = "MyWifi"
wifi_pwd     = "MyWifiPassword"
wifi_country = "ES"       # ISO 3166 two-letter country code
wifi_hidden  = "false"    # "true" for a hidden SSID
```

The password is protected in the live configuration after it has been applied. The default country on a clean image is `00` (world domain); set the real country before normal use so the permitted channels and transmit power are correct.

For a hidden network, set `wifi_hidden` to `"true"`. No separate WPA2/WPA3 selection is required. IWD chooses the appropriate security method from the access point.

## Verify the connection

From an SSH session, use:

```sh
iw dev
networkctl status
ip addr show wlan0
```

If Wi-Fi is unavailable at boot, RePlay still starts and can be configured later over Ethernet or by editing the SD card. Credentials are runtime data and should not be included in screenshots, logs, or shared configuration files.
