---
title: Authentication with Single Sign-on
layout: helpcenter-mobile
parent: _helpcenter-mobile/features.md
categories: [Ecosystem Analytics Mobile Android iOS SSO single sign on authentication]
permalink: /helpcenter-mobile/features/single-sign-on/
weight: 13
---

## What is User Authentication?

**User Authentication** is a Rakuten Ecosystem Mobile feature that enables users to sign into your application using their Rakuten ID. Features of the User Authentication module include:

*   Login/Logout: Users can login or logout of their accounts on the provided login/logout page.
*   Basic User Information: Through **User Authentication**, you can view basic information about the user after they login, such as their name, birthday and gender.
*   Remember Me: Users can set the login/logout page to remember their login credentials.
*   Forgot Password: Users can receive a new password if they have forgotten their old one.
*   Standardized User Interface: The User Authentication module comes with a ready-to-use user interface that you can integrate into your app. You can also create your own user interface to fit the style of your app.

User Authentication is required for enabling Single Sign-on in your app. Single Sign-on automatically signs users in or out of all other Rakuten applications after they sign in or out of any Rakuten application.

Here's how it works:

1.  Install the Rakuten Mobile SDK Module into your application. See: [Installing the Rakuten Mobile SDK](../04_getting_started_with_rem_sdk)
2.  Install the **User Authentication Module** into your app.
3.  Create a Login/Logout page.
4.  User enters their Rakuten ID and password.
5.  Rakuten Membership Service verifies the Rakuten ID and password of the user through the Rakuten Mobile SDK Module.
6.  If the login information is correct, your application gains access to the user's account details, Rakuten Super Points and shopping history.

![sso main](../images/img_sso_article_banner_300_173.png)

## Why should I use User Authentication?

#### Leverage more than 70 million Rakuten members

Rakuten's membership program is the cornerstone of the Rakuten Ecosystem. A user's Rakuten ID connects them to Rakuten products and services, and tracks their activity to provide a better experience for both the user and Rakuten merchants. User Authentication is an essential component of every Rakuten application.

#### Don't force users to remember another User ID

Many users may not want to create a different Rakuten ID just for your application. User Authentication is the easiest way for users to log into your application without juggling different accounts. 

![sso mobile app](../images/img_sso_mobile_app_ui_169_300.png)

#### Seamlessly transition between Rakuten applications

The Single sign-on component of User Authentication ensures a smooth changeover from other Rakuten applications into your application, creating a better overall experience for users.

#### Significantly cut down login time

Having to remember and type a password can significantly increase login time and the chances of a failed login. SSO can enable users to skip this step and start using your App right away.

| Average Time Spent (non-SSO) | Average Time Spent (SSO) | Login Time Reduction Rate |
| -- | -- | -- |
| 88 sec | 5 sec | 94% |

_* Source: Site Catalyst report for Rakuten Ichiba Android App during October 2016_

#### Step 1: (Single Sign-on Only) Apply for Whitelist

You must apply for your app to be whitelisted to use the Single Sign-on feature in your application. You can use the [Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) to confirm that your application is compatible with User Authentication and request to have your application whitelisted. Include your app's Application ID in the request.

#### Step 2: Install the Rakuten Ecosystem Mobile SDK

You must download and install the Rakuten Ecosystem Mobile SDK into your application's codebase before you can add Rakuten Mobile SDK features to your app. You can download the SDK for your Android or iOS from the [REM SDK page](http://www.raksdtd.com/sdk/).

#### Step 3: Install the User Authentication Module

You can add other Rakuten Mobile SDK features after the Rakuten Ecosystem Mobile SDK is installed in your application. See the [REM SDK Android](http://www.raksdtd.com/android/) guide for a step-by-step guide on installing the User Authentication module in your Android application. See the [RAuthentication Builtin UI](http://www.raksdtd.com/ios-sdk/authentication-3.3/authentication-ui.html) page for a step-by-step guide on installing **User Authentication** into your iOS application.  

#### Step 3: Create a Login/Logout page

Many Rakuten Mobile SDK features include a mobile user interface, which is standardized and tested by the Rakuten Ecosystem Mobile team. You can use this UI to save time on application development and provide the user with a uniform experience across Rakuten applications. See the [guide for a step-by-step guide on creating login/logout UI in your Android application.]("http://www.raksdtd.com/android-sdk/user-4.0/</a) See the [RAuthentication Builtin UI](http://www.raksdtd.com/ios-sdk/authentication-3.3/authentication-ui.html) page for a step-by-step guide for creating login/logout UI in your iOS app. When you logout, the UI asks you to choose whether to only logout from current app or to logout from all apps on this phone. [![SSO logout](http://www.raksdtd.com/wp-content/uploads/2015/09/SSO-logout-300x230.png)](http://www.raksdtd.com/wp-content/uploads/2015/09/SSO-logout.png)

## Testing User Authentication

#### Test Login Verification

Enter your Rakuten ID and password on your Login/Logout page. If the login is successful, Rakuten Membership Services can verify users' login credentials, and your app is working properly.

#### Test Single Sign-on

Sign into your app with your Rakuten ID and open a different Rakuten application that supports Single Sign-on. If Single Sign-on is working properly, you will remain logged into your account in all other Rakuten applications.

## Additional Resources

* [Roadmap for Rakuten Ecosystem Mobile SDK](https://confluence.rakuten-it.com/confluence/display/SSEDPT/REM+-+Roadmap+2017) 
* [iOS SDK Reference Documentation]](http://www.raksdtd.com/ios-sdk/) 
* [Android documentation](http://www.raksdtd.com/android-sdk)

Contact us through our [Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) for any User Authentication questions.