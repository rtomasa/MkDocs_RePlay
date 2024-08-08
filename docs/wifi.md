# Wi-Fi Configuration

If you want to configure Wi-Fi on a Raspberry Pi without a monitor (headless setup), you can do this via SSH whether by using a text based UI or issuing commands.

Here’s how you can configure your Wi-Fi:

1. SSH into the Raspberry Pi. The credentials are: `root / replayos`.
2. Use `nmtui` or `nmcli` to Configure your Wi-Fi.

## Wi-Fi Configuration Using `nmcli`

To create a persistent Wi-Fi configuration file that NetworkManager will use on boot, you can use `nmcli` to add and modify a connection:

```sh
# Add Wi-Fi connection
nmcli connection add type wifi ifname wlan0 con-name "MyWiFi" ssid "YourSSID"

# Configure Wi-Fi security
nmcli connection modify "MyWiFi" wifi-sec.key-mgmt wpa-psk
nmcli connection modify "MyWiFi" wifi-sec.psk "YourPassword"

# Bring up the connection
nmcli connection up "MyWiFi"
```

## Wi-Fi Configuration Using `nmtui`

### Summary of Steps

1. **Open `nmtui`**: `nmtui`
2. **Navigate to "Activate a connection"**: Use arrow keys and Enter
3. **Select Wi-Fi Network**: Choose your Wi-Fi network
4. **Enter Wi-Fi Password**: Enter the password for the network
5. **Activate Connection**: Wait for the confirmation of connection
6. **Exit `nmtui`**: Navigate to "Quit" and press Enter

### Example Walkthrough

Here's a brief example of what the process looks like in the terminal:

1. **Open `nmtui`**:
   ```sh
   nmtui
   ```
2. **Main Menu**:
```
+-------------------------------------+
|          NetworkManager TUI         |
+-------------------------------------+
|  * Activate a connection            |
|  * Edit a connection                |
|  * Set system hostname              |
|  * Quit                             |
+-------------------------------------+
```
3. **Activate a Connection**:
```
+-------------------------------------+
|        Activate a connection        |
+-------------------------------------+
|  * Wired connection 1               |
|  * MyWiFiNetwork                    |
|  * AnotherWiFiNetwork               |
|  * YetAnotherWiFi                   |
|  * Back                             |
+-------------------------------------+
```
4. **Enter Wi-Fi Password**:
```
+-------------------------------------+
|        Enter Wi-Fi Password         |
+-------------------------------------+
|  SSID: MyWiFiNetwork                |
|  Password: ****************         |
|                                     |
|  <OK>                               |
|  <Cancel>                           |
+-------------------------------------+
```
5. **Connection Activated**:
```
+-------------------------------------+
|          NetworkManager TUI         |
+-------------------------------------+
|  Connection activated successfully  |
|                                     |
|  <Back>                             |
+-------------------------------------+
```
6. **Exit `nmtui`**:
```
+-------------------------------------+
|          NetworkManager TUI         |
+-------------------------------------+
|  * Activate a connection            |
|  * Edit a connection                |
|  * Set system hostname              |
|  * Quit                             |
+-------------------------------------+
```

By following these steps, you can easily configure Wi-Fi on your Raspberry Pi or any Linux system using `nmtui`. This tool provides a straightforward interface for managing network connections without needing to edit configuration files manually or use complex command-line options.