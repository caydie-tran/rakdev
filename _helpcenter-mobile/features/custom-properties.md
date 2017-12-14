---
title: Custom Properties
layout: page
parent: _helpcenter-mobile/features.md
categories: [Ecosystem, Analytics, Mobile, Android, iOS, configuration, scrm]
---

## What is the Custom Properties feature?

The **Custom Properties** tool enables you to store and access application configurations. Through Custom Properties, your application can retrieve data directly from the **Rakuten Ecosystem Mobile** servers, and configuration changes are configuration changes are immediately reflected in the current version of your application. **Custom Properties** does not require re-releasing your application for every configuration, and does not require App Store approval.

Here's how it works:

1.  Application configuration data is stored on **Rakuten Ecosystem** servers
2.  Your application retrieves data securely through an SSL
3.  Configuration changes take effect immediately

For example, **Point Partner** -- an **Rakuten Ecosystem Mobile** application -- stores configurations for different endpoints and API URLs using the **Custom Properties** tool. When API URLs or endpoints change, configurations are changed using the Custom Properties tool and are immediately reflected in the **Point Partner** application.

## Why Should I Use Custom Properties?

### **Centralized Settings**

**Custom Properties** centralizes configuration scripts, initialization data, and any other data that has the potential to change during the life span of your app.

### **Immediate implementation**

Changes you make in the **Custom Properties** tool take immediate effect, so there is no need to develop and release a new version of your application. More importantly, there is no need to wait for App Store approval or when the user updates the application.

## How Do I Set Up Custom Properties For My App?

### Step 1: Set up your Rakuten Ecosystem Mobile Services account

To set up your account, please submit query through 
[Inquiry Form](https://developers.rakuten.com/hc/en-us/requests/new?ticket_form_id=399907) with the name of your product or service, the **Business User** contact information, and the **Developer** contact information. You will receive your login credentials for both **Business Users** and **Developers**, and further instructions on setting up and enabling features.

### Step 2: Set up your Custom Properties

1.  Login to the **Rakuten Ecosystem Mobile Services** portal and choose your application from the dropdown menu. Click **Custom Properties**.
2.  Add your JSON or XML configurations by typing directly into the JSON Editor, or by uploading a valid JSON or XML file.
3.  You can store different sets of configurations for different platforms. The **Custom Properties** tool supports iPhone, iPad and Android.

![custom_1](../images/img_custom_properties_1.png)

### Step 3: Fallback and Caching

You can provide a **Fallback URL** as a safety precaution. This URL will be used if the **Custom Properties** settings stored on **Rakuten Ecosystem Mobile Services** are not available. How to Enable **Fallback**:

1.  1.  Select **Use Fallback**
    2.  Enter a valid **Fallback URL** that provides JSON or XML
    3.  Click **Save**

![custom_2](../images/img_custom_properties_fallback.png)

### Step 4: View your**History**

The **History** section provides a read-only view of changes made using the **Dynamic Confgurations** tool. Changes are stored here every time you click **Save**. You can restore previous configurations of your application in this section. ![custom properties history](../images/img_custom_properties_history.png)

### Step 5: Send configurations to your application

Once your application is added to the **Custom Properties** service, you will receive JSON code that can be inserted anywhere in your application.

### Step 6: Create and test various configurations

Use the platform tabs for iPhone, iPad and Android, and the Staging and Production tabs to create and test different configurations. You can use these tabs to see which configuration is best for your application.

# Testing Dynamic Configurations

After your configuration has been set up, ask your engineering team to verify that your application is receiving the JSON or XML code. You can test **Custom Properties** by making changes on the **Rakuten Ecosystem Mobile Services** website and seeing if they are reflected in your mobile application.

## Staging vs Production Testing

**Custom Properties** allows you to have two sets of properties: **Staging** and **Production**. You can use the **Staging** tab to test and experiment with different configurations during development. Once your app is in production, you can then shift your production configurations to the **Production** tab.

## Simulator Application Testing

You can use any mobile application simulator to view and verify configurations on your mobile application.