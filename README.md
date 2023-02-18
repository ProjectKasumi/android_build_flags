# Build flags for Project Kasumi

## Everything is easy if you know. And so here I provide all the flags you can use to configure your build.

```
KASUMI_BUILD_TYPE := gapps
TARGET_GAPPS_ARCH := arm | arm64
```

First flag will ship your build with GApps while second flag
will define GApps architecture.

If you omit the GApps arch, your arch will be detected
automatically.

```
KASUMI_BUILD_TYPE := auroraoss
```

This flag will ship your build with Aurora Store and AuroraServices.

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
