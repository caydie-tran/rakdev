---
title: Android SDK FAQ
layout: helpcenter-mobile
parent: _helpcenter-mobile/faq.md
categories: [ecosystem, analytics, mobile, android, faq]
weight: 6
---

1. How does Android Single Sign-On work?

The Android User Module uses the Android system Account Manager to store user login information and tokens.

Only the first application that uses the User Module can install or upgrade the account authenticator of the user module. All subsequent applications cannot update the account authenticator of the user module, even if they include a newer version of the user Module. This is an Android limitation. For this reason, it is important for developers to always release an update once a new version of the user Module is available, so that all users have the latest version of the User Module.

Due to these limitations, User Module functionality is frozen as of version 3.1. Any application that includes the User Module must include 3.1. Further updates will only be applied for critical security issues.

Supported:

* SSO
* Ichiba login
* Ichiba cookie login
* Global login
* Books login
* Standardized UI (optional)
* Not supported: Login without SSO (The User module has been rewritten from version 2.4, and is not backward compatible.)