---
title: Feedback
layout: helpcenter-mobile
parent: _helpcenter-mobile/features.md
categories: [Ecosystem Analytics Mobile Android iOS feedback in-app sdk]
permalink: /helpcenter-mobile/features/feedback/
weight: 8
---

## What is Feedback?

**Feedback** is a service provided by the **Rakuten Ecosystem Mobile** that enables developers to get direct input from users on the usability and functionality of their mobile applications. Here's how it works:

1.  Users send application feedback, including bug reports, feature requests, and general comments.
2.  Feedback data is stored by Rakuten Ecosystem Mobile Services (REMS).
3.  Developers view and process data on the Rakuten Ecosystem Mobile Services dashboard.

![feedback_1](../images/img_feedback_header.png)
## Why Should I Use Feedback?

### **Connect with users**

**Feedback** opens a line of direct communication between users and developers. Users can go straight to you with suggestions or requests, cutting out the middleman of application store reviews. You can also encourage users that give positive feedback to rate the application in app stores.

### **Improve user experiences**

**Feedback** enables you to better understand areas in need of improvement in your applications. When you fix an issue or add a feature based on user feedback, you are tailoring your application to better suit your users' needs.

## Features

### **Receive Feedback**

**The Rakuten Ecosystem Mobile SDK** gives you the user interfaces and libraries necessary to receive data from **users****.** **Users** are enabled to provide the following types of feedback:

*   Star ratings
*   Feedback on functionality and usability
*   Feature requests
*   Bug reports

Pending user consent, **Devices** can send:

*   Crash logs
*   Device information
*   Operating System information
*   Region settings
*   Custom app data

**Feedback** provides four pages for developer use. You can also develop and use your own interfaces.


### 1. **Feedback Selection Screen**: 
Users can choose to **Send Feedback**, **Request a Feature**, or **Report a Bug**. 
![feedback_2](../images/img_feedback_selection.jpg)

### 2. **Feedback Screen**: 
Users can rate their experience on a five-star scale and provide written feedback on functionality and usability. Users can tap **Preview** to verify their feedback before sending it in. 
![feedback_3](../images/img_feedback_screen.jpg)


### 3. **Bug Report Screen** 
Users can send written descriptions of bugs encountered during their experience. 
![feedback_4](../images/img_feedback_bug_report.jpg)

### 4. **Feature Request Screen** 
Users can provide a **Feature Title** to summarize the feature and the **Description** space to describe it in detail. 
![feedback_5](../images/img_feedback_feature_request.jpg)



### **Process Feedback Data**

**Rakuten Ecosystem Mobile Services** provides you with a dashboard to view feedback collected from users. It also gives you the flexibility enable or disable the feature remotely. The dashboard summarizes your feedback statistically and graphically, and enables you to view individual pieces of feedback through using a filter. 

![feedback_6](../images/img_feedback_rems.png)

The **Graph** displays the volume of feedback received in the last day, week, month, and all time.

![feedback_7](../images/img_feedback_rems_graph.png)   

The **Statistics** section of the dashboard totals user star ratings and feedback types. 

![feedback_8](../images/img_feedback_rems_stats.png)

The **Filter** enables you to sort user feedback by **Resolution Status**, **Feedback Type**, and **Application.** The **Search** function enables you to sort the list by keyword. When you enter a search term, the list is automatically updated.

![feedback_9](../images/img_feedback_rems_filters.png)


## How Do I Get Feedback For My Apps?

**Step 1: Download the Rakuten Mobile SDK** Install the Rakuten Mobile SDK on your applicable platform:

*   [Android](http://www.raksdtd.com/android-sdk/)
*   [iOS](http://www.raksdtd.com/ios-sdk/)

**Step 2: Register your app with Mobile Ecosystem Services** 
Submit a request to our help center with the following information:

*   Application package name (Android) and bundle id (iOS).
*   The Rakuten Intra accounts of users that need to have access to the service. 

Users will be informed once the service is configured on production and staging environment. 

**Step 3: Build Feedback Into Your App**

*   The Rakuten Mobile SDK includes ready-to-use material and user interfaces.

**Step 4: Test your new Feedback feature** 

The **Rakuten Ecosystem Mobile SDK** team provides you with two methods of testing your new feature: a **Test Automation file** and a **QA application**.

The **Test Automation File** includes behavior driven development (BDD) scenarios, which are applicable to the SDK provided default UI and can be used with automation testing tools. 
Download the file here: [BDD Scenarios for feedback.txt](../16_feedback_bdd_scenario) 

The **QA Application** provided as part of the source code repository, is a sample app that implements an end-to-end Feedback module. If you need access to the QA app on your personal phone, query via
[Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) for a Hockey app invite. 

Within the **QA Application**, you can access a staging environment. Any feedback sent from the staging environment will be sent to the **Rakuten Ecosystem Mobile Services** dashboard. You can reference the **QA Application** code to set up your own staging environment.

## Rakuten Ecosystem Mobile Services API

The **Rakuten Ecosystem Mobile** team provides an API that sends data to the ** Rakuten Ecosystem ****Mobile Services **dashboard.

### API Features

*   REST API
*   No end-user login required
*   Permanent token client SDK authorization
*   SSL encryption
*   JSON data exchange
*   HTTP custom responses

### API Fields and Descriptions

The **Rakuten Ecosystem Mobile Services** API sends the information in the table below.

| Field | Description | Required | Data Type | Validation (Business Rules)|
| --- | --- | --- | --- | --- |
| Demographics | Member information including age, gender, location | No | Key Value Pair (Map/Hash) |
| Custom App Data | Custom JSON code from client apps | No | text / JSON |
| App ID | Client app ID | Yes | numeric | App ID format |
| Device ID | Client device ID | Yes | alphanumeric | Device ID format |
| Login Status | Whether or not the user is logged in to an account associated with the application | Yes | boolean |
| Star Rating (UI) | User ratings on a scale of zero to five | Yes | numeric | between 0 and 5 only |
| Free Text (UI) | User input including bug reports, feedback, or feature requests | Yes | text | unlimited length |
| Title (UI) | User title for bug reports, feedback, or feature requests | Yes | text | 255 characters |
| Classification (UI) | Bug Report, Feedback, or Feature Request | Yes | numeric | limited to three types 1.  Feedback 2.  Bug report 3.  Feature request|
| Crash Logs | User can attach relevant logs to a bug report | Yes | file / blob |
| Device Model | Report the make and model of the client device | Yes | alphanumeric |
| OS Version | Report the operating system versionÂ of the client device | Yes | alphanumeric |
| Region Setting | Report the Region Setting of the client device at the time Feedback was sent. | Yes | alphanumeric |
| SDK Library Ver. | Report the installed versions of any SDK libraries | Â Yes | alphanumeric |