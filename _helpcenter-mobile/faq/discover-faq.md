---
title: Discover FAQ
layout: helpcenter-mobile
parent: _helpcenter-mobile/faq.md
categories: [ecosystem analytics mobile android faq discover]
permalink: helpcenter-mobile/faq/discover-faq/
weight: 4
---

1. I am a BU, what do I need to integrate Discover in my App?

    For Business Units in Japan, please contact CWDD at [mobile-eco-system@mail.rakuten.com](mailto:mobile-eco-system@mail.rakuten.com) 
    
    For business units outside Japan, please refer to [BU's Guide to Enable Discover feature](../../02_features/07_configure_discover_bu)

2. Where can I get credentials to integrate Discover in my App?

    For Business Units in Japan, please contact CWDD at [mobile-eco-system@mail.rakuten.com](mailto:mobile-eco-system@mail.rakuten.com) 
    
    For business units outside Japan, please refer to [BU's Guide to Enable Discover feature](../../02_features/07_configure_discover_bu)

3. I am an engineer, what do I need to integrate Discover in my App?

    Ask your BU to get the following credentials: 
    * Service ID
    * Application Name/ID
    * Discover API (Production and Staging) subscription keys 
    
    For Business Units in Japan, BU should get these credentials from COE (formerly CWD) at [mobile-eco-system@mail.rakuten.com](mailto:mobile-eco-system@mail.rakuten.com) 
    
    For business units outside Japan, please refer to  [BU's Guide to Enable Discover feature](../../02_features/07_configure_discover_bu)

4. I am an engineer, I got the credentials to integrate Discover but I do not know what to do with them.

    On Android

    * **my-application-id** refers to the name of the Application registered in REMS (i.e., viber_Android) 
    
    * **my-application-revision** refers to the version of your Application that will include Discover (i.e., 1.1.0) 
    
    * **my-service-id** refers to the identifier of your service in REMS (i.e., viber) 
    
    * **my-API-subscription-key** refers to the Discover API subscription key

    On iOS

    * **applicationNam** refers to the name of the Application registered in REMS (i.e., viber_iOS) 
    * **applicationVersion** refers to the version of your Application that will include Discover (i.e., 1.1.0) 
    * **serviceIdentifier** refers to the identifier of your service in REMS (i.e., viber) 
    * **authorizationKey** refers to the Discover API subscription key

    API documentation:

    * Android SDK: [http://www.raksdtd.com/android-sdk/discover-LATEST/](http://www.raksdtd.com/android-sdk/discover-LATEST/) 
    * iOS SDK: [http://www.raksdtd.com/ios-sdk/discover-LATEST/](http://www.raksdtd.com/ios-sdk/discover-LATEST/)

5. I am an engineer, where do I get the Discover API subscription keys?

    1. Using the credentials you got from your BU, login to [https://remsapijapaneast.portal.azure-api.net/](https://remsapijapaneast.portal.azure-api.net/)

    2. Navigate to the Profile page. ![Navigate to Profile Page](../images/img_click_show_to_display.png)
    
    3. Click "Show" to display the subscription key. ![Click Show to display subscription key](../images/img_click_show_subscription_key.png)

6. Discover API returns 404, Why?

    Please check if at least one app is marked as displayed in Discover ![Mark App as displayed in Discover page](../images/img_discover_404.png).