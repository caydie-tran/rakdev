---
title: Finger Print Recognition
layout: page
parent: _esd/helpcenter-mobile.md
categories: [Ecosystem, Analytics, Mobile, Android, iOS, finger print, authentication, biometric]
---

# What is Touch ID and Fingerprint Recognition?

Mobile apps can use Touch ID on iOS, or a fingerprint recognition sensor on Android, to confirm a user's identity.

The current version of the SDK provides fingerprint recognition support for verifying the identity of a logged in user.

For example, when a logged-in shopper in Japan Ichiba app proceeds to checkout, the app requires the shopper to verify their identity. If fingerprint recognition is supported on the Japan Ichiba app, the shopper can either use their registered fingerprint to confirm their identity, or enter their password.

Fingerprint recognition is not an alternative to basic authentication using a username and password. Fingerprint recognition can only be used to reconfirm a logged-in user's identity.

# Requirements

*   The mobile device must have a fingerprint sensor, such as Touch ID for iOS devices.
*   The user has a registered fingerprint with the device.
*   The username and password saved in the app must belong to the same user whose fingerprint is saved on the device.
*   The user is logged into the app. The app must use Rakuten Ecosystem Mobile SDK's user library to store the username and password of the user in the account manager (for Android) or keychain (for iOS).

# Why should I use Fingerprint Recognition?

Fingerprint recognition is a great way to simplify the login process for your users. Rakuten fingerprint recognition also offers an end-to-end option for error handling and server authentication, as well as support for enabling and disabling fingerprint recognition in the app. If fingerprint recognition is not working, the app falls back to username and password credentials, ensuring that users do not get locked out of your app.

# How does Fingerprint Recognition work?

Let's say a user is performing a sensitive task â€” such as changing account details, viewing payment details or changing a delivery address â€” and the app needs to re-confirm the user's identify.

The user is presented with the following dialog box:

![Touch id prompt](../images/img_fingerprint_prompt_169_300.png) 
On this screen, the user can swipe their finger on the sensor or Touch ID, and their identity will be reconfirmed.

If the user presses Cancel above, they are shown the following dialog box which allows them to enter password and verify their identity.

![Cancel Touch ID prompt](../images/img_fingerprint_prompt_cancel_169_300.png)

If user selects Enter Password, they are shown the following identity confirmation dialog box:

![Enter Password Screen Shot](../images/img_fingerprint_enter_password_screen_169_300.png)

# What does the User Interface for Fingerprint Recognition look like?

#### Android:

The following screens show the identity confirmation popups and fallback UI to enter password for Android. This UI is provided by the Rakuten Ecosystem Mobile SDK.

![Fingerprint-android-ui](../images/img_fingerprint_android_ui_1024_390.png)

#### iOS

The following screens show the identity confirmation popups and fallback UI to enter password for iOS. This UI is provided by the Rakuten Ecosystem Mobile SDK.

![Fingerprint-ios-ui](../images/img_fingerprint_ios_ui_1024_836.png)

# How do I set up Fingerprint Recognition for my app?

You must install the Rakuten Ecosystem Mobile SDK and certain modules to use fingerprint recognition. For Android apps, you need to install the [user module](http://www.raksdtd.com/android-sdk/user-4.0). For iOS apps, you need to follow the [RBuiltinVerification Workflow](http://www.raksdtd.com/ios-sdk/authentication-3.9/interface_r_builtin_verification_workflow.html).

#### Android

For new apps on Android devices, see [Installing the SDK (New Project)](http://www.raksdtd.com/android/installing-sdk-new/) to install the SDK. See the [User Module Tutorial](http://www.raksdtd.com/android-sdk/user-4.0) to install the user module. You can also access [sample code](https://gitpub.rakuten-it.com/projects/ECO/repos/core-android-user/browse) for the user module.

For existing apps on Android devices, see [Installing the SDK](http://www.raksdtd.com/android/installing-sdk/) to install the SDK. See the [User Module Tutorial](http://www.raksdtd.com/android-sdk/user-4.0) to install the user module. You can also access [sample code](https://gitpub.rakuten-it.com/projects/ECO/repos/core-android-user/browse) for the user module.

#### iOS

For new apps on iOS devices, see [Installing the SDK (New Project)](http://www.raksdtd.com/ios/installing-sdk-new/) to install the SDK. See the [RBuiltinVerification Workflow](http://www.raksdtd.com/ios-sdk/authentication-3.9/interface_r_builtin_verification_workflow.html) for workflow information. You can also access [sample code](https://gitpub.rakuten-it.com/projects/ECO/repos/core-ios-authentication/browse/Samples/VerificationWorkflow) for the workflow.

For existing apps on iOS devices, see [Installing the SDK](http://www.raksdtd.com/android/installing-sdk/) to install the SDK. See the [RBuiltinVerification Workflow](http://www.raksdtd.com/ios-sdk/authentication-3.9/interface_r_builtin_verification_workflow.html) for workflow information. You can also access [sample code](https://gitpub.rakuten-it.com/projects/ECO/repos/core-ios-authentication/browse/Samples/VerificationWorkflow) for the workflow.

# How do I test Fingerprint Recognition?

You can manually test fingerprint recognition in a simulator.

You can also obtain BDD scenarios from the Rakuten Ecosystem Mobile SDK's QA team. Email ecosystem-mobile@mail.rakuten.com for more information.

# Additional Resources:

[Roadmap for Rakuten Ecosystem Mobile SDK](https://confluence.rakuten-it.com/confluence/display/SSEDPT/REM+-+Roadmap+2017)

Rakuten Ecosystem Mobile SDK guides:

*   [Android guide](http://www.raksdtd.com/android/)
*   [iOS guide](http://www.raksdtd.com/ios/)

Rakuten Ecosystem Mobile SDK Reference Documentation:

*   [Android documentation](http://www.raksdtd.com/android-sdk/)
*   [iOS documentation](http://www.raksdtd.com/ios-sdk/)

See the [FAQ page](../../04_faq) for frequently asked questions or contact us via
[Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) for support.