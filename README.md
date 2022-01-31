# Build flags for Project Kasumi

## Everything is easy if you know. And so here I provide all
## the flags you can use to configure your build.

### Coming from LineageOS

```
WITH_SU := true
```

This flag will ship your build with LineageSU (The good old
SuperUser that's built into LineageOS and most of its forks).

-----

### Coming from Project Materium

```
KASUMI_BUILD_TYPE := gapps
TARGET_GAPPS_ARCH := arm | arm64
```

First flag will ship your build with GApps while second flag
will define GApps architecture.

If you omit the GApps arch, it will be defaulted to ARM64.

```
TARGET_FACE_UNLOCK_SUPPORTED := true | false
```

This flag will define whether if your build will be shipped with
face unlock or not. For ARM devices, though, you have to keep this
off if you don't have the lib for it present.

-----

### Special to Project Kasumi

As of 1.0 "PoPiPa";

```
KASUMI_BUILD_TYPE := auroraoss
```

This flag will ship your build with Aurora Store and AuroraServices.

```
KASUMI_SHIP_LAWNCHAIR := true
```

This flag will ship your build with Lawnchair included and remove
Trebuchet+.

```
KASUMI_SHIP_ADAWAY := true
```

This flag will ship your build with AdAway included.

```
TARGET_NEEDS_LINEAGE_ISFP_PERM := true
```

This flag is specifically for devices with in-screen fingerprint
hardware and needing
`vendor.lineage.biometrics.fingerprint.inscreen.xml`. [You can check
`device.mk` to see if your device needs it.](https://github.com/Haky86/android_device_samsung_a70q/blob/21d461bb2fa491b2268df1aabe0ef82185b185af/device.mk#L42)

To come to what this flag does, it defines that file's path as the
one of Kasumi's (Namely `vendor/kasumi`) and so nothing problematic
occurs regarding this file. If your maintainers tell you to change
that path from `vendor/lineage` to `vendor/kasumi` while building,
remember this flag and tell them about it - Link if necessary.

```
TARGET_BOOT_ANIMATION_RES := 480 | 720 | 1080 | 1440
```

This flag defines the boot animation resolution to use. If you
omit this, it will be defaulted to "720".
