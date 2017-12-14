---
title: Card Info
layout: page
parent: _helpcenter-mobile/features.md
categories: [ecosystem, card, mobile, android, ios, card, card info]
---

## What is Card Info?

CardInfo is a REM SDK module that enables users to enter their credit card information by scanning their credit cards using their mobile device's camera, or manually enter their card information. With CardInfo, the device's camera is able to:

*   Scan the credit card number
*   Associate the scanned credit card number to a credit card type
*   Scan the credit card expiration month and year

![scan card UI](../images/img_scan_card_ui_174_300.jpg)[Â ](http://www.raksdtd.com/wp-content/uploads/2016/09/scan-result-UI.jpg)![scan result UI](../images/img_scan_result_ui_173_300.jpg)

## Software and Hardware Requirements

| Platform | Software REquirements | Hardware Requirements |
| -------- | --------------------- | --------------------- |
|![Android icon](../images/img_android_icon.png)|Android SDK 4.0.3 (API 15) or higher| ARM7 or higher |
|![Apple icon](../images/img_apple_icon.png)|iOS version 8 or higher| ARM7 or higher |
|||

## How does CardInfo work?

#### 1. Set the required credit card information

YouÂ can set which credit card information is required from your users:

*   Credit card Number
*   Credit card Type
*   Credit card expiration month and year
*   CVV number
*   Card holder's name

#### 2. Set supported credit card types

You can set which credit card typesÂ are accepted:

*   American Express
*   Diners Club
*   JCB
*   Master Card
*   Union Pay
*   VISA

#### 3. User scans a credit card

Using the camera on their mobile device, the user scans their credit card.

#### 4. User confirms card information

A confirmation UI screen appears, and the user confirms the credit card that they scanned. They may also enterÂ credit card information that was not scanned,Â such as the CVVÂ number.

## Why Should I Use CardInfo?

### Quick and Easy User Experience

Instead of tapping at least 16 buttons to enter the credit card number, users can just position the card in front of the camera to scan the card information. CardInfo also eliminates the risk of mistyping the credit card number, and having to enter it again.

### Secure and Protected Information

The CardInfo SDK does not store or transmit credit card numbers, making sure your users' credit card information is safe.

## SDK Documentation

* iOS: [CardInfo Guide for iOS Developers](http://www.raksdtd.com/ios-sdk/cardinfo-0.1/)
* Android: [Cardinfo guide for Android Developers](http://raksdtd.com/android-sdk/cardinfo-0.1/)