# Why This Repository is Public

## Background

This repository is a fork of [moizhassankh/ffmpeg-kit-android-16KB](https://github.com/moizhassankh/ffmpeg-kit-android-16KB), which provides FFmpeg Kit pre-built with **16KB page size alignment** for Android 15+ (API 35) compatibility.

## Why Public?

This repository **must be public** because we use [JitPack](https://jitpack.io) as our Maven repository to distribute the AAR artifact.

**JitPack requires public repositories** to build and serve artifacts without authentication tokens. Making this repo public allows our Flutter project (`komune-mobile`) to pull the dependency via Gradle without any extra authentication setup:

```gradle
maven { url "https://jitpack.io" }

implementation 'com.github.Fauzi-Venturo:ffmpeg-kit-android-16KB:6.1.1'
```

## What This Repo Contains

- Pre-built FFmpeg native libraries (`.so` files) compiled with `max-page-size=16384` (16KB alignment)
- Android library wrapper for FFmpeg Kit
- No proprietary or sensitive code — this is entirely based on open-source FFmpeg (LGPL v3.0)

## Used By

- **komune-mobile** (CUiT app) — `plugins/ffmpeg_kit_flutter/android/build.gradle`

## Original Source

- Upstream: [arthenica/ffmpeg-kit](https://github.com/arthenica/ffmpeg-kit) (archived)
- 16KB fork: [moizhassankh/ffmpeg-kit-android-16KB](https://github.com/moizhassankh/ffmpeg-kit-android-16KB)
