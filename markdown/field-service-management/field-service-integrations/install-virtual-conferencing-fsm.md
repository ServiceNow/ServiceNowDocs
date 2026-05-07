---
title: Install Field Service Management Virtual Conferencing Integration
description: You can install the Field Service Management Virtual Conferencing Integration application \(com.snc.fsm\_vci\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Field Service Integrations
classification: field-service-integrations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration with Virtual Conferencing, Integrating Field Service Management with other applications, Configure, Field Service Management]
---

# Install Field Service Management Virtual Conferencing Integration

You can install the Field Service Management Virtual Conferencing Integration application \(com.snc.fsm\_vci\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Field Service Management Virtual Conferencing Integration requires the following plugins. Ensure that these plugins are activated before you install Field Service Management Virtual Conferencing Integration.
    -   **Required ServiceNow plugins**
        -   **Notify \(com.snc.notify\)**

            Provides support for SMS and voice channels on the platform. For more information about activating Notify, see [Activate Notify](https://www.servicenow.com/docs/access?context=t_ActivateNotify&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

-   Field Service Virtual Conferencing Integration requires the following ServiceNow Store applications. Ensure that these applications are installed before you install Field Service Management Virtual Conferencing Integration.
    -   **Required ServiceNow Store applications to integrate Zoom**
        -   **Zoom Spoke**

            Integrate the Zoom account of your company with your ServiceNow instance. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=installing-applications-in-application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

        -   **Notify Zoom Connector**

            Associates the Notify communication channel with Zoom meetings. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=installing-applications-in-application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

    -   **Required ServiceNow Store applications to integrate Microsoft Teams**
        -   **Notify Connector for Microsoft Teams**

            Manage and initiate a Microsoft Teams meeting directly from a task. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=installing-applications-in-application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

        -   **Microsoft Teams Communication Spoke**

            Manage groups calls and meetings in Microsoft Communications account from your ServiceNow instance. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=installing-applications-in-application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Field Service Management Virtual Conferencing Integration application \(com.snc.fsm\_vci\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Field Service Management Virtual Conferencing Integration.

4.  Select **Install**.


**Parent Topic:**[Integration with Virtual Conferencing](../concept/virtual-conference-integration-fsm.md)

