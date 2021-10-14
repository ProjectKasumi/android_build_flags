# Build flags for Project Kasumi

## Everything is easy if you know. And so here I provide all the flags you can use to configure your build.

### Coming from LineageOS

```
WITH_SU := true
```

This flag will ship your build with LineageSU (The good old SuperUser that's built into LineageOS and most of its forks).

-----

### Coming from Project Materium

```
KASUMI_BUILD_TYPE := gapps
TARGET_GAPPS_ARCH := arm | arm64
```

First flag will ship your build with GApps while second flag will define GApps architecture.

If you omit the GApps arch, it will be defaulted to ARM64.

```
TARGET_FACE_UNLOCK_SUPPORTED := true | false
```

This flag will define whether if your build will be shipped with face unlock of not. For ARM devices, though, you have to keep this off if you don't have the lib for it present.

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

This flag will ship your build with Lawnchair included and remove Trebuchet+.

```
KASUMI_SHIP_GSANS := true
```

This flag will ship your build with Google Sans as default font instead of Roboto.

```
KASUMI_SHIP_ADAWAY := true
```

This flag will ship your build with AdAway included.
