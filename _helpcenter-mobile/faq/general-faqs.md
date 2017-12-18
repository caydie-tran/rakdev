---
title: General FAQs
layout: helpcenter-mobile
parent: _helpcenter-mobile/faq.md
categories: [ecosystem, analytics, mobile, android, faq]
weight: 1
---

1.  How do the elements of Rakuten Ecosystem Mobile (REM) interact with each other?

    There are three diagrams that can help you understand the relationship of components, servers & services for the Rakuten Ecosystem Mobile:

    *  ![REM Component Diagram](../images/rem_component_diagram.png)
    *  ![REM Architecture Diagram](../images/rem_acrchitecture_diagram.png)
    *  ![Integration Diagram](../images/rem_integration_diagram.png)

2. How do I get an RAE Client ID for my app?

    Please fill out the following application form to apply for a Client ID: [1-1 Rakuten App Engine: Create RAE Client ID](https://confluence.rakuten-it.com/confluence/display/RAED/1-1+Rakuten+App+Engine%3A+Create+RAE+Client+ID)

3. Can I use existing RAE functions with the Ecosystem Mobile SDK?

    The Ecosystem Mobile SDK has a number of features that use existing RAE functions which include:

    *   Rakuten ID (Japan)
    *   Rakuten ID (Global)
    *   Points (Japan)
    *   Points (Global)
    *   Rakuten Analytics Tracker

    Please [contact us](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) if you need to use a different RAE component that is not a part of the Mobile SDK.

4. Does the Ecosystem Mobile SDK include Push notifications? Can we install the BAAS SDK in addition to the Mobile SDK?

    Yes, you can use the Push Notification Platform, also known as PNP, in the Ecosystem Mobile SDK. It uses the same PNP that is present in the BAAS SDK. Please see the [iOS](http://www.raksdtd.com/ios-sdk/) and [Android](http://www.raksdtd.com/android-sdk/) SDK documents for more information about the Push Notification SDK module.

5. Can an outside vendor access the REM portal site?

    Outside vendors can access the REM portal website if their IP address has been whitelisted. Please [contact the REM Portal team](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) to get an IP address whitelisted.

6. Where can I learn more about the Rakuten Analytics Tracking SDK (RAT)?

    Please see the [Analytics SDK](../../02_features/01_analytics_and_rat_sdk) articles for a reference on the Analytics SDK module. You can find links to other related documents on the following page: [Analytics_RAT](https://confluence.rakuten-it.com/confluence/display/REM/Analytics_RAT)

7. How do I get an Account ID and Application ID for the RAT SDK to integrate into my Android and iOS apps?

    You must register your apps with the following application form to get an Account ID or Application ID assigned to your apps: [01_RAT New Use Application](https://confluence.rakuten-it.com/confluence/display/GEAP/01_RAT+New+Use+Application)

8. How do I test our iOS and Android apps with the Analytics data in the staging environment?

    You can test the Analytics data with Kibana, a tool that shows how the Analytics data is sent out. Please see this page for more information on Kibana: [https://confluence.rakuten-it.com/confluence/display/GEAP/10.RAT+data+check](https://confluence.rakuten-it.com/confluence/display/GEAP/10.RAT+data+check)

    There is also a BI tool that allows you to see additional statistics. Please see the Log Analytics > (RAT)Log Analysis L1 * section of this page for more information: [https://confluence.rakuten-it.com/confluence/pages/viewpage.action?pageId=542459044](https://confluence.rakuten-it.com/confluence/pages/viewpage.action?pageId=542459044)
9. How does the Ping SDK module work, and how can I configure the Ping Admin page?

    Please see the [iOS](http://www.raksdtd.com/ios-sdk/) and [Android](http://www.raksdtd.com/android-sdk/) SDK docs for a reference on the Ping SDK module, along with the "Introduction to Ping" posts for [iOS](http://www.raksdtd.com/2016/02/05/an-introduction-to-ping-for-ios-developers/) and [Android](http://www.raksdtd.com/2016/02/05/an-introduction-to-ping-for-android-developers/). You can find links to other related documents on the following Confluence page: [Ping](https://confluence.rakuten-it.com/confluence/display/REM/Ping)

10. How do I start using the Ping Admin for Staging and Production?

        First, you must have a Ping user account. Please see the Introduction to Ping documentation for [iOS](http://www.raksdtd.com/2016/02/05/an-introduction-to-ping-for-ios-developers/) and [Android](http://www.raksdtd.com/2016/02/05/an-introduction-to-ping-for-android-developers/).

11. Can we control how our application reacts after receiving a ping status?

        Yes, the client application determines how it reacts when receiving a ping status.

12. Does the Ping SDK include a specific UI for the Force Update feature?

        Force Update does not currently have a specific UI, but we are working to provide one in the future.

13. How long does it take to reflect any updates done on the Ping Admin page?

        Ping Admin changes take about five to ten minutes to reflect updates.

14. Where can I learn more about Single Sign-On?

        Please see the [iOS](http://www.raksdtd.com/ios-sdk/authentication-latest) and [Android](http://www.raksdtd.com/android-sdk/user-latest) SDK documentation for more information on the User Authentication SDK module for Single Sign-On. 
        
        Additional information can be found on the following Confluence page: [User Authentication using](../../02_features/15_user_authentication_with_sso)

15. Does Single Sign-On support persistent settings?

        Yes, the Rakuten Ecosystem Mobile SDK remembers the credentials of the user after signing in through Single Sign-On.

16. How do I obtain an app ID for the Ping Service?

        Please create a request through the [inquiry form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) along with following information:

        * Service Name (App Display Name)
        * Package ID for Android/Bundle Id for iOS
        * Admin Email AddressPlease note that group mailing lists are not allowed to be Ping Admins. Please use a single user account when signing up.


17. Can I identify the users who receive Push notifications?

        Yes. You can get the list of successes and failures on the [Sent Message Detail Report](https://confluence.rakuten-it.com/confluence/display/PNPD/Sent+Message+Detail+Report).

18. Can I identify which users opened a Push notification?

        No.Â As of March 2016, PNP does not provide TrackingAPI. Please consider an external tool for tracking KPI, such as SiteCatalyst.

19. How do I get a new app registered with REMS?

        Please create a request through the [inquiry form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) along with the following information:

        * Service Name (App Display Name)
        * Package ID for Android/Bundle Id for iOS
        * Admin Email AddressREMS Environments: 
        ** STG: [https://ramses-staging.azurewebsites.net/](https://ramses-staging.azurewebsites.net/) 
        ** PRO: [https://rmservices.apps.global.rakuten.com/](https://rmservices.apps.global.rakuten.com/)

20. How do I get a new app registered with Apptimize?

        Please create a request through the [inquiry form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907).

21. What is global "mall_id"?

        mall_id is a static token for Global Shopping that differentiates between different marketplaces.

22. Does RAT needs to authenticate against Global ID?

        No, you do not need to use the Global id with RAT. The only requirement is to provide a string format: any user ID provided by an app team is compatible.

23. How long are RAE refresh tokens available after being published? What happens when refresh tokens expire?

     The Rakuten Ecosystem Mobile SDK provides a method to refresh the access token, using the refresh_token as a request parameter.
     
     The response to this request will include a new refresh_token. The app handles refreshing the access token if it is expired, or asks the user to login again. The refresh_token expiration must be longer than the access_token. If the refresh_token provided is invalid, the SDK returns an error.

24. The RAE client ID application form requires a service URL. What URL should I use for a new mobile app?

     If there is no URL for the service in your new mobile app, you can use a generic URL. Please note in a comment that your application is for a mobile-only service.