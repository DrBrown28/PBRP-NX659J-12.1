# Pit_Black_Recovery_For_nx659j
To build Custom recoveries for Nubia Red Magic 5S/5G

Kernel and all blobs are extracted from [NX659J-update.zip](http://romdownload.nubia.com/%E7%BA%A2%E9%AD%945G/V9.50/NX659J-update.zip) firmware.

The Nubia RedMagic 5G (codenamed _"NX659J"_) and Nubia RedMagic 5S (codenamed _"NX659J_V1S or NX659J"_) are high-end gaming smartphones from Nubia.

Nubia RedMagic 5S / 5G was announced and released in March / July 2020.

## Device specifications

| Device       | Nubia RedMagic 5G / 5S                      |
| -----------: | :------------------------------------------ |
| SoC          | Qualcomm SM8250 Snapdragon 865              |
| CPU          | 8x Qualcomm® Kryo™ 585 up to 2.84GHz        |
| GPU          | Adreno 650                                  |
| Memory       | 8GB / 12GB/ 16GB RAM (LPDDR5)               |
| Shipped Android version | 10                               |
| Storage      | 128GB / 256GB UFS 3.0 flash storage         |
| Battery      | Non-removable Li-Po 4500mAh                 |
| Dimensions   | 168.56 x 78 x 9.76 mm                       |
| Display      | 2340 x 1080 (19.5:9), 6.65 inch             |

## Device picture

![Nubia RedMagic 5G](https://ui.nubia.cn/upload/image/5e66e39ab9ea42.jpg)

## Features

**Works**

- Booting.
- ADB
- ADB Sideload
- MTP
- OTG
- Super partition functions
- Vibration
- Encryption
- Flashing zips and rom files

## Compile

First checkout the PBRP manifest in it's latest branch:

```
repo init -u https://github.com/PitchBlackRecoveryProject/manifest_pb -b android-12.1
repo sync

```

Use ccache
```
#Enable ccache
export USE_CCACHE=1
export CCACHE_EXEC=$(which ccache)
```

Finally execute these:

```
export ALLOW_MISSING_DEPENDENCIES=true
. build/envsetup.sh
lunch pb_NX659J-eng
mka pbrp
```

To test it:

```
fastboot flash recovery out/target/product/NX659J/recovery.img
```
