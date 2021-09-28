# Build flags for Stellar-Weeb

## Everything is easy if you know. And so here I provide all the flags you can use to configure your build.

### Coming from LineageOS

```
WITH_SU := true
```

This flag will ship your build with LineageSU (The good old SuperUser that's built into LineageOS and most of its forks).

-----

### Coming from Stellar OS

```
STELLAR_BUILDTYPE := gapps
TARGET_GAPPS_ARCH := arm | arm64
```

First flag will ship your build with GApps while second flag will define GApps architecture.

If you omit the GApps arch, it will be defaulted to ARM64.

```
TARGET_FACE_UNLOCK_SUPPORTED := true | false
```

This flag will define whether if your build will be shipped with face unlock of not. For ARM devices, though, you have to keep this off if you don't have the lib for it present.

-----

### Special to Stellar-Weeb

As of 1.2 Staging "Botan";

```
SHIPPING_WITH_LAWNCHAIR := true
```

This flag will ship your build with Lawnchair included and remove Trebuchet+.

```
SHIPPING_WITH_GSANS := true
```

This flag will ship your build with Google Sans as default font instead of Roboto.

```
SHIPPING_WITH_ADAWAY := true
```

This flag will ship your build with AdAway included.
