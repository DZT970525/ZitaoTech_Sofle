<h1 align="center">Z i t a o T e c h - S o f l e</h1>
ZitaoTech-Sofle keyboard combines a 60-key split keyboard with MX switches with a built-in TrackPoint, helping users stay focused by eliminating hand movement between keyboard and mouse.  

# Key Features
- Dual mouse (trackpoint, trackpad and opt. trackball)
- Two Encoders
- Two Ultra-Low-Power memory lcd display
- Aluminium case
- 30 keys per side

# Image gallery
<p align="center">
<img width="800"  src="https://github.com/DZT970525/ZitaoTech_Sofle/blob/main/Pic/SoflePic1.jpg"/>
</p>

# Keymap

<p align="center">
<img width="800"  src="https://github.com/DZT970525/ZitaoTech_Sofle/blob/main/Pic/Sofle_Keymap.png"/>
</p>

# Trackpoint and mouse layer [🔼](#contents)
When you put your finger on the trackpoint and move the keyboard will automatically enter mouse layer and will exit to default layer0 when there is no trackpoint move.
The detailed mouse layer keymap can be found on the picture:

<p align="center">
<img width="800"  src="https://github.com/DZT970525/ZitaoTech_Sofle/blob/main/Pic/MouselayerPic.png"/>
</p>

# Change trackpoint dpi on the fly [🔼](#contents)
In the default firmware, when Layer 1 is active, these two small buttons can be used to adjust the TrackPoint DPI.  
The TrackPoint provides 10 DPI levels in total. During dpi adjustment, the LED will indicate you the current DPI level.  
<p align="center">
<img width="250"  src="https://github.com/DZT970525/KEYPOINT/blob/main/Picture/change_dpi.png"/>
</p>

# How to connect this keyboard with your device [🔼](#contents)
- Turn on the Bluetooth on your PC or your phone
- Find the device ```ZITAOTECH_SOFLE``` and pair with it then you should type with the keyboard
> [!CAUTION]
> After you delete the bluetooth profile and if you want to pair with the keyboard with another device when you have already paired with some device before, make sure to enter layer 1 and press the encoder on the left half keyboard to clear the bluetooth profile on the keyboard side. Otherwise there will be error when you want to pair with another device!!! Please use the following steps to delete the bluetooth pairing
- First delete the bluetooth profile(somewhere it's called forget the device or unpair the device) on your device
- Enter layer 1 and press the encoder on the left split keyboard 
- Refresh the Bluetooth setting page on your device(You can turn on and off the bluetooth) and then you can pair the keyboard with your device again or with other devices on the same bluetooth channel.

# How to make flash a new firmware and reset the keyboard [🔼](#contents)

You can make the keyboard enter bootloader when the keyboard is connected with your PC and flash a new firmware to the keyboard.

There is a reset button on the keyboard and you can use a pin to double tap the reset button within 500ms and the keyboard will enter bootloader.

Now a new USB Disk will be found by your PC called nice!nano, you can drag the new uf2 firmware file into the USB disk and a new firmware will be flashed.

If you have issues will bluetooth connect like you can't connect the keyboard anymore with your PC, you can first flash the reset firmware into the keyboard and re-flash the normal firmware and everything will be reset so you can connect the keyboard with your device again.

You can find the firmware [here](https://github.com/DZT970525/ZitaoTech_Sofle/tree/main/Firmware)

# Multi device connect [🔼](#contents)
By default the keyboard can be paired with 4 devices at the same time and can be switched between them seamlessly. Here are the steps how to connect with devices:
1. Assume you have already connected this keyboard with one device
2. Now enter layer 1 and rotate the encoder on the left half keyboard and the lighted number will show you which bluetooth channel(which device) the keyboard is ready to be connected

<p align="center">
<img width="250"  src="https://github.com/DZT970525/KEYPOINT/blob/main/Picture/left_display_number.png"/>
</p>
Now the keyboard is ready to be paired with another device
Similarly, you can pair this keyboard with a third and a fourth device.  

4. Once pairing is done, you can switch between the devices the same way.

> [!CAUTION]
> - The BT_CLEAR keycoode — which is triggered by pressing the encoder on the left half keyboard — is calculated independently for each device. This means that when you trigger BT_CLEAR while connected to the second device, it won’t affect any of the other devices.

# Output select [🔼](#contents)
The keyboard can be set at USB output or Bluetooth output, it can be read on the left display.  
You can toggle the output by **pressing the T key at layer one by default**  
This output is important when you want to update your keymap via ZMK Studio.  
<table >
    <tr>
        <td><img src="https://github.com/DZT970525/KEYPOINT/blob/main/Picture/USB_Output_image.png"  style="width:300px;"/></td>
        <td><img src="https://github.com/DZT970525/KEYPOINT/blob/main/Picture/BLE_Output.png"  style="width:300px;"/></td>
    </tr>
</table>

# Realtime Keymap Updating [🔼](#contents)
[ZMK Studio](https://zmk.dev/docs/features/studio) provides runtime update functionality to ZMK powered devices, allowing users to change their keymap layers without flashing new firmware to their keyboards.  

You can use ZMK Studio with ```Chrome/Edge``` at [https://zmk.studio/](https://zmk.studio/).  

Before you use ZMK Studio, you need to get the keyboard plugged with you computer and set the keyboard at ``USB output mode`` [Please refer to this content](https://github.com/DZT970525/KEYPOINT/tree/main#output-select-), then you can select the port shown on the ZMK Studio page and then start the keymap updating.  

The picture below shows you how it looks like when the keyboard connects with ZMK Studio successfully.  
<p align="center">
<img width="800"  src="https://github.com/DZT970525/KEYPOINT/blob/main/Picture/zmk_studio.png"/>
</p>

> [!NOTE]
> - The USB output status will only show when the keyboard is connected with a host device through a cable

# How to pair with dongle

You can use this keyboard with an external dongle then you don't need to mess up with Bluetooth.

<p align="center">
<img width="400"  src="https://github.com/DZT970525/ZitaoTech_Sofle/blob/main/Pic/Dongle.png"/>
</p>

The dongle can show the current layer, wpm, battery of each keyboard and the current output status.

But the default firmware doesn't include the dongle part, to pair with the dongle need to do the following steps:

1. Make the left keyboard enter bootloader and flash the reset firmware. [How to make the keyboard enter bootloader](https://github.com/DZT970525/ZitaoTech_Sofle/tree/main#how-to-make-flash-a-new-firmware-and-reset-the-keyboard-)
2. After the reset firmware is flashed, flash the normal firmware for the left keyboard
3. Do the same thing on the right keyboard: first flash the reset firmware and re-flash the normal firmware.

You can find the firmware [here](https://github.com/DZT970525/ZitaoTech_Sofle/tree/main/Firmware/Macintosch_firmware)
> [!NOTE]
> - Make sure you power on the left keyboard first when the dongle is plugged otherwise the dongle will show the battery percent of the right keyboard on the left side.
