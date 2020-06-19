# BeaconRnTest
This is an example application to test the 2.0 beta version of the helpscout beacon ios sdk with react native

## Requirements
React native requires Node & Watchman to be installed.  These can be installed on macOS via Homebrew:
```
brew install node
brew install watchman
```
 This project also requires yarn to be installed, which can also be installed view Homebrew:
```
brew install yarn
```

## Building & Running

This project can be built and run using yarn.

```
yarn && yarn ios
```

It can also be ran with xcode by building and running with the `BeaconRnTest` scheme.


## General information

The iOS portion of this project is located in the `/ios` directory.  The project has been initialized with cocoapods so the `BeaconRnTest.xcworkspace` file must be used when opening the iOS project with xcode.

This example project was generated using `npx react-native init`.  After that a `Dummy.swift` file was created via xcode in the `/ios/BeaconRnTest` directory in order to generate a swift bridging header.  The ios deployment target was then set to `11.0` as per the requirement for the beacon ios sdk.  Finally, the `Beacon` pod version `2.0.0-beta.2` was added to the Podfile for the `BeaconRnTest` target and `pod install` was executed.

## Other

Some generic convenience methods were added to the `package.json` file:

- `yarn clean` will delete the node_modules directory, pods download directory, ios build directories, and android build directories.  Then it will re-install all node dependencies.
- `yarn pods` will re-install pods
