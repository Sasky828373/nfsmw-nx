# nfsmw-nx Android port

Experimental Android/ARM64 host for the nfsmw-nx ReXGlue port.

## Goal
Keep the existing Xbox 360 recompilation and native Vulkan renderer, while replacing the Horizon/libnx host layer with Android NDK equivalents.

Initial target:
- Android arm64-v8a
- API 28+
- NativeActivity bootstrap
- Vulkan loader through Android NDK
- game files supplied by the user at runtime

This branch intentionally keeps the existing Switch build untouched.

## Build prerequisites
- Android SDK
- Android NDK
- CMake 3.25+
- Ninja
- JDK 17+

The Android host is being brought up incrementally. The first milestone is a loadable APK/native library; game boot requires the generated ReXGlue game sources and the user's legally obtained Xbox 360 game files.
