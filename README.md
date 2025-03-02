# Friend: Open-Source AI Wearable with 24h+ on single charge

Assembled          |  Disassembled
:-------------------------:|:-------------------------:
![CleanShot 2024-03-06 at 17 19 58](https://github.com/BasedHardware/friend/assets/43514161/f333cecb-cab8-481e-ae9b-37b9b742e2c1)| <img src="https://github.com/BasedHardware/friend/assets/43514161/af939aca-1257-4f67-8118-e1a91f2d4949" alt="drawing" width="1200"/>

[![Discord Follow](https://dcbadge.vercel.app/api/server/kEXXsnb5b3?style=flat)](https://discord.gg/kEXXsnb5b3) &ensp;
[![License: GPLv3](https://img.shields.io/badge/license-GPLv3-blue)](https://opensource.org/license/agpl-v3)

Friend is an AI wearable device that records everything you say, gives you proactive feedback and advice. 

## Features

- **Real-Time AI Audio Processing**: Leverage powerful on-device AI capabilities for real-time audio analysis.
- **Low-powered Bluetooth**: Capture audio for 24h+ on a small button battery
- **Open-Source Software**: Access and contribute to the pin's software stack, designed with openness and community collaboration in mind.
- **Wearable Design**: Experience unparalleled convenience with ergonomic and lightweight design, perfect for everyday wear. 

## How it works

```mermaid
graph TD
A[Device] -- Streams Audio --> B[Phone App]
B -- Saves Audio --> C[Phone Storage]
C -- After X mins --> D[Send Audio to Whisper API]
D -- Returns Transcript --> B[Phone App]
B -- Saves Transcript --> F[Phone Storage]

style A fill:#FFFFFF, stroke:#FF4136, stroke-width:2px, color:#FFFFFF
style B fill:#FFFFFF, stroke:#1ABC9C, stroke-width:2px, color:#FFFFFF
style C fill:#FFFFFF, stroke:#FFCC00, stroke-width:2px, color:#1F2020
style D fill:#FFFFFF, stroke:#2ECC40, stroke-width:2px, color:#1F2020
style F fill:#FFFFFF, stroke:#FF6B6B, stroke-width:2px, color:#FFFFFF

linkStyle 0 stroke:#FF4136, stroke-width:2px
linkStyle 1 stroke:#1ABC9C, stroke-width:2px
linkStyle 2 stroke:#FFCC00, stroke-width:2px
linkStyle 3 stroke:#2ECC40, stroke-width:2px
linkStyle 4 stroke:#FF6B6B, stroke-width:2px
```

## Structure

There are 2 different apps in these repositories located in different branches and folders. Our goal is to merge them into one big project. 

- [Standalone Branch](https://github.com/BasedHardware/friend/tree/AppStandalone) or Folder "AppStandalone": Standalone version of the app that doesn't require any hardware to use it. 

- [AppWithWearable Branch](https://github.com/BasedHardware/friend/tree/AppWithWearable) or Folder "AppWithWearable": Wearable-connected version of the app that requires the "Friend necklace" to use it.  

- [Main Branch] Branch that contains firmware, hardware, designs and both apps

## Hardware Buying Guide (<$20 total)

- Board: Seeed Studio XIAO nRF52840 Sense | $15 on [Seedstudio](https://www.seeedstudio.com/Seeed-XIAO-BLE-Sense-nRF52840-p-5253.html) and $24 on [Amazon](https://www.amazon.com/Seeed-Studio-XIAO-nRF52840-Microcontroller/dp/B09T94SZ8K/ref=sr_1_2?dib=eyJ2IjoiMSJ9.i8MUToWd9xYaOg5PHVw2pyxS9i6YZMcZTG4DVV3lwRRKxy64YMOtO-LDhe63d90cDl7xEr3CeA2zN4P5c2G7nGgJl99_6yCVplKsFqtxJyfSQuCMUyZON27nWRtnp-uW1wazpgUV0lN5ds7FKkYz5HTI8bZoLnK2OnFuUet_S4Wsr20oABAovtdI2xrjVYyLaiqLzxrpZyveKDRk_TDpht0rztApuX-YrBb00GDQyFs.sZLkUFW18C8b3EnZpgVKEomXioMKdSLq0F17PikAwc0&dib_tag=se&keywords=nrf52840&qid=1711331537&sr=8-2&th=1) | <$15/unit

- Rechargeable Coin Battery| [$13 for 5 units on Amazon](https://www.amazon.com/EEMB-LIR2450-Rechargeable-Lithium-ion-Batteries/dp/B096LRQWJS/ref=sr_1_2_sspa?c=ts&dib=eyJ2IjoiMSJ9.iB9wqIOnOFHp9bY1qXkvWnYNLa8HARTAYvJVpVbQw-qguwquzLFLUkNGPkwizKa3c7DF0VJuhO9BTT_NvIx7fCvPalViw9V0BMf0AJP70zR5RR3IxfqXO0P7cEVGBldfucYyftWN05Wd58HGdIFSFyDy1ov1-10FzULlR4uIAAkFzUiSMCHzRcC_JSDym8cVGWr6lnYd6X_sn3yLDRaWdzPvoonRihopnSSN_4YS8FB7htsM_hVHhxfkq7VSPEN9Gha0j2_g2N1yFz3c_bHUywG7FTp1GVSX3BWb9LAhWbY.DTlkyIjSmkY3V14SNbhsNkghKuK2l-hoeHuKQYqgqbI&dib_tag=se&keywords=Coin+%26+Button+Cell+Batteries&qid=1711331648&refinements=p_n_feature_twenty_browse-bin%3A10063714011&s=hpc&sr=1-2-spons&ts_id=389581011&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1) and also [link for europe ](https://www.amazon.de/dp/B096LRQWJS?ref=ppx_pop_mob_ap_share)but you only need one | $2.5/unit

- Slider switch | $7 for 30+ units [on Amazon](https://www.amazon.com/Tnuocke-Vertical-Position-Latching-SS12F15-G5/dp/B099N3HFPG/ref=sr_1_2?dib=eyJ2IjoiMSJ9.vWYaZHNA7Z38_YnK7oxLKHvVPX-koqNn5CYGqZXKURCQso_zrAwckot4_h8c77Kgy2-m8FcrQymrZff0rlZIGdECJFA5Rwc5EQObrZ5wDb9zjnwVjonhSZfHlyM-KkJKO4_E6mKcC_I0vZg2vS1PBPkNSAXj9H9pTVK3D2iVtuoMNsxvAEwrYUPx3gYOiIjMOzJYoj8aHPmy2W1R4bWcPWp8IvhbO1GO29TT0jVE97U.ZavNMHkM9KYGMLSB_3DREpSJjhQ16_cjqOpo7aPAfHY&dib_tag=se&keywords=slider%2Bswitch&qid=1711332053&sr=8-2&th=1) but you only need one | <$1/unit

- 3D-print design of the case is located [here](https://github.com/BasedHardware/friend/tree/main/3d-printing%20designs)

## Getting Started 

Follow these steps to get started with your Friend. Note, we tested everything on a mac + iphone. Currently trying to make it work for Android

### Install the app

1. Clone the repo ``` git clone https://github.com/BasedHardware/friend.git ```
2. Choose which version of the app you want to install (see Structure). 
   - Don't have the device? run ```cd AppStandalone``` in terminal
   - Have the device/NRF Board? run ```cd AppWithWearable``` in terminal
3. Install [Flutter](https://docs.flutter.dev/get-started/install/macos/mobile-ios?tab=download) and [CocoaPods](https://guides.cocoapods.org/using/getting-started.html)
4. Install your environment variables
   - For AppWithWearable, open file api_calls.dart located in  ``` AppWithWearable/lib/backend/api_requests  ``` Find "Whisper" and instead of "key", provide your own api-key for openai whisper for transcriptions to work
   
   ![CleanShot 2024-03-25 at 21 58 42](https://github.com/BasedHardware/Friend/assets/43514161/d0fb89d2-07fd-44e3-8563-68f938bb2319)
   - For AppStandalone, update variables in in .env.template file

5. iOS: [Install XCode](https://apps.apple.com/us/app/xcode/id497799835?mt=12) then navigate to the iOS folder. You might need to launch Xcode to select a team and specify a bundle identifier. 
   Android: Download/install [android Studio ](https://developer.android.com/studio) then navigate to the Android folder
   Don't run in web/simulator: Bluetooth will not work
6. Run ```flutter clean ``` then ``` flutter pub get ``` then ``` pod install ```
7. When everything is installed, run ```flutter run ```, this should run your app on a selected device

**No-Code Alternative**: 
- Don't have the device? [Clone this Flutterflow Project ](https://app.flutterflow.io/project/friend-0x9u40)
- Have the wearable device? [Copy this Flutterflow Project](https://app.flutterflow.io/project/friend-share-19bk3d)

### Install Firmware

1. [Download Arduino](https://www.arduino.cc/en/software)
2. Run ```cd src/BluetoothDeviceDriver ``` in your home repository and Open Arduino .ino file, go to "Settings" and paste these 2 links in additional Boards Manager URLs

   ```
   https://adafruit.github.io/arduino-board-index/package_adafruit_index.json
   https://files.seeedstudio.com/arduino/package_seeeduino_boards_index.json
   ```
   ![IMAGE 2024-03-24 19:44:35](https://github.com/BasedHardware/friend/assets/43514161/f08cf422-8d30-4ffa-b61c-0e8ee4a0e685)
3. Go to Boards Manager and download these 2 Boards 

   ![IMAGE 2024-03-24 19:46:49](https://github.com/BasedHardware/friend/assets/43514161/9c85a0c4-ee73-42ba-a75b-3f8fafa81cbe)

4. Connect NRF52840 board via USB cable to your computer
5. Go to Tools > Board > 
   ![IMAGE 2024-03-24 19:50:42](https://github.com/BasedHardware/friend/assets/43514161/065e794f-6e20-4f91-a6bf-1b43a5a3614e)
   and select "Seeed nRF52 mbed-enabled Boards (you need board that has Sense) 

   Also select Port (should be something that contains USB...) 
   ![IMAGE 2024-03-24 19:55:07](https://github.com/BasedHardware/friend/assets/43514161/0719de62-b58f-4ceb-85e2-d288916375c9)

6. Go to Sketch => Include Library => Add .zip library and upload a library which you should download [from here](https://github.com/Seeed-Studio/Seeed_Arduino_Mic), make sure you download the `Seeed_Arduino_Mic` repository itself as a .zip file and not use the .zip from its releases section.
7. Install Arduino BLE and Seeed Arduino LSM6DS3 libraries which can be found in Arduino's menu
8. Click "Upload" and then open Serial Monitor to see logs

### Testing Audio Recording on Your Computer

Follow these steps to test audio recording on your computer using a Python script:

1. Open your terminal and navigate to your home directory.

2. Change to the "src" folder:
   ```
   cd src
   ```

3. Install the required Python modules:
   ```
   pip install -r requirements.txt
   ```

4. Run the Python script:
   ```
   python local_laptop_client.py
   ```
   This script will list the available audio devices and their corresponding IDs.

5. Copy the ID of the desired audio device.

6. Open the `local_laptop_client.py` file in a text editor and locate the following line:
   ```python
   DEVICE_ID = "564A72F4-4552-8CE8-719D-8D5CB2E5D43D"
   ```
   Replace `"564A72F4-4552-8CE8-719D-8D5CB2E5D43D"` with the ID you copied in step 5.

7. Save the changes to the `local_laptop_client.py` file.

8. Run the script again:
   ```
   python local_laptop_client.py
   ```
   or
   ```
   python3 local_laptop_client.py
   ```

9. You can now control the audio recording:
   - Double-tap the device to start recording.
   - Double-tap the device again to stop recording.

The recorded audio files will be stored periodically in the `src/recordings` directory.

That's it! You have now set up and tested audio recording on your computer.

### Assemble the device

**Step 0:** Make sure you have bought everything from the buying guide above

<img src="https://github.com/BasedHardware/Friend/assets/43514161/fdc7f8bd-6205-49a8-aa31-ea4ef6655ba4" width="300">

**Step 1:** You need to design the case using 3D printer. Find .stl file [here](https://github.com/BasedHardware/Friend/blob/main/3d-printing%20designs/Cover%20%2B%20Case.stl). If you don't know how to do it, send this file to someone who has a 3d printer

**Step 2:** 
Solder everything together like on the picture below. using a soldering kit. Don't have it? buy [this one for $9](https://a.co/d/0XdthUV)

![CleanShot 2024-03-28 at 17 01 53](https://github.com/BasedHardware/Friend/assets/43514161/c254668c-1662-412f-8b2c-05a97fb68419)

<img src="https://github.com/BasedHardware/Friend/assets/43514161/5fe4cb81-eb64-41c6-b24c-e2da104b465e" width="300">

**Step 3:** 
Fit everything in the case. Biggest hole is for the usb port. In my example, I put the battery first, then the board and then the switch, however it's not an ideal design. If you will figure out a better solution, please contribute!

<img src="https://github.com/BasedHardware/Friend/assets/43514161/4abae04c-2477-4b9a-a74c-077a463f4c29" width="300">

**Step 4:** Use hot glue to attach the lid to the case. You can also use a scotch tape first for testing purposes. Last, on the USB-port side, you'll find 2 small round holes. This is where the thread should go through. 

<img src="https://github.com/BasedHardware/Friend/assets/43514161/2ffcfbf4-6637-4bb6-89e5-bd75cf78eebd" width="200">

Congratulations! you now have a fully working and assembled device!

## Contributing

[Join our Discord!](https://discord.gg/kEXXsnb5b3)
We welcome contributions from the community! If you're interested in improving Friend, our current biggest goal is to combine both apps together (AppStandalone with AppWithWearable).
- Standalone App brings great prompts and rich structure
- AppWithWearable brings simple bluetooth connecting functionality

## Support

For open-source support, please open an issue on GitHub and/or ask in our [Discord Community](https://discord.gg/kEXXsnb5b3). For commercial support, license inquiries, or any other questions, please contact us directly at [team@whomane.com](mailto:team@whomane.com).

## Disclaimer

Please note that the Friend is a prototype project and is provided "as is", without warranty of any kind. Use of the device should comply with all local laws and regulations concerning privacy and data protection.

Thank you for your interest in Friend, the open-source AI wearable. We're excited to see what you'll build with it!

## Licensing

Friend is available under dual licensing options:

1. **GNU General Public License (GPL)**: For open-source projects and community development, Friend is available under the GPL. This strong copyleft license ensures that all modifications and derived works are also open-source, fostering a collaborative development environment.

2. **Commercial License**: For individuals or entities wishing to use Friend in closed-source projects or who require more flexible licensing terms than those offered by the GPL, a commercial license is available. The commercial license permits private modification, use, and distribution, as well as commercial support and warranty.

### Choosing Your License

- If you wish to contribute to or use Friend in open-source projects, you are free to do so under the terms of the GPL, as detailed in the LICENSE file.
- If you require a commercial license for your project or enterprise, please contact us at [team@whomane.com](mailto:team@whomane.com) to discuss your needs and obtain licensing information.
