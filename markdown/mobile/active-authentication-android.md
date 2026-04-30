---
title: Keep native apps active during authentication on Android devices
description: Use the preventAppKillOnAuth property on your ServiceNow instance to help prevent Android devices from killing the mobile app when put to background during login. Use this configuration to allow for a smoother authentication experience by keeping the app active until users complete or cancel the login process.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 2
breadcrumb: [Mobile properties, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Keep native apps active during authentication on Android devices

Use the **preventAppKillOnAuth** property on your ServiceNow instance to help prevent Android devices from killing the mobile app when put to background during login. Use this configuration to allow for a smoother authentication experience by keeping the app active until users complete or cancel the login process.

## Before you begin

Role required: admin

## About this task

**Note:** The **preventAppKillOnAuth** may need to be set only if you're experiencing login issues, where the app restarts after being put in the background and then is resumed. After such restarts, the app can fail to redirect to the native mobile interface after login. This issue was found to occur on OEM devices like Redmi, POCO, and Oppo.

The **preventAppKillOnAuth** property is a pre-authenticated mobile setting that when set to true signals to the system that an important task is in progress. This setting maintains that the mobile app remains alive during the authentication process even when moved to the background.

Mobile properties are configured as records in the sys\_sg\_properties table on the  ServiceNow Mobile Platform server.

**Note:**  The **preventAppKillOnAuth** property is supported from the 20.6.0 mobile client release.

-   **Example**

    When you open an authenticator app to retrieve code or approve a login request, the ServiceNow mobile app moves to the background. In such a situation the Android OS may terminate the app in the following circumstances:

    -   If the device is running low on memory.
    -   If the battery saver mode enabled.
    -   If the system settings has a limit to the number of background apps enabled to run simultaneously.

## Procedure

1.  Navigate to **All** &gt; **sys\_extension\_point.list**.

    The Extension Points Mobile table displays.

2.  Find the  **global.CustomPreAuthProperties ** entry in the **API Name** column, and select it.

3.  Search for the **Extension Point CustomPreAuthProperties** record, under Related Links, and select ** Create implementation**.

4.  Select **True/False** in the **Type** field.

5.  In the **Script Include CustomPreAuthProperties** record, add the **preventAppKillOnAuth** property to the  script.

    -   **Example**

        The proceeding code is an example configuration that specifies that Android devices keep the ServiceNow mobile app active until users complete or cancel the login process.

        ```
        var CustomPreAuthProperties = Class.create(); 
        
        CustomPreAuthProperties.prototype = { 
        
            initialize: function() {}, 
        
            /** 
        
             * Returns a JSON object keyed by the custom property names. 
        
             */ 
        
            getProperties: function(input) { 
        
                return { "preventAppKillOnAuth": true }; 
        
            }, 
        
            type: 'CustomPreAuthProperties' 
        
        }; 
        ```

6.  Select  **Active**  to activate the script include.

7.  Select  **Update**  to save your changes.


**Parent Topic:**[Mobile properties](../concept/mobile-properties.md)

