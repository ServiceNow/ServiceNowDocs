---
title: Install Workplace Reservations for Microsoft Outlook Add-in
description: Install the Workplace Reservations for Microsoft Outlook Add-in application from ServiceNow Store applications. Visit the ServiceNow Store to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.
locale: en-US
release: australia
product: Workplace Service Delivery
classification: workplace-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Workplace Reservations for Microsoft Outlook Add-in, Workplace Reservations for Microsoft Outlook Add-in, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Reservations for Microsoft Outlook Add-in

Install the Workplace Reservations for Microsoft Outlook Add-in application from ServiceNow Store applications. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Before you begin

Also install the Workplace Service Delivery Components application from the store as the Workplace Reservations for Microsoft Outlook Add-in application is built on the Seismic workspace. The Workplace Service Delivery Components store the components built on Seismic to enhance the experience brought to employees while using the Workplace Reservations for Microsoft Outlook Add-in application.

Complete the following setup instructions:

1.  Navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.
2.  Verify that the following plugins are activated:
    -   Workplace Core \(sn\_wsd\_core\) minimum version 2.6.
    -   Latest version of Workplace Reservation Management \(sn\_wsd\_rsv\).
    -   Latest version of Workplace Calendar Synchronization \( sn\_wsd\_rsvsync\).

Use the following details when required:

-   Name of the application: Workplace Reservations for Microsoft Outlook Add-in
-   ID of the application: sn\_wsd\_msaddin

**Important:** The Workplace Reservations for Microsoft Outlook Add-in application uses the credentials used for Microsoft Exchange Online Synchronization.

Role required: admin

**Warning:** If you are installing the Workplace Reservations for Microsoft Outlook Add-in application in a Windows system, it is required to have the “WebView2 runtime” installed on the client devices. You can download it here: [https://developer.microsoft.com/en-us/microsoft-edge/webview2/](https://developer.microsoft.com/en-us/microsoft-edge/webview2/).

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application by using the filter criteria and search bar.

    Search for the application by its name \(Workplace Reservations for Microsoft Outlook Add-in\) or ID \(sn\_wsd\_msaddin\). If you cannot find the application, you may have to request it from the ServiceNow Store.

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    A list of dependent plugins and applications are displayed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Workplace Reservations for Microsoft Outlook Add-in.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Click **Install**.


**Parent Topic:**[Configure Workplace Reservations for Microsoft Outlook Add-in](../concept/configure-workplace-rsv-for-outlook-addin.md)

**Related topics**  


[Create a manifest file for Microsoft Outlook Add-in](add-manifest-file-for-outlook-addin.md)

[Upload the manifest file for a single user](upload-manifest-for-single-user.md)

[Upload the manifest file in Microsoft Office 365](upload-the-manifest-file-office365.md)

