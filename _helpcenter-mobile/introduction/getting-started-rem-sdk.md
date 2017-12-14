---
title: Getting started with REM SDK
layout: page
parent: _helpcenter-mobile/introduction.md
categories: [Android, iOS, SDK, REM, tutorial]
---

This page is your gateway to using the **Rakuten Ecosystem Mobile SDK (REM SDK)** in your iOS or Android apps. You need certain app credentials depending on the REM SDK features you use to integrate the SDK in your app.

NOTE: You must have access to **[GitPub](https://gitpub.rakuten-it.com/)** to use the iOS SDK. If you are affiliated with Rakuten, join the **dev-gitpub-user** mailing list using [DLM](https://dlm.rakuten-it.com/) to request access to GitPub. The name of the project is [ECO](https://gitpub.rakuten-it.com/projects/ECO). If you are not affiliated with Rakuten, [click here](https://confluence.rakuten-it.com/confluence/display/GDT/For+access+appication+to+use+R-Atlassians+from+an+external+network) for more information.

## App Versioning

When using the REM SDK, we recommend that your App version follows [Semantic Versioning 2.0](http://semver.org/).
Following Semantic Versioning helps the REM team to provide a better support and accurate analytics for your App.

## REM SDK Technical Documentation
See the iOS and Android platform specific pages for links to the REM SDK, tutorial articles and developer documentation:

![Android icon](img_android_icon.png) [Android SDK API Reference Documentation](http://raksdtd.com/android-sdk/)

![iOS icon](img_ios_icon.png) [iOS SDK API Reference Documentation](http://www.raksdtd.com/ios-sdk/)


## App Credentials

| App Credentials | Description|
| -- | -- |
| RAE | Required to access Rakuten App Engine (RAE)  APIs (Authentication, Points, Push, etc). |
| Ping App ID | Required to use the Force Update feature |
| PNP | Required to use the Push Notification Platform (PNP) service |
| RAT | Required to use the Rakuten Analytics Tracker (RAT) service |
| Feedback | Required to use the Feedback feature on REMS |
| Ping | Required to use the Ping feature on REMS |
| Discover | Required to use the Discover feature on REMS |

For details, please read below

### RAE Credentials

1.  Get Rakuten App Engine (RAE) credentials by obtaining a _client-id_ and _client-secret_ for both staging and production for your preferred environment from OSPD. Your environment can be either regular or 24Ã—7.
2.  Fill out and submit this form: **[RAE Application](https://confluence.rakuten-it.com/confluence/display/RAED/1-1+Rakuten+App+Engine%3A+Create+RAE+Client+ID)**

### Request RAE Scopes

Make sure that the necessary scopes are granted for your application.
Request RAE Scopes from [here](https://developers.rakuten.com/hc/en-us/articles/115005020348-Client-ID-Management-Module-Dashboard-User-Guide-for-Rakuten-App-Engine-RAE-).

*   memberinfo_read_name €“ required scope for login on iOS

### Ping Application ID

You need a _ping application id_, for both staging and production, to use the Force Update feature.

Use the [REM Inquiry Form](https://rakuten-esd.zendesk.com/hc/en-us/requests/new?ticket_form_id=399907) to request a ping account.

### PNP Credentials

You need a Push Notification Platform (PNP) _client-id_ + _client-secret_ credentials for both staging and production, as well as a _sender id(Android only/Provided by GCM)_. Click [here](https://confluence.rakuten-it.com/confluence/display/PNPD/2-1.+Getting+Started) to learn more about PNP.

Fill out and submit the [PNP Application](https://confluence.rakuten-it.com/confluence/display/PNPD/Push+Notification+Platform%3A+Create+New+PNP+Client+ID) to obtain PNP credentials.

### RAT Credentials

You need an _account id_ and an _application id_ to use Rakuten Analytics Tracker (RAT).
Click here [here](https://confluence.rakuten-it.com/confluence/display/RAT/RAT+Home) to learn more about RAT.

Fill out and submit the [RAT Application](https://confluence.rakuten-it.com/confluence/display/RAT/RAT+Introduction+Application+Form) form to obtain RAT credentials.

### Enable Feedback on REMS

Your app must be registered in Rakuten Ecosystem Mobile Service (REMS) to use the Feedback feature.

Request a Feedback account through the [Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) with your application Bundle id (iOS)/Package name (Android), and admin email.

### Enable Ping on REMS

Your app must be registered in Rakuten Ecosystem Mobile Service (REMS) to use the Ping feature. The Ping Application ID is provided after the REMS Ping account is created.

Request a Ping account through the [[Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) with your application Bundle id (iOS)/Package name (Android), and admin email.

### Enable Discover

Your app must be registered in Rakuten EcoSystem Mobile Service(REMS) and [Rakuten API Portal](https://remsapijapaneast.portal.azure-api.net/) to use the Discover feature.

Service ID and Subscription Key is provided after the REMS Discover account is created.
Request a Discover account through the [Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) with your application Bundle id (iOS)/Package name (Android), admin email, and list of applications you want to promote.