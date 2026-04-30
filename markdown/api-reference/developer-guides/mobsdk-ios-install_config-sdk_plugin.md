---
title: Install and configure the Mobile SDK scoped application
description: Before writing any application that leverages the Mobile SDK, you must install and configure the Mobile SDK scoped application.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Get started with Mobile SDK - iOS, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Install and configure the Mobile SDK scoped application

Before writing any application that leverages the Mobile SDK, you must install and configure the Mobile SDK scoped application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the Mobile SDK page on the ServiceNow Store web site.

    For details, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

2.  Select **Request Install** to download the Mobile SDK scoped application onto your ServiceNow instance.

3.  Verify that the Mobile SDK scoped application was properly installed on your ServiceNow instance.

    1.  Open the plugin's form: `System Definition` &gt; `Plugins`.

    2.  In the search field, enter `mobile_sdk`.

        A screen similar to the following should appear:

        ![Verify Mobile SDK plugin](../../image/mobile_sdk-verify_plugin.png)

    3.  Verify that the plugin **Id** is `sn_mobile_sdk` and that the version is the latest.

4.  Open the Mobile SDK Settings \[sn\_mobile\_sdk\] table and create a new application record for the application that will leverage the Mobile SDK.

    ![Mobile SDK Settings form](../../image/mobile_sdk-sn_mobile_sdk-screen.png)

    1.  In the **Name** field, enter the name of your application that will leverage the Mobile SDK.

    2.  In the **Android Application ID** and **Apple Bundle ID** fields, enter the ID of your mobile application.

        For example, if the Mobile SDK was added to your mobile applications, then these IDs would be the IDs of the mobile applications.

    3.  In the **SDK Settings** field, enter JSON configuration properties for all of the feature services that your application will leverage, set to `true`.

        For example:

        ```
        {
            "graphql": {
                "enabled" : true,
                        "allowGuestAccess" : true
            },
            "table": {
                "enabled" : true,
                        "allowGuestAccess" : true
            },
            "api": {
                "enabled" : true,
                        "allowGuestAccess" : true
            },
            "attachment": {
                "enabled" : true,
                        "allowGuestAccess" : true
            },
            "chat": {
                "enabled" : true,
                        "allowGuestAccess" : true
            },
            "web": {
                "enabled" : true,
                        "allowGuestAccess" : true
            },
            "push": {
                "enabled" : true
            }
        }
        ```

        Ensure that the **Advanced** check box is unselected. This allows you to enter JSON in the **SDK Settings** field.

        ![SDK settings](../../image/mobile_sdk-sn_mobile_sdk_settings.png)

        Any applicable configuration added in **SDK Settings** is used in conjunction with the ServiceNow instance configuration.

        For example, if `chat: enabled = true`, your ServiceNow instance must have the Virtual Agent plugin installed to leverage the chat functionality. If the Virtual Agent plugin is installed, but **SDK Settings** contains `chat: enabled = false`, your application is not able to leverage the chat interface.

    4.  Select **Submit** to save your application settings.

5.  Optional. If you want your application to leverage User Experience Analytics, register your application with the User Experience Analytics application.

    1.  Reopen your application's Mobile SDK Settings record.

    2.  In the bottom-left of the screen, select **Register for Analytics**.

        A screen similar to the following appears:

        ![Register analytics](../../image/mobile_sdk-register-analytics.png)

    3.  Select **Update** to save the registration.

6.  Verify your SDK Settings.

    1.  Navigate to the **REST API Explorer**.

    2.  Enter the following in the specified fields:

        -   **Namespace**: `sn_mobile_sdk`
        -   **API Name**: `Mobile SDK`
        -   **API Version**: `latest`
    3.  Select **Get settings for Android App \(GET\)**.

    4.  In the **applicationID** field, enter the Android Application ID that you entered in the associated Mobile SDK Settings record and then select **Send**.

        The response should look similar to the following:

        ![Verigy SDK settings](../../image/mobile_sdk-verify_SDK-Settings.png)

        The JSON **Response Body** should look similar to the following:

        ```
        { 
          "platformVersion": "utah", 
          "enabled": true, 
          "analytics": { 
            "AnalyticsEnabled": true, 
            "AnalyticsEnabledForUnauthenticatedUser": false, 
            "EndpointUrl": "https://my-instance.servicenow.com.com", 
            "InstanceId": "db63a848db9f6091fd3467c8f4879524", 
            "ApiKey": "de742fc9db9f6090e03ad7c8f4961923:af0f36b91bc074109a9054a26032a6bf", 
            "ApiAuth": "11ab4240a6d5459c96d2bfb8e1aa3ddd", 
            "ConsentSettings": null, 
            "AppName": "TestNow App", 
            "AppType": "MobileSDK", 
            "ChannelType": "sdk", 
            "Configuration": {} 
          }, 
          "sdk": { 
            "graphql": { 
              "enabled": true 
            }, 
            "table": { 
              "enabled": true 
            }, 
            "api": { 
              "enabled": true 
            }, 
            "attachment": { 
              "enabled": true 
            }, 
            "chat": { 
              "enabled": true 
            }, 
            "web": { 
              "enabled": true 
            },
            "push": { 
              "enabled": true 
          } 
        } 
        ```


