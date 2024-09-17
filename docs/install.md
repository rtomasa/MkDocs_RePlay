# Installation

First we need to install Replay OS into your MicroSD card.

## Flashing the image

* We suggest you to use [balenaEtcher](https://www.balena.io/etcher/){target=_blank} for flashing the system to the MicroSD card.
Download it from their [official web site](https://www.balena.io/etcher/){target=_blank} and install it.

* Next, download the latest version of RePlay OS from the [Download](./download.md) section.

* Now insert your MicroSD card into your computer and open balenaEtcher. Then, click on **Flash from file**:
![Step 1](img/inst_01.png)

* Navigate to your download folder and select the RePlay OS image file:
![Step 2](img/inst_02.png)

* Next click on **Select target** and select your MicroSD card where the system will be installed:

![Step 3](img/inst_03.png)
![Step 4](img/inst_04.png)

* Finally click on the **Flash!** button and wait until the flashing operation finish:

![Step 5](img/inst_05.png)
![Step 6](img/inst_06.png)

* When the operation completes, you'll see **Flash complete!** and **1 Successful target**.
If the flash fails, try again. If it still fails, your MicroSD card could be broken, so use a different MicroSD card.

* Finally, you can close balenaEtcher, remove the MicroSD card and plug it into your Raspberry device.

## Connect the primary HDMI

**IMPORTANT:** Ensure you are using the primary HDMI port when booting your Raspberry Pi. Using the wrong port will result in a black screen.

![Step 7](img/pi_hdmi_1.png)

## First Boot

When booting your Raspberry Pi for the first time, it will perform some initial operations silently (black screen), such as creating and expanding a new FAT partition on the MicroSD card for storing your ROMs, BIOS, saves, and config files.

Please note that these operations could take some time, so be patient. **DO NOT POWER OFF** the device and wait until the system displays the user interface.

![UI](img/fst_boot.png)

Congratulations! You are now ready for fun!