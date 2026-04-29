---
title: Configure an external authentication browser for ServiceNow mobile apps
description: Admins can configure an external browser for mobile apps. This external browser is used during authentication so external URLs that are opened by the same browser can maintain sessions and cookies.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Configure an external authentication browser for ServiceNow mobile apps

Admins can configure an external browser for mobile apps. This external browser is used during authentication so external URLs that are opened by the same browser can maintain sessions and cookies.

## Before you begin

Role required: admin

## About this task

Cookies aren't shared between ServiceNow® mobile app browsers and external browsers that load external sites. ServiceNow mobile apps enable end users to log in with an SSO \(single sign-on\) service such as Okta or Microsoft Entra ID. These SSO services provide a seamless and secure authentication experience for end users. However, sometimes end users might want to open authenticated third-party links that use the same SSO service within the app but not be required to log in again. For example, an end user might want to open a link to a report that is hosted on a different platform that uses the same SSO service as the ServiceNow mobile app.

To enable end users to access links on different platforms that use the same SSO service as the ServiceNow mobile app, admins can configure an external browser for login to the ServiceNow mobile app, so cookies are shared between login and the external site. This means that the SSO session persists after the end user logs in and then automatically logs the end user into external sites if those sites use the same SSO provider as the ServiceNow mobile app.

-   **Web browser properties**

    Use the following properties to specify the external browser and the authentication browser in the `CustomPreAuthProperties` script include.

    |Mobile app operating system|Property|Description|
    |---------------------------|--------|-----------|
    |iOS|**SNExternalBrowseriOS**|Configures the browser type to use for opening external links on iOS apps.|
    |iOS|**SNAuthenticationBrowseriOS**|Configures the browser type to use for authenticating users on iOS apps.|
    |Android|**SNExternalBrowserAndroid**|Configures the browser type to use for opening external links on Android apps.|
    |Android|**SNAuthenticationBrowserAndroid**|Configures the browser type to use for authenticating users on Android apps.|

-   **Property values**

    The following browser types can be specified for the web browser properties.

    |Property value|Description|
    |--------------|-----------|
    |**safari**|Apple Safari|
    |**chrome**|Google Chrome|
    |**firefox**|Mozilla Firefox|
    |**edge**|Microsoft Edge|
    |**workspaceone**|AirWatch VMware Workspace ONE|
    |**webatwork**|MobileIron Web@Work|
    |**blackberryaccess**|BlackBerry Access|
    |**maas360**|IBM MaaS360|
    |**citrix**|Citrix Secure|

-   **Example**

    ```
    {"SNExternalBrowseriOS": "safari", "SNAuthenticationBrowseriOS": "safari"}
    ```

    **Important:** The values for both properties must match for SSO sessions to persist between login and other browsing.


## Procedure

1.  Navigate to **All** &gt; **sys\_extension\_point.list**.

    The Extension Points table displays.

2.  In the API Name column, find the **global.CustomPreAuthProperties** entry and select it.

3.  In the Extension Point CustomPreAuthProperties record, under **Related Links**, select **Create implementation**.

4.  In the Script Include CustomPreAuthProperties record, add the external browser and the authentication browser properties to the **Script**.

    For example, here's a configuration that specifies the Apple Safari browser for the external and the authentication browsers:

    ```
    var CustomPreAuthProperties = Class.create();
    CustomPreAuthProperties.prototype = {
         initialize: function() {
         },
    
         /**
          * Returns a JSON object keyed by the custom property names.
          */
         getProperties: function(input) {
              return {"SNExternalBrowseriOS": "safari", "SNAuthenticationBrowseriOS": "safari"};
         },
    
         type: 'CustomPreAuthProperties'
    };
    ```

5.  Select **Active** to activate the script include.

6.  Select **Update** to save your changes.


**Parent Topic:**[Mobile authentication](../concept/mobile-authentication.md)

