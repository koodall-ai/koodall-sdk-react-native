# Koodall AR Toolkits SDK Native  
[![](https://www.koodall.ai/media/images/logo/logo-color.svg)](https://www.koodall.ai/)

[React Native Face AR SDK](https://www.koodall.ai/face-filters.html) is part of the **Koodall AR Toolkits SDK**. This SDK provides powerful augmented reality tools for applying visual effects to photos and live video streams, including use cases in live streaming and video conferencing. The package offers the following features:

- **Face and hand tracking**
- **3D face filters**
- **Virtual try-on**: jewelry, cosmetics, glasses, contacts, headwear, and more
- **Color filters (LUTs)**
- **Face touch-up tools**
- **Virtual backgrounds**
- **Screen recording and screenshot capture**
- And more...

## [Requirements](https://docs.koodall.ai/far-sdk/tutorials/capabilities/system_requirements)

## Usage

### Token Management  
You can freely explore all SDK features before committing to a license. To obtain a trial token, contact us at [sales@koodall.ai](mailto:sales@koodall.ai).

### Getting Started  

1. **Clone the repository** and ensure your [React Native CLI development environment](https://reactnative.dev/docs/environment-setup) is configured.  
2. **Insert the Client Token** into the appropriate section of [`example/src/App.tsx`](example/src/App.tsx#L18).  
3. **Install dependencies** by running the `yarn` command.  
4. **(iOS)** Navigate to `example/ios` and execute `pod install` to install iOS dependencies. Then, return to the root directory.  
5. **Connect a device** and run `yarn example ios` or `yarn example android`. Alternatively, open the Xcode or Android Studio projects located in `example/ios` or `example/android`.  

You can also use `npm` to execute the sample. See [example/README.md](example/README.md) for details.

---

## Integration Steps  

Below are the steps to integrate the **Koodall SDK** into an existing React Native app. Make sure you have a valid client token.

1. **Add the SDK Dependency**  
    Use the following command to install the SDK:  
    ```sh
    yarn add @koodall/react-native

2. **(iOS) Add the native SDK reference:**
Include the Koodall SDK in the [`ios/Podfile`](example/ios/Podfile#L13): 
    ```ruby
    source 'https://github.com/koodall-ai/koodall-sdk-podspecs.git'
    ```
    Define the required version:
    ```ruby
    $bnb_sdk_version = '~> 1.13.0'
    ```
    List [SDK packages](https://docs.koodall.ai/far-sdk/tutorials/development/installation) you plan to use.

3. **(Android) Add the native SDK reference:**
Add the [maven repository](example/android/build.gradle#L13) to `build.gradle` and define `ext.bnb_sdk_version`.
In the example/android/app/build.gradle file, list the necessary [SDK packages you need](https://docs.koodall.ai/far-sdk/tutorials/development/installation).

4. **Integrate the Code**
Copy code from e`xample/src/App.tsx` into your project.

5. **Add Effects Folder**
Include the `effects` folder in your project:
* **iOS:** Link the folder in Xcode (`File → Add Files to...`).
* **Android:** Add [this](example/android/app/build.gradle#L132) code to the `build.gradle` file.

6. **For iOS**: add [`NSCameraUsageDescription`](example/ios/ReactNativeExample/Info.plist#L34).


## Documentation
Refer to [this file](src/index.tsx) for available APIs. For more detailed information about the [Koodall AR Toolkits SDK](https://docs.koodall.ai/), visit the official documentation.