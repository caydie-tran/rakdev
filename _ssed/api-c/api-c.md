---
layout: ssed
permalink: /ssed/api-c/
weight: 2
category: api-c
title: Api-c
---


## API C

### Introduction 
Real-time mobile app crash tracking/reporting. 

### Software Requirements
- API 15 or higher

### Installation
1.	Include Subscription ID in AndroidManifest as MetaData:

    ```
    <meta-data android:name="com.rakuten.tech.mobile.relay.SubscriptionKey"
        android:value="${Subscription-ID}" />
    ```

2.	In the build.gradle of your android application include:

    Import (Production):

    ```
    compile 'com.google.android.gms:play-services-iid:11.0.4'
    ```

    ```
    compile 'com.rakuten.tech.mobile:crash-reporting:0.2.0'
    ```

    If your application alreayd includes google play-services:

    ```
    compile ('com.rakuten.tech.mobile:crash-reporting:0.2.0') {
            exclude group: 'com.google.android.gms', module: 'play-services-iid'
        }
    ```

### Getting Started
1.	If Crash Reporting has successfully compiled in the app, it will work immediately when the app runs without inserting any further code.

### Custom Keys
Associate arbitrary key/value pairs with your crash reports.

  ```
  CrashReport.getInstance().setBoolean(String key, boolean value);
  ```

  ```
  CrashReport.getInstance().setDouble(String key, double value);
  ```

  ```
  CrashReport.getInstance().setFloat(String key, float value);
  ```

  ```
  CrashReport.getInstance().setInteger(String key, int value);
  ```

  ```
  CrashReport.getInstance().setString(String key, String value);
  ```

### Custom Logs
Associate logs with your crash reports.

  ```
  CrashReport.getInstance().log(String message);
  ```
