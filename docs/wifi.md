# Wi-Fi Configuration

To configure Wi-Fi on RePlay OS, you can do it using SSH or SFTP very easily.

Here’s how you can configure your Wi-Fi:

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