# device_xiaomi_sweet-twrp

Tree for building TWRP for Xiaomi Redmi 10 Pro

The Xiaomi Redmi Note 10 Pro (codenamed "sweet / sweetin") are mid range smartphones from Xiaomi.

## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
| CPU     | 2x2.3 GHz Kryo 470 Gold & 6x1.8 GHz Kryo 470 Silver      |
| Chipset | Qualcomm SM7150 Snapdragon 732G (8 nm)                   |
| GPU     | Adreno 618                                               |
| Memory  | 6/8 GB RAM                                               |
| Shipped Android Version | 11 with MIUI 12                          |
| Storage | 128 GB (UFS 2.2)                                         |
| Battery | Non-removable Li-Po 5020 mAh                             |
| Display | 1080 x 2400 pixels, 6.67 inches (~395 ppi pixel density) |
| Rear camera 1 | 64 MP, f/1.9, LED flash, HDR, panorama, 4K@30fps  |
| Rear camera 2 | 8 MP, f/2.2, 118˚ (ultrawide)                      |
| Rear camera 3 | 5 MP, f/2.4, (macro)                               |
| Rear camera 4 | 2 MP, f/2.4, (depth)                               |
| Front Camera | 16 MP, f/2.5, Panorama, 1080p@30fps                 |
| Sensors | Fingerprint (side-mounted), accelerometer, gyro, proximity, compass |
| Release Date | March 2021                                          |

## Device picture
![Xiaomi Redmi Note 10 Pro](https://i.imgur.com/t3byGh9.png "Xiaomi Redmi Note 10 Pro")

## Compile

First repo init the TWRP 12.1 tree (shallow clone):

```shell
repo init --depth=1 -u https://github.com/Huexxx/platform_manifest_twrp_aosp.git -b twrp-12.1
```

Sync source:

```shell
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

Clone device tree:

```shell
git clone https://github.com/Huexxx/twrp_device_xiaomi_sweet -b 13 ./device/xiaomi/sweet
```

Finally execute these:

```
. build/envsetup.sh
lunch twrp_sweet-eng
mka recoveryimage
```

## Credits

Special thanks to the following people or repo:

- [TeamWin](https://github.com/TeamWin)
- [nebrassy](https://github.com/nebrassy)
- [basamaryan](https://github.com/basamaryan)
