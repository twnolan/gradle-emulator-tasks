# Gradle Emulator Tasks

This repository includes gradle tasks that can be used to control android emulators.


## Commands

### Android Pre-TestCommands

the following are composite commands are the commands to be used when starting an emulator for a test

```
launchAndroidMEmulator - Check if required emulator imgae is installed, install if not, create emulator from image, start emulator ANDROID-M
launchAndroidNEmulator - Check if required emulator imgae is installed, install if not, create emulator from image, start emulator ANDROID-N
launchAndroidOEmulator - Check if required emulator imgae is installed, install if not, create emulator from image, start emulator ANDROID-O
```

### Android Sub command Tasks

the following are individual commands that are used together in the composite commands above 

```
createAndRunEmulatorAndroidM - Starts emulator, creates and starts emulator if it does not exist ANDROID-M
createAndRunEmulatorAndroidN - Starts emulator, creates and starts emulator if it does not exist ANDROID-N
createAndRunEmulatorAndroidO - Starts emulator, creates and starts emulator if it does not exist ANDROID-O
installSDKPackages - Install missing emulator packages
listEmulators - lists all emulators on host machine
listInstalledSDKPackages - List all installed android sdk packages
```

## Maintainence

In order to update the android images to new version edit the following code:

```
String[] androidImageN = ["ANDROID-O", "system-images;android-27;google_apis_playstore;x86"]
String[] androidImageNMinus1 = ["ANDROID-N", "system-images;android-25;google_apis_playstore;x86"]
String[] androidImageNMinus2 = ["ANDROID-M", "system-images;android-23;google_apis;x86"]
```