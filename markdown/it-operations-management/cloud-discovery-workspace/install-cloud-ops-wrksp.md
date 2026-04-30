---
title: Install Cloud Discovery Workspace
description: You can install the Cloud Discovery Workspace application \(com.cloud\_operations\_workspace\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: xanadu
product: Cloud Discovery Workspace
classification: cloud-discovery-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Cloud Discovery Workspace, ITOM Visibility, IT Operations Management]
---

# Install Cloud Discovery Workspace

You can install the Cloud Discovery Workspace application \(com.cloud\_operations\_workspace\) if you have the admin role.

## Before you begin

**Note:** When Cloud Discovery Workspace is installed, several plugins and applications are also installed. For more information, see [Plugins or applications installed with ITOM Visibility](../../it-operations-management/reference/plugin-app-itom-visibility.md).

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Cloud Discovery Workspace requires the following plugin. Ensure that the following plugin is activated before you install Cloud Discovery Workspace.
    -   **Required ServiceNow plugins**
        -   **Discovery \(com.snc.discovery\)**

            ServiceNow Cloud Discovery finds applications and devices on your network, and then updates the CMDB 360 with the information it finds. For more information on activating Discovery, see [Request Discovery](../../discovery/task/t_ActivateTheDiscoveryPlugin.md).


Role required: admin

## About this task

When you install the Cloud Discovery Workspace application, it automatically installs the following role:

<table id="table_ss2_33v_fsb"><thead><tr><th>

Role name

</th><th>

Description and tasks

</th><th>

Nested roles

</th></tr></thead><tbody><tr><td>

sn\_cloud\_ops\_ws.cloud\_ops\_admin

</td><td>

The Cloud Discovery Workspace admin can perform the following actions:-   View the Cloud Discovery Workspace dashboard
-   Create Cloud Discovery schedules
-   Monitor Cloud Discovery operations
-   View Cloud Discovery reports

</td><td>

-   sn\_itom\_ui\_comp.itom\_component\_user
-   discovery\_admin
-   cloud\_admin

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Cloud Discovery Workspace application \(com.cloud\_operations\_workspace\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Cloud Discovery Workspace.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


