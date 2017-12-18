---
title: Rakuten Super Points SDK
layout: helpcenter-mobile
parent: _helpcenter-mobile/features.md
categories: [Ecosystem, Analytics, Mobile, Android, iOS, rakuten super points, super points, points]
weight: 11
---

## What is Super Points SDK?

The **Points module** is a feature of the **Rakuten Ecosystem Mobile SDK** that enables users to view their **Rakuten Super Points** balance and rank-up information. Installing the **Points module** into your application will allow users to easily keep track of their Super Points without moving away from your application. The **Points module** includes:

*   Total Points Breakdown: Shows the user's limited term points, Rakuten cash, and Super Points.
*   Membership Status: Shows the user's Rakuten membership status.
*   Rank-up Information: Shows how many points the user needs to move to the next Rakuten rank.
*   myRakuten: Directs the user to their myRakuten page.
*   Rakuten Point Club: Directs the user to their Rakuten Point Club page.

Here's how it works:

1.  The user signs into your Points-enabled application with their Rakuten ID.
2.  Rakuten Membership Service verifies the Rakuten ID and password of the user through the **Rakuten Mobile SDK Module**.
3.  The user receives their Rakuten **Points** information on the **Points** screen.

## Why should I use Points?

#### Extra motivation for users

Many users are motivated to improve their Rakuten membership rank by making purchases. Implementing the Points module makes it easy for users to track their **Points** and show them how close they are to ranking up.

### Easy way to save

With the **Points module**, users can easily view their Rakuten Super Points. Knowing how much users can save on your products with Super Points will encourage them to make purchases in your shop.

## How do I set up Points for my application?

#### Step 1: Install the Rakuten Ecosystem Mobile SDK

Before you can add Rakuten Mobile SDK features to your Android apps, you must download and install the **Rakuten Ecosystem Mobile SDK** into your application's codebase. You can download the SDK for your Android or iOS from http://www.raksdtd.com/sdk/

#### Step 2: Install the Points Module

After the **Rakuten Ecosystem Mobile SDK** is installed in your application, you can add other Rakuten Mobile SDK features. For your Android application, please see [this tutorial](../13_super_points_android_integration) for a step-by-step guide on installing the **Points module** in your Android application. For iOS application, please see [this tutorial](../14_super_points_ios_integration) for a step-by-step guide on installing **Points**.  

## Testing Points

#### Test Points:

To test **Points**, simply sign into your app with a Rakuten ID. If your app displays the accurate Points information of the Rakuten ID, the **Points module ** is working correctly.

## Additional Resources

**Super Point SDK integration Tutorials**
* [Android tutorial](../13_super_points_android_integration)
* [iOS tutorial](../14_super_points_ios_integration)

**Rakuten Ecosystem Mobile SDK Roadmap**[Roadmap for Rakuten Ecosystem Mobile SDK](https://confluence.rakuten-it.com/confluence/display/SSEDPT/REM+-+Roadmap+2017)

**Rakuten Ecosystem Mobile SDK guides:**
*   [Android guide](http://www.raksdtd.com/android/)
*   [iOS guide](http://www.raksdtd.com/ios/)

**Rakuten Ecosystem Mobile SDK Reference Documentation:**

*   [Android documentation](http://www.raksdtd.com/android-sdk/)
*   [iOS documentation](http://www.raksdtd.com/ios-sdk/)

See the [FAQ page](../../04_faq) for frequently asked questions or contact us via
[Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) for support.