# steam-macos-native
Native ARM64 build of Steam for MacOS

# Why?
Steam installer still requires Rosetta but installs the native application for ARM. This serves as a mirror and allows you to skip Rosetta installation entirely.

Tested on my Macbook Neo and MacOS Tahoe

# Instructions

Unzip and move Steam to /Applications, then launch to update.


# Verification

If you wish to verify file wasn't tampered with, use:
```
$ codesign --verify --deep --strict --verbose=2 Steam.app
```
Example output:

> --prepared:/Applications/Steam.app/Contents/Frameworks/crashhandler.dylib
> --validated:/Applications/Steam.app/Contents/Frameworks/crashhandler.dylib
> --prepared:/Applications/Steam.app/Contents/Frameworks/Breakpad.framework/Versions/Current/.
> --validated:/Applications/Steam.app/Contents/Frameworks/Breakpad.framework/Versions/Current/.
> Steam.app: valid on disk
> Steam.app: satisfies its Designated Requirement

