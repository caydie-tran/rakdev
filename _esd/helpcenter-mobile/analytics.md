---
title: What is Analytics?
layout: page
parent: _esd/helpcenter-mobile.md
categories: [Ecosystem, Analytics, Mobile, Android, iOS]
---

## What is Analytics?

The Analytics module enables developers to easily track data and KPI information in their applications. Features of Analytics include Rakuten Easy ID tracking and custom event tracking with custom parameters, such as genre and item identifiers.

Analytics also uses the Rakuten Analytics Tracker (RAT) extensively to manage analytics data and information.

Here's how it works:

1.  Developers implement the Analytics module into the app and create custom events and parameters.
2.  Data is sent to the Rakuten Analytics Tracker (RAT) when the app is in use and it triggers a tracked event. This data includes preset values and custom ones set by the developer.
3.  Data is extracted through a Hadoop client, such as Hive or Impala, and the RAT data is extracted into a JSON or CSV file. The data can also be visualized using the RAT Business Intelligence (BI) tool.
4.  The JSON output is processed and uploaded to DOMO or another visualizing tool.

![diagram analytics](../images/img_analytics.png)

## Why should I use Analytics?

#### Broader Scope for Data Tracking

Analytics data can be used jointly with other databases to track larger sets of results. Additionally, Analytics does not restrict what data is tracked in mobile apps, and Analytics can be used to track micro-level details such as scrolling and tapping.

#### Secured Data in Existing Rakuten Infrastructure

The Analytics module stores its data on the Rakuten Analytics Tracker to protect sensitive user information. This allows the sending of easy IDs, which is not possible with third-party solutions. The RAT team is also available for direct help and support.

## How do I set up Analytics for my app?

#### Step 1: Obtain credentials and ID

You need a RAT account â€” which includes an account ID, and service ID â€” to use Analytics. You can get a RAT account by filling out the [RAT Introduction Application Form](https://confluence.rakuten-it.com/confluence/display/RAT/RAT+Introduction+Application+Form). 

RAT assigns your Account ID. For example, you may use `1` for Rakuten Ichiba Japan, and `3` for Rakuten Books. A single account may have multiple services. You may want to consult with the account owner about naming the new service ID.

#### Step 2: Install the Rakuten Ecosystem Mobile SDK

You must download and install the Rakuten Ecosystem Mobile SDK into your applicationâ€™s codebase before you can add Rakuten Mobile SDK features to your apps. You can download the SDK for your Android or iOS [here](../../01_overview/04_getting_started_with_rem_sdk).

#### Step 3: Integrate the Analytics module and track events

The ready-to-use Analytics module is a collection of native libraries that allow mobile applications to send data directly to RAT. You can implement different trackers depending on your platform:

*   [Android Trackers](http://www.raksdtd.com/android-sdk/)
*   [iOS Trackers](http://www.raksdtd.com/ios-sdk/)

See the [SDK Tracking Specification for RAT](https://confluence.rakuten-it.com/confluence/display/SSEDPT/SDK+Tracking+Specification+for+RAT) page for more information about tracked data. Deploy your app and enable sending after implementing trackers.

#### Step 4: Collect and visualize the tracked data

There are three methods to collect and visualize data. See the [RAT Analytics Tool](https://confluence.rakuten-it.com/confluence/display/RAT/03.RAT+Analytics+Tool) page for more information. If you have access to the Rakuten DU DOMO, you can check out your statistics under [ORCA > Mobile](https://rakuten-du.domo.com/page/707385546). You can request for access [here](https://confluence.rakuten-it.com/confluence/pages/viewpage.action?pageId=551980173).

[![analytics2](../images/img_analytics_2.png)]

## What is being tracked with Analytics?

Some events and parameters in your app are automatically tracked without having to write additional code. The following are examples of automatically tracked events:

*   first launch
*   launch
*   update
*   install
*   open push notification

See the [SDK Tracking Specification for RAT](https://confluence.rakuten-it.com/confluence/display/ESD/SDK+Tracking+Specification+for+RAT) for more information about tracked data.

## How do I report issues with Analytics?

You can report SDK issues through ourÂ [inquiry form](https://rakuten-esd.zendesk.com/hc/en-us/requests/new?ticket_form_id=399907)


### AdditionalÂ Resources

[Android SDK Reference Documentation](http://www.raksdtd.com/android-sdk/)

[iOS SDK Reference Documentation](http://www.raksdtd.com/ios-sdk/)