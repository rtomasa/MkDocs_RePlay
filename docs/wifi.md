# Wi-Fi Configuration

To configure Wi-Fi on RePlay OS, you can do it in two different ways very easily:

## Manual RePlay Configuration

1. Insert the RePlay SD card into your computer.
2. Open the **replay FAT partition** and navigate to `config\replay.cfg`.
3. Edit the file and set the parameters:
```cfg
wifi_name    = "MyWifi"
wifi_pwd     = "********"
wifi_country = "ES"
```
4. Refer to the full list of valid country codes here: [ISO 3166 Country Codes](https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes).

## Manual Linux Configuration

1. SSH into the Raspberry Pi. The credentials are: `root / replayos`.
2. Execute `nano /etc/wpa_supplicant/wpa_supplicant-wlan0.conf` to configure your Wi-Fi:
```cfg
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

country=ES

network={
    ssid="YourNetworkName"
    psk="YourNetworkPassword"
}
```
3. Change `country`, `YourNetworkName` and `YourNetworkPassword` with your Wi-Fi configuration and press `Ctrl+X` to exit (press `Y` and then `Enter` to save and confirm).
4. Reboot the system.

By following these steps, you can easily configure Wi-Fi on RePlay OS.