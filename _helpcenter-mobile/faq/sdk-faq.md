---
title: REM SDK FAQs
layout: helpcenter-mobile
parent: _helpcenter-mobile/faq.md
categories: [ecosystem analytics mobile android faq general rem sdk]
permalink: helpcenter-mobile/faq/sdk-faq/
weight: 2
---

1. Can I develop an app for Android Single Sign-On with Rakuten Global ID?

    Yes, you can develop an app for Android SSO with Rakuten Global ID.

2. Does the Single Sign-On SDK support the Sabun-toroku feature?

    Sabun-toroku is not supported at this time.

3. Can I log out of Single Sign-On without going to LogoutActivity?

    Yes. You can use LoginService#logout() as a programmatic logout.

4. What should I do if I receive the following error? "Application not allowed to access account"

    This error occurs if your application is not whitelisted. Rakuten Ecosystem Mobile does not include debug or unsigned applications in the whitelist due to security concerns. 
    
    Please try the following troubleshooting tips to resolve the error:

    1. Uninstall all Rakuten apps and install your own application as a debug (unsigned) build. 
    2. Uninstall all Rakuten apps and install another app with Single Sign-On (the TestUI sample,for example) as debug or unsigned build before installing your own application. The first application with Single Sign-On controls the account authenticator and the whitelist. If the first application is a debug application, the whitelist authentication will be disabled for all additional apps that access Single Sign-On.

5. How do I get a new app registered with the PNP service for OSPD?

    Please contact Push Notifications Platform team in ESD Department via email, or use the request form, to apply for new app registration.

6. How do I request "read" scope permission for Ichiba Order History?

    Please submit a Request for Search form.

    Please email [Shiono, Takao | Tak](mailto:takao.shiono@rakuten.com) to get approval to use Ichiba's purchase history data. Then, please email [Choe, Jungmin | Min](mailto:jungmin.choe@rakuten.com) to get SID of purchase history search engine by passing the query review. The purchase history SID should be separate for each RAE Client ID.
7. What versions of Android does the Rakuten Ecosystem Mobile support?

    The Rakuten Ecosystem Mobile supports Android versions Android 4.0.3 (SDK 15) to Android 6.0 (SDK 23).

8. What versions of iOS does the Rakuten Ecosystem Mobile support?

    The Rakuten Ecosystem Mobile currently supports iOS 7 or higher.

9. How can I access GitPub?

    NOTE: You'll need access to **[GitPub](https://gitpub.rakuten-it.com/)** to use the Android or iOS SDK. If you are affiliated with Rakuten, please join the **dev-gitpub-user** mailing list using [DLM](https://dlm.rakuten-it.com/) to request access to GitPub. The name of the project is [ECO](https://gitpub.rakuten-it.com/projects/ECO). 
    
    If you are not affiliated with Rakuten, please [click here](https://confluence.rakuten-it.com/confluence/display/GDT/For+access+appication+to+use+R-Atlassians+from+an+external+network) for more information.

10. What are the different types of Rakuten IDs?

        **JapanID** is the ID service used for applications in Japan. **GlobalID** is the ID service used for Global Applications. **EasyID** is the unique identifier for all the Rakuten Members worldwide, used internally within Rakuten. This is a sequentially generated number. Datatype of easyID is "int" (of Java). Its a 32 bit signed integer. The max value it can hold is "2,147,483,647". 
        
        Due to security policies, EasyID should not be used by client applications. **MemberID** is the unique identifier for all the Rakuten members outside Japan, used internally within Rakuten. Due to security policies easyIDs can not be shared with Group Companies, hence easyID is converted into another identifier called "memberID" and provided to group companies. MemberID is one-to-one mapped with easyID.