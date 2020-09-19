---
title: "iOS"
date: "2020-09-18"
latestSDK: "v6.4"
lastRelease: "2020-09-09"
---

The Swrve native iOS SDK enables your app to use all of these features. This guide contains all the information you need to integrate the SDK into your app.

> The code examples in this guide refer exclusively to Swrve iOS SDK version 6.0+. If you are upgrading from an SDK older than version 6.0, please also refer to the SDK release notes to review major changes made to the SDK methods and APIs in all major versions.

## Requirements

- The Swrve iOS SDK supports iOS 10 and later but is able to handle older OS versions with a dummy SDK.
- OTT – The Swrve iOS SDK includes support for tvOS. There are no additional integration steps, however if you use Carthage or manually install the SDK, you must specify the platform. For more information, see the relevant section under [Installing the SDK](https://docs.swrve.com/developer-documentation/integration/ios/#Installing_the_SDK).
- Ensure you have the latest version of Xcode.
- If you’re developing your app in Swift, we recommend upgrading to the latest SDK version to prevent compatibility issues. For more information, see Integrating the iOS SDK using Swift.
- The App ID and API Key for your app. This information is available in Swrve on the Integration Settings screen (on the Settings menu, select Integration settings).


## Frameworks

The Swrve SDK references the following frameworks:

- CFNetwork.framework
- StoreKit.framework
- Security.framework
- QuartzCore.framework
- CoreTelephony.framework
- UIKit.framework
- MessageUI.framework
- CoreLocation.framework
- AVFoundation.framework
- CoreText.framework
- UserNotificationsUI.framework
- UserNotifications.framework

If you want to exclude the push notification feature, you can remove the following frameworks by adding an associated preprocessor macro (for more information, see How do I exclude optional iOS frameworks?):

- UserNotificationsUI.framework
- UserNotifications.framework

### Automatic Reference Counting
If your Xcode project does not use Automatic Reference Counting (ARC), and you’re manually installing the SDK (that is, not using CocoaPods), you must enable ARC for each file in the Swrve SDK.