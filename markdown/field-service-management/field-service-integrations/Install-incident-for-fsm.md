---
title: Install Incident Management for Field Service
description: You can install the Incident Management for Field Service application \(sn\_fsm\_inc\_mng\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Field Service Integrations
classification: field-service-integrations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration with Incident Management, Integrating Field Service Management with other applications, Configure, Field Service Management]
---

# Install Incident Management for Field Service

You can install the Incident Management for Field Service application \(sn\_fsm\_inc\_mng\) if you have the admin role.The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Incident Management for Field Service requires the following plugins. Ensure that these plugins are activated before you install Incident Management for Field Service.
    -   **Required ServiceNow plugins**
        -   **CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\)**

            Enable your agents so they can engage with customers, answer questions, create cases, and resolve issues. For more information, see [Set up CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-config-workspace-set-up&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Incident Management for Field Service application \(sn\_fsm\_inc\_mng\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install .

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Integration with Incident Management](../concept/incident-for-fsm.md)

