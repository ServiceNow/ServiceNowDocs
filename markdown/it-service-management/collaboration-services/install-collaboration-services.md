---
title: Install Collaboration services
description: You can install the Collaboration services application \(sn\_tcm\_collab\_hook\) if you have the admin role.
locale: en-US
release: xanadu
product: Collaboration Services
classification: collaboration-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Collaboration services, IT Service Management]
---

# Install Collaboration services

You can install the Collaboration services application \(sn\_tcm\_collab\_hook\) if you have the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Collaboration services requires the following ServiceNow Store applications. Ensure that these applications are installed before you install Collaboration services.
    -   **Required ServiceNow Store applications**
        -   **Slack Spoke for ServiceNow IntegrationHub \[com.sn.slack.ahv2\]**

            If you want Slack integration for tasks or task communication management, install the Slack Spoke for ServiceNow IntegrationHub application. The application provides actions that you can use when designing flows. These actions allow you to communicate with Slack APIs.

        -   **ServiceNow for Microsoft Teams**

            If you want to integrate ServiceNow for Microsoft Teams, install the IT Service Management integration with Microsoft Teams or HR Service Delivery integration with Microsoft Teams applications as required. For more information on the integration, see [ServiceNow for Microsoft Teams](https://www.servicenow.com/docs/access?context=c_ServiceNowForMSTeams&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

        -   **ServiceNow for Zoom**

            If you want to integrate ServiceNow instance with Zoom, for complete information, see [ServiceNow for Zoom](https://www.servicenow.com/docs/access?context=sn_zoomIntegration&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).


Role required: admin

## About this task

For the tables that are installed with Collaboration services, refer [Components installed with Collaboration services](../reference/installed-with-collaboration-services.md)

.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the  application \(\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install .

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


