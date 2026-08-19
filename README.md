# Cubot P50 (P50 / marlon) Proprietary Vendor Blobs

> Proprietary vendor files and HAL binaries for Cubot P50 (MediaTek MT6765 / MT6762)

## What is this?
This repository contains the extracted proprietary blobs, MediaTek HAL shared libraries, TrustKernel TEE trustlets, firmware images, and audio tuning parameters extracted from the official stock firmware (`full_v956-user 11 RP1A.200720.011 20220816 release-keys`).

## Included Components
- **MediaTek Core HALs**: Audio, Bluetooth, Camera, DRM, GNSS/GPS, Radio/RIL, Power, Sensors, Thermal, and USB.
- **TrustKernel TEE**: Secure OS trustlets (`.ta`), `teed` storage daemon, Keymaster 4.0, and Gatekeeper 1.0.
- **Display & Graphics**: PowerVR Rogue GE8320 IMG DDK drivers, Gralloc 4.0, and Hardware Composer 2.0.
- **Radio & Telephony**: MTK Dual-SIM telephony stack and APDB calibration databases.

## Integration
Include in your device tree makefile:
```makefile
$(call inherit-product, vendor/cubot/marlon/marlon-vendor.mk)
```

And in `BoardConfig.mk`:
```makefile
include vendor/cubot/marlon/BoardConfigVendor.mk
```

## License
- The binaries and firmware included are proprietary to MediaTek Inc. and CUBOT Mobile Limited.
- Makefiles and build scripts: SPDX-License-Identifier: Apache-2.0
