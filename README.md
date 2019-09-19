# Description
This repository shows how the Vibes Push SDK can be integrated into a React Native application natively.


## General Requirements 
1. You will need to obtain an application ID for your app from Vibes Customer Service. This will be referred to as `yourAppId` throughout this document.
2. Everything you see in this repository is based on recommended behavour in the Vibes Push Notification SDK documentation available [here](https://developer.vibes.com/display/APIs/Vibes+Push+Notifications+SDK).
3. You will need to specify a url addressing our servers for different markets based on your target audience. This url is refferred to as `yourApiUrl` throughout this document. For the US market, the url is `https://public-api.vibescm.com/mobile_apps`. For  the non-US market, the url is `https://public-api.vibescmeurope.com/mobile_apps`. 

### Requirements for iOS
1. You will need to replace the **yourAppId** AND **yourApiUrl** in the `ios/sampleReactNative/Info.plist` with a previously obtained application ID and one of the server urls above.
2. You will notice that the `ios/Podfile` file contains the reference to the Vibes SDK library for iOS. You may change the library version in this file.
3. The rest of the code initializes and configures the environment to receive and display push notifications in an iOS environment. You are invited to copy and reuse as appropriate.

### Requirements for Android
1. You will need to replace the **yourAppId** AND **yourApiUrl** in the `android/app/build.gradle` with a previously obtained application ID and one of the server urls above. These are passed into the AndroidManifest.xml file to configure the SDK.
2. You will notice that the `android/app/build.gradle` file contains the reference to the Vibes SDK library for Android (**com.vibes.vibes:vibes:3.1.0**). Also take not of the versions of other dependencies such as firebase-messaging and google-play-services. Those are important, and should reflect in your react-native app.
3. You will need to provide your own **google-services.json** file, matching one generated for the specific *applicationId* in the Firebase console.
4. The rest of the code initializes and configures the environment to receive and display push notifications in an Android environment. You are invited to copy and reuse as appropriate.