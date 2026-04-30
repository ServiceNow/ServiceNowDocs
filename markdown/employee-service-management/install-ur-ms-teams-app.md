---
title: Install Universal Request integration with Microsoft Teams application
description: Install the Universal Request integration with Microsoft Teams application \(sn\_uni\_req\_msteams\). You can initiate Microsoft Teams conversations within your ServiceNow instance by using this application. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Plan your installation, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Install Universal Request integration with Microsoft Teams application

Install the Universal Request integration with Microsoft Teams application \(sn\_uni\_req\_msteams\). You can initiate Microsoft Teams conversations within your ServiceNow instance by using this application. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Universal Request integration with Microsoft Teams requires the following plugin. Ensure that the plugin is activated before you install Universal Request integration with Microsoft Teams.
    -   **Required ServiceNow plugins**
        -   **Universal Request: Virtual Agent Conversations \(com.snc.universal\_request.va\)**

            The Universal Request Virtual agent conversations plugin is required for the Virtual Agent functionalities to be activated.

-   Universal Request integration with Microsoft Teams requires the following ServiceNow Store application. Ensure that the application is installed before you install Universal Request integration with Microsoft Teams.
    -   **Required ServiceNow Store applications**
        -   **ServiceNow for Microsoft Teams \(sn\_now\_teams\)**

            The ServiceNow for Microsoft Teams store application must be activated for the Universal Request integration with Microsoft Teams application to function.


Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Universal Request integration with Microsoft Teams application \(sn\_uni\_req\_msteams\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Universal Request integration with Microsoft Teams.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


-   **[Approve application restricted caller access privileges](ur-mst-approve-rca.md)**  
Approve restricted caller access \(RCA\) privileges in the target scope so that you can provide scope access privileges. Approving the RCA privileges enables the script includes in Universal Request scope to be accessed from the Universal Request integration with Microsoft Teams scope.

**Parent Topic:**[Plan your installation](../concept/plan-installation-ms-teams.md)

