---
title: Mobile system property configurations
description: Several system properties are available for you to further configure the mobile app. For example, use system properties to require a PIN, hide the image on the app homepage, configure the blur in background option, or disable sharing attachments from the mobile app.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/additional-mobile-configuration.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile system property configurations

Several system properties are available for you to further configure the mobile app. For example, use system properties to require a PIN, hide the image on the app homepage, configure the blur in background option, or disable sharing attachments from the mobile app.

-   **[Require an app PIN for the mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/require-app-pin.md)**  
Require users to enter a PIN when the application has been inactive for five minutes. To require the mobile user to set and enter a local application PIN, add the system property **glide.sg.require\_mobile\_application\_pin**.
-   **[Configure mobile re-authentication system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-reautentication-concept.md)**  
Set mobile re-authentication system properties so users must re-authenticate their login credentials when performing specific actions.
-   **[Configure the blur app option to improve security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/t_BlurApp.md)**  
As a security feature, administrators can configure the mobile app to blur or appear blackened, depending on the operating system, when not in focus on a mobile device. When you double-click the home button on your mobile device to close apps or navigate back to where you left off, the ServiceNow app appears blurred or blackened.
-   **[Configure the status for rooted and jailbroken devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/configure-rooted-jailbroken-devices.md)**  
Define whether jailbroken \(iOS\) and rooted \(Android\) devices are permitted on your mobile device. The default value is set to `false` to increase security and to minimize possible disruption to your system.
-   **[Configure the mobile app to clear the copy/paste clipboard and block ability to share content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/configure-copy-paste.md)**  
To have the mobile app clear the pasteboard when the app enters the background, as well as block the ability to share content, add the system property **glide.sg.clear\_pasteboard\_when\_backgrounded**.
-   **[Configure the maximum number of records returned for data items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/configure-data-item-row-count.md)**  
To set the maximum number of rows retrieved for the table defined in the data item, add the system property **glide.sg.data\_item.row\_count**.
-   **[Configure pagination size for search lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/configure-pagination-size.md)**  
To configure the amount of search list results that load to the screen as the user scrolls down, add the system property **glide.sg.choice\_list.window\_size**.
-   **[Configure the maximum number of records returned for list UI parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/configure-max-ui-param.md)**  
To configure the maximum number of records returned for a list of parameters, add the system property **glide.sg.list.max\_items\_number**.
-   **[Configure a placeholder image for missing images in mobile apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/set-default-missing-image.md)**  
You can specify an image on your instance as a placeholder for missing images. This image appears in your mobile apps when a record has an image field with an empty value, such as a user avatar or catalog item. You can select a different image to use for each table on your instance.
-   **[Configure which external apps are available for deep linking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-allow-deeplink.md)**  
Administrators can define which external apps can be used in deep links with the **glide.sg.allowed\_external\_deeplinks** property.
-   **[Block users from downloading or sharing attachments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/block-users-download-shar-attach.md)**  
Set the **glide.sg.block\_mobile\_attachments\_sharing** system property to `true` to hide the sharing button in the mobile app native viewer.
-   **[Configure group ACL for aggregation requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/config-grp-acl-4-aggreg-req.md)**  
Use the **glide.sg.group\_acl.enabled** system property to control the validation of access control lists \(ACL\) during aggregation requests that are related to displaying results from data items that use grouping.
-   **[Control whether users can view attachments in external applications on Android devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/vu-attach-extapp-android.md)**  
Set the **glide.sg.block\_mobile\_attachments\_external\_viewing** system property to true to prevent Android users from opening attachments in third-party applications.

**Parent Topic:**[Considerations before implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/imp-considerations.md)

