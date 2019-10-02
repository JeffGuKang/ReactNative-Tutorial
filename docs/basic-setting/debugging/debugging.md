# Debugging

## Enabling keyboard shortcuts 

+ ios (Requirement)
    + Open Hardware menu, select Keyboard, and make sure that "Connect Hardware Keyboard" is checked

## Accessing the In-App Developer Menu

+ ios
    + You can acess the developmenu
    1. Shake your device or sel ect "Shake Gesture" inside the Hardware menu (iOS Simulator)

    2. Keyboard shortcut 
        + `⌘D` (iOS emulator)
        + `⌘M` (Android emulator, Mac OS)
        + `Ctrl+M` (Windows, Linux)
        + Use command `adb shell input keyevent 82` to open the dev menu (82 being the Menu key code, Android)

    ``` The Developer Menu is disabled in release (production) builds.```


# In-app Errors and Warnings

Errors and warning are displayed inside your app in development builds

## Errors

In-app erros are displayed in a full screen alert with a red back inside your app (known as a Red Box)

You can use `console.error()` to manually trigger one.

## Warnings

Warnings will be displayed on screen with a yellow background(known as a Yellow Box)

+ Show more information (Click on the alerts or to dismiss them)

You can use `console.warn()` to trigger a YellowBox

+ Disable YellowBoxes during development
 
    `console.disableYellowBox=true;` 

+ Specific warnings can be ignored programmatically by setting an array of prefixes that should be ignored

    ``` 
    import {YellowBox} from `react-native`;
    YellowBox.ignoreWarnings(['Warning: ...']);
    ```

+ CI/Xcode 
    YellowBoxes can be disabled by setting `IS_TESTING` environment variable

 RedBoxes and YellowBoxes are automatically disabled in release (production) builds

# Chrome Developer Tools (To Debug)

`Note: the React Developer Tools Chrome extension does not work with React Native, but you can use its` [standalone version](live-reload.md#React-developer-tools)


+ Select `Debug JS Remotely` from the Developer Menu [http://localhost:8081/debugger-ui.](http://localhost:8081/debugger-ui.)

+ Select `Tools → Developer Tools` from the Chrome Menu to open the `Developer Tools.`

+ Keyboard shortcuts
 + `⌘⌥I` (macOs)
 + `Ctrl+Shift+I` (Windows)

+ Step further [Pause On Caught Exceptions](https://stackoverflow.com/questions/2233339/javascript-is-there-a-way-to-get-chrome-to-break-on-all-errors/17324511#17324511)





