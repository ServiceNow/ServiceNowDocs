---
title: Create a branded landing page for a single instance
description: Create a branded pre-login landing page with a ServiceNow mobile login button or mobile deep links. These elements redirect users either to a specific area within the ServiceNow mobile app or to the login screen.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-15"
reading_time_minutes: 2
breadcrumb: [Branded landing page for a single instance, Mobile instances, Configuring the Mobile Platform, Mobile Platform]
---

# Create a branded landing page for a single instance

Create a branded pre-login landing page with a ServiceNow mobile login button or mobile deep links. These elements redirect users either to a specific area within the ServiceNow mobile app or to the login screen.

## Before you begin

Role required: admin

## About this task

**Note:** This feature is supported from ServiceNow mobile app version 19.0 and above.

**Note:** For the Xanadu version and earlier, this functionality is supported using the property **sys\_extension\_point** with the API name global.CustomPreAuthProperties. From Yokohama, you can use the **preLoginLandingPage** property and remove the property **sys\_extension\_point** with the API name global.CustomPreAuthProperties from the existing script.

The **sys\_extension\_point** with the API name global.CustomPreAuthProperties still works in the Yokohama version, even if the **preLoginLandingPage** property isn’t defined. However, if both properties are defined, the property **preLoginLandingPage** takes precedence. For information about creating a branded landing page in the Yokohama version and later, refer to this topic in the Yokohama or later documentation version.

## Procedure

1.  Navigate to **All** &gt; **sys\_extension\_point.list**.

2.  Search and select for the property **global.CustomPreAuthProperties** in **API Name** column.

3.  Select the **Create implementation** link, which is found in the **Related Links** section of the **Extension Point** page.

4.  Replace the existing script with the following script in the **Script** field.

    ```
     var CustomPreAuthProperties = Class.create(); 
    CustomPreAuthProperties.prototype = { 
        initialize: function() {}, 
        /**   
       * Returns a JSON object keyed by the custom property names.   
       */ 
        getProperties: function(input) { 
            var customProperties = {}; 
            if (input.clientType == 'agent') { // Applicable only to Agent type  
                customProperties["preLoginLandingPage"] = { 
                    "url": "https://url1.com", 
                    "loginLabelTranslationKey": "sign_in_label_txt" 
                } 
            } else if (input.clientType == 'request') { // Applicable only to Requestor type  
                customProperties["preLoginLandingPage"] = { 
                    "url": "https://url2.com", 
                    "loginLabelTranslationKey": "access_account_label_txt" 
                } 
            } 
            return customProperties; 
        }, 
        type: 'CustomPreAuthProperties' 
    }; 
    ```

5.  Replace the following values in the script:`"https://url1.com"`, `"https://url2.com"`, with a public web page URL or a ServiceNow domain public web page.

6.  Replace the value of **loginLabelTranslationKey** with a button label key from the following table.

    **Note:** The predefined button key is translated according to the users preferred language settings on the app.

    |Predefined button label key|Displayed button label name|
    |---------------------------|---------------------------|
    |`login_label_txt`|Log in|
    |`sign_in_label_txt`|Sign in|
    |`enter_label_txt`|Enter|
    |`access_account_label_txt`|Access account|
    |`continue_label_txt`|Continue|
    |`get_started_label_txt`|Get started|
    |`proceed_label_txt`|Proceed|

7.  Select the **Active** field if you want this mobile property to be active.

8.  Select **Update**.


## What to do next

You may want to change the login page to be compatible with the style of the branded landing page. For more information, see [Publish mobile apps with custom branding](../concept/mobile-publishing.md) and [Next Experience theming for mobile](../concept/explore-ne-theming.md).

For more information on using deep links, see [Navigation links within a branded landing page](../reference/branded-landing-page-links.md) and [Deep linking for mobile](../concept/deep-link-mobile.md).

