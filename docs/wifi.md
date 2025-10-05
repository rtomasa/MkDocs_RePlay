# Wi-Fi Configuration

RePlay OS supports WPA2, WPA3, and Transition mode. Configure it in either way below.

## Option 1: RePlay config (SD card)

1. Insert the SD card in your computer.
2. Open the **replay** FAT partition and edit `config\replay.cfg`.
3. Set:

```cfg
wifi_name    = "MyWifi"
wifi_pwd     = "********"
wifi_country = "ES"           # ISO 3166 code (e.g., ES, US, DE)
wifi_mode    = "transition"   # wpa3 | wpa2 | transition
wifi_hidden  = "false"        # "true" if SSID is hidden
```

Notes:

* `transition` works on mixed WPA2/WPA3 SSIDs.
* Use `wpa3` for WPA3-only APs.
* Use `wpa2` for WPA/WPA2 APs. If your AP requires TKIP, select `wpa2` and enable TKIP on the router.
* Refer to the full list of valid country codes here: [ISO 3166 Country Codes](https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes).

## Option 2: RePlay config (Ethernet)

Use the same fields and notes as in **Option 1**. Edit the live config over SSH.

Steps:

1. Connect the Pi via Ethernet and SSH in: `ssh root@<ip-or-hostname>`  (password: `replayos`)
2. Stop RePlay to release the config: `pkill replay`
3. Edit the file on the SD card: `nano /media/sd/config/replay.cfg`
4. Save, flush, and reboot:

   ```
   sync
   reboot
   ```

## Option 3: Manual Linux config

1. Connect the Pi via Ethernet and SSH in: `ssh root@<ip-or-hostname>`  (password: `replayos`)
2. Edit: `nano /etc/wpa_supplicant/wpa_supplicant-wlan0.conf`
3. Paste the profile that fits your network.

### WPA3-Personal (SAE)

```cfg
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=ES

network={
    ssid="YourNetworkName"
    psk="YourNetworkPassword"
    key_mgmt=SAE
    proto=RSN
    pairwise=CCMP
    group=CCMP
    ieee80211w=2
}
```

### WPA2/WPA3 Transition

```cfg
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=ES

network={
    ssid="YourNetworkName"
    psk="YourNetworkPassword"
    key_mgmt=WPA-PSK SAE
    proto=RSN
    pairwise=CCMP
    group=CCMP
    ieee80211w=1
}
```

### WPA2-Personal (secure default)

```cfg
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=ES

network={
    ssid="YourNetworkName"
    psk="YourNetworkPassword"
    key_mgmt=WPA-PSK
    proto=RSN
    pairwise=CCMP
    group=CCMP
}
```

### WPA/WPA2 legacy with TKIP (only if required by AP)

```cfg
network={
    ssid="YourNetworkName"
    psk="YourNetworkPassword"
    key_mgmt=WPA-PSK
    proto=WPA RSN
    pairwise=CCMP TKIP
    group=CCMP TKIP
}
```

4. Hidden SSID: add `scan_ssid=1` inside `network{}`.
5. Apply without reboot:

```sh
ip link set wlan0 up
systemctl try-reload-or-restart wpa_supplicant@wlan0.service || wpa_cli -i wlan0 reconfigure
wpa_cli -i wlan0 reassociate
```

## Verify and troubleshoot

* Status: `wpa_cli -i wlan0 status`
* IP: `ip addr show wlan0`
* Scan: `wpa_cli -i wlan0 scan && sleep 2 && wpa_cli -i wlan0 scan_results`

## Router & Access point tips

* WPA2: set **WPA2-PSK + AES/CCMP**. Avoid **Auto** and TKIP.
* WPA3: enable **WPA3-Personal (SAE)** with **PMF required**.
* Set the correct `country` for proper channel use.
