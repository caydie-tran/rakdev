---
title: Push Notification Platform (PNP)
layout: page
parent: _esd/helpcenter-mobile.md
categories: [Ecosystem, Analytics, Mobile, Android, iOS, pnp, push notification]
---


## What are Push Notifications?

Push notifications are messages sent by a service to an application on a mobile device. It is enabled as a service by the Push Notification Platform (PNP) on the Rakuten Ecosystem Mobile. Mobile devices must be registered to receive Push notifications. Registration can be enabled or disabled through the application or server.

Push notifications are supported on Android, iOS and Windows.

![Push Notifications](../images/img_push_notifications.png)

Here's how it works:

![Push Notifications - How it works](../images/img_push_notifications_map.png)



## Registering for Push Notifications” External API Invocation

1.  The app tells the SDK that the device wants to be able to receive messages.
2.  The SDK tells Rakuten App Engine (RAE) that the app wants to call PNP.
3.  RAE authorizes the app's RAE Credentials and forwards the request to PNP.
4.  PNP authorizes the app's PNP Credentials and registers the device.
5.  The app on the device can now receive messages from the server.

The app requests to unregister or stop receiving messages using the same process.

## Sending Push Notificationsâ€” Internal API Invocation

1.  The server of the app tells PNP that it wants to send a message to a target. This message can be composed programmatically or manually via the [PNP Dashboard](https://confluence.rakuten-it.com/confluence/display/PNPD/PNP+Dashboard+Links).
2.  PNP authorizes the PNP Credentials of the app and queues the request to send to Google Cloud Messaging (GCM) Service or Apple Push Notification Service (APNS). The GCM key or APNS certificate of the app is used in this step.
3.  GCM or APNS sends the message to the target app.

## Why should I use Push Notifications?

### Increase retention and engagement

Push notifications improve application retention and engagement by messaging the user and keeping them in contact with the application. You can also send promotions and alerts to your customers.

### Target users

You can create custom Push notifications for specific segments of your user base to make sure you are sending your audience the most relevent information for their needs. You can also link Easy IDs or Global IDs to user devices, or target individual users.

### Schedule and Manage Messages

You can track Push notification status and history on the [PNP Dashboard](https://confluence.rakuten-it.com/confluence/display/PNPD/PNP+Dashboard+Links), as well as schedule upcoming Push notifications. Limit the number of messages sent at one time and set a schedule to distribute the message.

## How do I set up Push Notifications for my application?

## Step 1: Request a RAE Scope

Your application must have RAE to invoke the PNP API. Request an [ID and the necessary scope](https://confluence.rakuten-it.com/confluence/display/RAED/2-2.++Application+client_credentials#id-2-2.Applicationclient_credentials-Createapplicationticket) if you do not have a RAE client ID.

You can check which [APIs](https://confluence.rakuten-it.com/confluence/x/JbPeAg) you need to invoke to determine the corresponding scope. You can find the available RAE scopes [here](http://ws-jenkins.stg-jpe1.rakuten.rpaas.net/job/rae.document/lastSuccessfulBuild/artifact/dist/index.html#/main).

## Step 2: Get Google/Apple Keys or Certificates

You need to request keys or certificates in order to send push notifications depending on the platform of the device.
You must have a [GCM key](https://developers.google.com/cloud-messaging/gcm#key) for Android devices. This key is required in the PNP Dashboard.
You must [entitle your app for push notifications and get a certificate](https://confluence.rakuten-it.com/confluence/display/PPA/iOS+Push+Notifications+Guide) for iOS devices. The certificate and password is required in the PNP Dashboard.
You can use official Rakuten accounts to obtain these requirements. Please enter [a request](https://officerakuten.sharepoint.com/sites/list/SDTD/MOBILEECO/MOBILESTAND/_layouts/15/viewlsts.aspx) to the Mobile App Management team for assistance.

## Step 3: Register your app to PNP

The [PNP Dashboard](https://confluence.rakuten-it.com/confluence/x/1AxdAg) is a user interface where you can manually send messages and/or manage the push notification settings of your service. You need PNP-specific credentials in order to invoke the API. Please see [here](https://confluence.rakuten-it.com/confluence/x/YPZRK) for more information. You must set the administrator for the PNP Dashboard when you send the request.

## Step 4: Set up the SDK for your app

Please see [here](http://www.raksdtd.com/android-sdk/push-latest/) for Android instructions.
Pleas see [here](http://www.raksdtd.com/ios/push-notifications/) for iOS instructions.

## Timeline

PNP setup takes about six business days to complete. Please contact the mobile teams directly for expedited requests.

![Timeline](../images/img_timeline.png)

## How do I send a Push Notification?

There are two ways to send a message after setting up your app: automatic and manual. The current distribution limit is 10,000 messages per minute per request.
See [here](https://confluence.rakuten-it.com/confluence/x/NoqMDw) for the latest load test results.

## Automatic Sending

You can use the [bulk push API](https://confluence.rakuten-it.com/confluence/x/RBkYEw) to send messages to specific targets. PNP Credentials are required.

### Android Example (PHP)
```php
/**
/**
 *
 * @param string $pushType The type of notification
 * @param string $message The title
 * @param string $message The message
 * @param string $data JSON encoded extra data to send
 * @param array $easyIds An array of easy ids to send the message to
 * @param string $gcmKey Google Cloud Messaging key
 *
 * @return mixed The result of the query or FALSE on failure
 */
public function bulkPushAndroid($pushType, $data,
        $easyIds, $gcmKey)
{
    // urls = http://api.pnp.db.rakuten.co.jp/api/
    // self::DEVICE_ANDROID = android
    $url = $this->urls[$this->env] . 'bulkpush/' . self::DEVICE_ANDROID;
    $params = array(
        'pnpClientId' => $this->pnpClientId,
        'pnpClientSecret' => $this->pnpClientSecret,
        'pushtype' => $pushType,
        'key' => $gcmKey,
        'data' => $data,
        'easyid' => implode(',', $easyIds),
    );
    $pnpParams = Yii::app()->params->itemAt('pnp');
    if (isset($pnpParams['reporting'])) {
        $params['reporting'] = $pnpParams['reporting'];
    }
    $resultXml =  $this->curlPost($url, $params);
    $result = self::parseResultXml($resultXml);
    return $result;
}
```

### iOS Example (PHP) 

```php
/**
 *
 * @param string $password APNS password
 * @param string $alert The ticker text to show
 * @param int $badge The number of the badge
 * @param string $sound the type of sound to play
 * @param string $pushType The type of notification
 * @param string $easyIds An array of easy ids to send to    
 * @param array $custom Custom values
 *
 * @return mixed The result of the query or FALSE on failure
 */
public function bulkPushIos($password, $alert=null, $badge=0, $sound='default',
        $pushType = null, $easyIds = null, $custom = null)
{
    if ($password == null) {
        throw new InvalidArgumentException('$password is null');
    }
    // urls = http://api.pnp.db.rakuten.co.jp/api/
    // self::DEVICE_ANDROID = ios
    $url = $this->urls[$this->env] . 'bulkpush/' . self::DEVICE_IOS;
    $params = array(           
        'pnpClientId' => $this->pnpClientId,
        'pnpClientSecret' => $this->pnpClientSecret,
        'password' => $password,
        'badge' => $badge,
        'sound' => $sound,
        'reporting' => '',
    );
   
    //add custom params
    if ($pushType != null) {           
        $params['pushtype'] = $pushType;
    }
    
    if ($easyIds != null && is_array($easyIds)) {
        $params['easyid'] = implode(',', $easyIds);
    }
    
    if ($alert != null) {
        $params['alert'] = $alert;
    }
    if ($custom != null) {
        $params['custom'] = json_encode($custom);
    }
    $resultXml =  $this->curlPost($url, $params);       
    return self::parseResultXml($resultXml);       
}
```

## Manual Sending

Go to the [PNP Dashboard](https://confluence.rakuten-it.com/confluence/x/1AxdAg) and login with your Rakuten Intra account. Please follow [this guide](https://confluence.rakuten-it.com/confluence/x/_J6MDw) on how to send a message.

# Testing

You must have the following before you test Push Notifications:

*   Check that your app has been setup correctly.
*   Your app is connected to Rakuten Intra network (r-dev or r-byod WIFI) to test in the staging environment.
*   The server sending the message is connected to Rakuten Intra network.
*   You are logged into a staging account, if you are using user_credentials for RAE authentication. Prepare the EasyID of the test user.
*   Regular and 24/7 RAE environments in staging are connected to PNP staging.

Testing Push Notification

1.  Create a simple text file containing the target EasyID. Only one EasyID per line is permitted. The file should be in UTF-8 format.
2.  Register the target user for Push notifications using your app.
3.  Send a push notification in any of the following three ways
    1.  Using your server.
    2.  Using our [Postman Collection](https://rakuten.atlassian.net/wiki/download/attachments/273286588/PNP1.0-Basic_Sending.json.postman_collection?version=1&modificationDate=1461217330199&api=v2). You need to install [Postman](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=en) first if you want to use it.
        If you already have it, import the collection. Choose ios or android.
        Enter your pnpClientId and pnpClientSecret.
        Upload the easy ID list file you created in step 1.
        For iOS, enter your message in the â€œalertâ€ parameter.
        For Android, enter your message as a JSON format in the â€œdataâ€ parameter.
        Click Send.
    3.  Using the PNP [Dashboard](https://confluence.rakuten-it.com/confluence/x/_J6MDw).
4.  The device should receive a message. Please see below for an example in iOS.[img_notiication](img_notification.png)]
5.  View the message log in the [Dashboard](https://confluence.rakuten-it.com/confluence/display/PNPD/2-7.+Viewing+Reports#id-2-7.ViewingReports-SentMessageDetailReport%28AppOpens/PushErrorResponse%29).

## Additional Resources

[Roadmap for Rakuten Ecosystem Mobile SDK](https://confluence.rakuten-it.com/confluence/display/ESD/REM+-+Roadmap+2016)

SDK Reference Documentation:[](http://www.raksdtd.com/ios-sdk/)

*   [Android SDK](http://www.raksdtd.com/android-sdk)
*   [iOS SDK](http://www.raksdtd.com/ios-sdk)

You can file a bug or fill out an Inquiry Form [here](https://confluence.rakuten-it.com/confluence/display/REMI/REM+Inquiry+form).

You can also contact the [Support team](http://www.raksdtd.com/support/) with any SDK issues.

*   [PNP Home Page](https://confluence.rakuten-it.com/confluence/x/MYDIAw)
*   [REM SDK Documentation](http://www.raksdtd.com/sdk/)
*   [RAE Home Page](https://confluence.rakuten-it.com/confluence/x/-gX9JQ)

</div>