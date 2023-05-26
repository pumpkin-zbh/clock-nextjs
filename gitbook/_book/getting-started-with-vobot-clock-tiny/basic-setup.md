# Basic Setup

## Setup

1. Connect your Phone/Tablet/Laptop/PC to the wireless hotspot (AP) displayed on the screen.

<figure><img src="./images/设置-1.jpg" alt=""><figcaption></figcaption></figure>

2. Visit the IP address shown on the screen with your Phone/Tablet/Laptop/PC IP Address: http://10.9.8.7/

<figure><img src="./images/设置-2.jpg" alt=""><figcaption></figcaption></figure>

3. Select the Wi-Fi SSID you prefer to connect the device to. (Note: Support 2.4 GHz Hotpot Only)
4. Fill the Wi-Fi password of the Wi-Fi SSID that you selected, and other address information needed. (Note: Case-sensitive)
5. Click "Connect to WiFi", and then the device will verify if it can connect to the assigned Wi-Fi, and check if the City/State/Region is Valid. Once the geolocation and time zone information was fetched successfully, the setup is completed.

<figure><img src="./images/设置-3.jpg" alt=""><figcaption></figcaption></figure>

## Button Operation

### Switching UI Pages

* During the normal operation, by short pressing the button, the UI will switch to the next page (plugin). Sometimes it will prompt to hold the button for 0.5 second to confirm an operation.

<figure><img src="./images/设置-4.jpg" alt=""><figcaption></figcaption></figure>

### Restore to Factory Default

* Press and hold the button for about 5 seconds, until the screen shows "Restoring to factory default", and then release the button.

<figure><img src="./images/设置-5.jpg" alt=""><figcaption></figcaption></figure>

### Regular Firmware Update

* On the firmware update page, if the new version is available, you may press and hold the button for about 1 second to enter the network update mode.
* The firmware update needs to connect to a Wi-Fi hotspot, please wait until the screen shows that the update is completed, and the device will automatically reboot.
* If the upgrade process is interrupted or gets stuck, you need to re-plug the power supply to try again.

### Rescue Mode

* In case the system completely crashes (rarely happens), you may use the rescue mode to completely recover to the latest firmware version, here is how:
  * Create a temporary WiFi hotspot: 
    * SSID: factory
    * PassWord: 12345678
  * Unplug the power cord, and right after plug back, immediately press the button and hold it for more than 5 seconds. At this time, it will erase the configuration and existing firmware. Then it connects to the Wi-Fi hotspot and downloads the latest version of firmware.

<figure><img src="./images/设置-6.jpg" alt=""><figcaption></figcaption></figure>

### Advanced

* This device is made of ESP32-C3 chipset. You can DIY your firmware totally by yourself and write it into the device over USB port (USB Serial CDC UART).
* To flash your firmware, press and hold the button first, then plug in the power supply. Then release the button. At this point, the device enters the Download mode.
* However, all firmware and data will get lost in this case, and the rescue mode and OTA feature will no longer be available. 
* We recommend to use Thonny (Python IDE) for beginners to manage the configuration file and write your plugins.
