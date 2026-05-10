# OrangeFox Device Tree for Xiaomi Sky (Redmi Note 12R / Poco M6 Pro 5G)

This is a work-in-progress OrangeFox Recovery Project device tree for the Xiaomi Sky (parrot platform).

## Device Specifications

| Feature               | Specification                                   |
| --------------------- | ----------------------------------------------- |
| SoC                   | Qualcomm Snapdragon 4 Gen 2 (SM4450)            |
| CPU                   | Octa-core (2x2.2 GHz Cortex-A78 & 6x1.95 GHz)   |
| GPU                   | Adreno 613                                      |
| Display Resolution    | 1080 x 2460                                     |
| Architecture          | arm64-v8a                                       |

## Tree Status

- **Status:** Experimental / Beta
- **Platform:** parrot
- **Maintainer:** Altaf Yafai
- **Base:** Android 12.1 (OrangeFox branch)

## Features

- Fully functional decryption (FBE)
- 90 FPS support (Hardware limit)
- Virtual A/B support
- Fastbootd support with ADSP firmware loading

## Build Instructions

To build OrangeFox for Xiaomi Sky:

1. Sync the OrangeFox manifest (12.1 branch).
2. Clone this repository into `device/xiaomi/sky`.
3. Run the following commands:
```bash
source build/envsetup.sh
export ALLOW_MISSING_DEPENDENCIES=true
lunch twrp_sky-eng
mka adbd recoveryimage
```

## Credits

- OrangeFox Recovery Project
- hipexscape (Base tree)
- pjgowtham (Reference)
- Altaf Yafai (Current Maintainer)
