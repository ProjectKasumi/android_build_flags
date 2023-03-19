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
KASUMI_SHIP_GCGOP := true
```

This flag will ship your build with GCam GO Prebuilt
included. For best results, combine this with GApps
builds only;

```
ifeq ($(KASUMI_BUILD_TYPE),gapps)
    KASUMI_SHIP_GCGOP := true
endif
```
