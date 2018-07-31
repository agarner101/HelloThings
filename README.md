# HelloThings
An intro to Android Things with Raspberry Pi

![alt text](https://i.imgur.com/P26mpQM.png)

## Requirements
##### 1. Computer with [Android Studio](https://developer.android.com/studio/) installed
##### 2. Raspberry Pi 3 Model B
- Can be found on [Adafruit](https://www.adafruit.com/product/3055)
- At time of writing (7-31-18) Pi 3 model **B+** is *NOT* supported
##### 3. Micro SD Card
- 8GB or larger
- Also needs adapter or dongle to connect to computer
##### 4. Monitor and Keyboard
- For GUI use when Pi is set up
- Can optionally be set up via terminal only
##### 5. (Optional) Ethernet Cable
- To connect Pi to your network
- Can connect via wifi instead

### Usage Guide
##### 1. Go to [Android Things Console](https://partner.android.com/things/console)
1. Sign up with your preferred gmail account
2. Accept terms and conditions
##### 2. Download Setup Utility CLI Tool
1. Click top-left hamburger menu and select **Tools**
2. Under **Setup Utility** click **Download**
##### 3. Run Setup Utility
On your development machine:
``` $ sudo ./android-things-setup-utility-macos ```
Select the following prompts as they appear:

1. `1 - Install Android Things and optionally set up Wi-Fi`
2. `1 - Raspberry Pi 3`
3. `1 - Default image: Used for development purposes ...`

Insert your SD card into your computer so that the Android Things image can be put on card. Press Enter to run Etcher CLI. This may take a few minutes.

Note: If a dialog appears that says **"The disk you inserted was not readable by this computer"**, this can be safely ignored.

Once complete, there are different options for connecting your Pi. Setup can be achieved via setup utility-only, but for this tutorial we will use the GUI way.

##### 4. GUI Setup
Using Requirements #4 above.
1. Connect Pi to Monitor/TV via HDMI for display
2. Connect Keyboard to Pi via USB for input
3. Connect Micro-USB cable to Pi for power
4. Download [Android Things Toolkit](https://play.google.com/store/apps/details?id=com.google.android.things.companion) from Play Store
5. Follow app instructions to set up

If everything is set up properly, the Android Things Dashboard should show:
![alt text](https://i.imgur.com/zmLIviK.png)

##### 4. Connect to Pi via ADB
Note the IP address shown on the dashboard. If there is no connection, go into the network settings to attempt wired connection, or check that ethernet cable is connected if opting for a wired connection. Ensure that computer is connected to the same network.

ADB Connect: (Replace <Your-Pi-IP> with the IP shown on the Android Things dashboard)
``` $ adb connect <Your-Pi-IP>:5555 ```

If successful, the following should appear:
``` connected to <Your-Pi-IP>:5555```

Connection can again be checked with:
``` $ adb devices```
Which will show:
``` 
List of devices attached
<Your-Pi-IP>:5555	device
```

##### 5. Run HelloThings app on Pi
1. Open HelloThings app in Android Studio
2. Run App -- **Run** > **Run App**
3. Select **Google Iot_rpi3**

##### Results
![alt text](https://i.imgur.com/P26mpQM.png)
