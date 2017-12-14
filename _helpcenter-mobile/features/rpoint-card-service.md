---
title: RPoint Card Service
layout: page
parent: _helpcenter-mobile/features.md
categories: [Ecosystem, Analytics, Mobile, Android, iOS, RPoint, RPoint card service]
---

## What is RPointCard Service?

**RPointCard** enables shoppers to spend **Rakuten Super Points** at physical points of sale (POS). It works exactly like a physical plastic card, giving Rakuten members the flexibility to leave their cards at home. **RPointCard** is a module included in the **Rakuten Ecosystem Mobile SDK**. It can be added to any application without depending on external modules. **RPointCard** has been tested on a multitude of iOS and Android devices, as well as on the most widely used barcode scanners in the Japanese market. Here's how it works:

1.  Users receive a unique barcode
2.  Users present barcodes at points of sale
3.  Users choose to earn or spend their Super Points

![How RPoint Card Works](../images/img_rpointcard_banner.png)

**Use Case:** Point Partner uses the **RPointCard** service as an alternative a physical card. Point Partner users can use their phone to redeem points without having to carry their physical card. Users also have access to their Super Point and can stay up to date on campaign information configured by the Point Partner BU.

## Why Should I Use RPointCard SDK?

**Delight the user with convenience** Today, most Rakuten users carry smart phones with them most of the time. As **RPointCard** serves the same purpose as a plastic card, users have the flexibility to make their wallets a little less bulky. 

**Enhance customer loyalty** When users make purchases or earn or spend Rakuten Super Points with your app, targeting them for further conversions is just a push notification or application update away.

## Included Features

All included features, listed below, contain built-in UIs and code libraries that can connect with backend services and APIs.

## 1. One Time Barcode Generation (OTB)

Unique barcodes are automatically generated and assigned to users for a period of time. Barcodes do expire, but they are automatically recreated without the user noticing.

*   View [OTB specifications](https://confluence.rakuten-it.com/confluence/display/PPA/App+Launch%3A+Functional+Specs).


| Scenario | User Interface|  |
| -- | -- | -- |
| Barcode displayed to user  | ![Barcode Displayed to user](../images/img_rpointcard_barcode_displayed_to_user.png) | |
| Black-list screen displayed to users on unapproved devices | ![Black list screen ](../images/img_rpointcard_black_list_screen.png) | During testing (QA) phase if it is dicovered that a certain type of device does not works with scanners (which scan the bar code), it is black listed. The app will get installed but the barcode won€™t appear. |
| Gray-list screen displayed to users on untested devices | ![Grey list screen ](../images/img_rpointcard_grey_list_error.png) | During testing (QA) phase if it is discovered that a certain type of device has low €œscanability€ with scanners (which scan the bar code), it is grey listed. For grey listed devices, a warning message is shown to the user before displaying bar code. User can cancel this message and view the bar code. |
| Maintenance message displayed to users when applicable | ![Maintainance Mode](../images/img_rpointcard_maintainance_mode.png) | |


## 2. Collecting user credentials

Users must supply the following information before using RPointCard:

1.  User ID
2.  Name
3.  E-mail address
4.  Date of birth
5.  Gender
6.  Address
7.  Phone number

Your app may have already collected some or all of this information from users. If any information is missing, shoppers are prompted to login and supply the remaining information during their first attempt to access RPointCard functionalities. The information collected is not stored on Client side by the app, instead it uses a secure API to store it in the Rakuten servers.

*   View [App Launch: Functional Specifications](https://confluence.rakuten-it.com/confluence/display/PPA/App+Launch%3A+Functional+Specs). (external link to confluence)

#### User Interface

![User Interface](../images/img_rpointcard_user_credentials.png)

## 3. Terms and Conditions

Users must agree to the terms and conditions before using RPointCard. The terms & conditions are set by BU looking after the RPointCard. These terms and conditions must be shown to the user & their agreement should be sought. It's a mandatory legal requirement for using the RPointCard SDK.

#### User Interface

![Terms and Conditions](../images/img_rpointcard__terms_and_conditions_169_300.png)

*   View [App Launch: Functional Specifications](https://confluence.rakuten-it.com/confluence/display/PPA/App+Launch%3A+Functional+Specs).

## 4. Banner Service for Rakuten Products

1.  How are these banners created ?
2.  Where are they stored ?
3.  Do they appear as a Carousel ?
4.  Can user swipe left / right to see more banners
5.  What's the total number of banners that a user can see ?
6.  What sort of control does app developer have on these banners & their content
7.  What benefit do they bring to the app developer themselves ?

Your BU can configure campaign banners that are displayed to users below their barcode. Users can swipe between banners to view all configured content.

#### User Interface

![Barcode for user](../images/img_rpointcard_user_barcode_169_300.png)

*   View [App Launch: Functional Specifications](https://confluence.rakuten-it.com/confluence/display/PPA/App+Launch%3A+Functional+Specs). (external link to confluence)

## How Do I Get RPointCard for My App?

#### Step 1: Set up your Rakuten Ecosystem Mobile Services account

To set up your account:

1.  1.  Query via
[Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907)
    2.  Provide the following information:
        1.  The name of your product (it will be added as a service)
        2.  **Business User** contact information
        3.  **Developer** contact information
    3.  You will receive a response containing:
        1.  Login credentials for** Business Users** and **Developers**
        2.  Further instructions on setting up and enabling features

#### Step 2: Install the Rakuten Ecosystem Mobile SDK

Follow the directions here: [Getting started with REM SDK for iOS and Android](../04_getting_started_with_rem_sdk)

#### Step 3: Collect the following information:

*   Your App ID
*   Access token (from Rakuten)
*   Access token scope

You can use Rakuten Ecosystem Mobile SDK for getting Access token & Scope

#### Step 4: Implement RPointCard in your application

View the documentation as required

*   [Android](https://confluence.rakuten-it.com/confluence/display/PPA/Android+RPointCard+SDK+Integration+Guide) documentation
*   [iOS](https://confluence.rakuten-it.com/confluence/display/PPA/iOS+RPointCard+SDK+Integration+Guide) documentation

## Testing Your RPointCard Configuration

#### Simulator Application

Use any mobile application simulator to view and test the application used for **RPointCard SDK**.

## Additional Resources

To get started, please check the list of functionalities and functional specifications detailed over here.

*   [Functionality](https://confluence.rakuten-it.com/confluence/display/PPA/01.+Functionality) Check the functionality specs for RPoint Card SDK
*   [FAQs](https://confluence.rakuten-it.com/confluence/display/PPA/04.+FAQ) For frequently asked questions
*   [Change Log ](https://confluence.rakuten-it.com/confluence/display/PPA/05.+Change+log) Information about all the changes in SDK
*   [Samples](https://confluence.rakuten-it.com/confluence/display/PPA/03.+Samples) We also provide sample source codes and UI

For any queries regarding RPointCard, please contact us :  [Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907)Â  