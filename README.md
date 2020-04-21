# OmniStack - Mobile

The mobile implementation of OmniStack course.

See more details in the [main repository](https://github.com/adrianokerber/omnistack).

## First steps

After clonning the repository run `yarn` or `yarn install` to download Node packages.

**WARNING**: Make sure you have [Java 8](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) installed. And point `JAVA_HOME` environment variable to it. Download [here](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) or [here](https://jdk.java.net/java-se-ri/8-MR3)

### Running the app

- Start your emulator or connect your device
- Run one of the commands to build/rebuild and deploy an app version to the device
    - iOS: `yarn ios`
    - Android: `yarn android`
- Run `yarn start` to start the debug without recompiling all the application for your device.

If you install a new dependency, you must rebuild the project on iOS using `pod install` and running `yarn ios` to deploy again. On Android you just need to run `yarn android`

NOTE: for more details look on `package.json`

### Device shortcuts

Android

- Double tap `R` to reload code on device
- `Ctrl + M` or shake to open React Native debug menu

iOS

- `Cmd + R` to reload code on device
- `Cmd + D` or shake to open React Native debug menu

#### Debug

In order to open debug, just open **React Native debug menu** and click **debug**. A Window will open on your browser to debug.

## Debugging tips

Running on an emulator can be tricky, so read the following tips.

- If using **AndroidSDK's emulator** run `emulator -list-avds` to retrieve the names of the configured emulator instances, then run `emulator -avd` plus the name of the avd you want to start. Eg: `emulator -avd Nexus_5_API_27`.
- In order to run Android emulator pointing to our local machine, just run `adb reverse tcp:3333 tcp:3333` that means, connect the device tcp _port_ to our development machine _port_. See more details on [documentation](https://developer.android.com/studio/command-line/adb#forwardports);