---
title: Install Playbooks for Field Service Management
description: Install the Playbooks for Field Service Management application \(sn\_fsm\_playbook\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Playbooks, Set up work orders and tasks, Configure, Field Service Management]
---

# Install Playbooks for Field Service Management

Install the Playbooks for Field Service Management application \(sn\_fsm\_playbook\) if you have the admin role.

## Before you begin

Role required: admin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Playbooks for Field Service Management requires the following plugins. Ensure that these plugins are activated before you install Playbooks for Field Service Management.
    -   **Required ServiceNow plugins**
        -   **Playbook Experience Core \(com.glide.playbook\_experience.config\)**

            Enables you to customize the default Playbook user experience to create your desired business process workflow.

        -   **Field Service Management**

            Enables you to manage work requests that are performed on location by field service agents.

            For information, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).

        -   **Process Automation Designer Core \(com.glide.pad.core\)**

            Enables you to create a simplified and task-oriented view of your process.

            For more information, see Process Automation Designer platform feature.


## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Playbooks for Field Service Management application \(com.sn\_fsm\_playbook\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Playbooks for Field Service Management.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


