WhirlyGlobe-SDK
===============

A precompiled version of WhirlyGlobe suitable for use when you don't want to keep compiling the whole thing

To build from the command line in the root directory (right above WhirlyGlobeSrc), do the following:

pod update
xcodebuild ARCHS="armv7 armv7s" ONLY_ACTIVE_ARCH=NO -workspace WhirlyGlobe.xcworkspace -scheme WhirlyGlobe-SDK -sdk iphoneos -configuration Debug clean build
xcodebuild ARCHS="i386" ONLY_ACTIVE_ARCH=NO -workspace WhirlyGlobe.xcworkspace -scheme WhirlyGlobe-SDK -sdk iphonesimulator -configuration Debug build

The output will be in WhirlyGlobe-SDK/SDKRoot and will include headers and a single (obese) library.
