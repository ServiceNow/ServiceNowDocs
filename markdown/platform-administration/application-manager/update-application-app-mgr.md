---
title: Update an application or plugin
description: Update an application or plugin to get the latest features that are compatible with your instance version.
locale: en-US
release: xanadu
product: Application Manager
classification: application-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Updating apps, Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Update an application or plugin

Update an application or plugin to get the latest features that are compatible with your instance version.

## Before you begin

For domain-separated instances:

-   applications must be installed and updated from the global domain.
-   The `sys_user` table record for the admin who completes the task must also be in the global domain.

Role required: admin or sn\_appclient.app\_client\_user

## Procedure

1.  Navigate to the **Updates** tab of Application Manager in one of the following ways.

    -   Navigate to **Admin** &gt; **Application Manager** &gt; **Updates**.
    -   Navigate to **All** &gt; **Admin** &gt; **Application Manager** &gt; **Updates**.
2.  Find and select the application or plugin that you want to update.

    You can search for an application or plugin by name, or use the sort and filter options available in the Application Manager.

3.  From the Summary section of the details page, select **Proceed to update**.

4.  Select a compatible version from the version drop-down menu.

5.  If the application or plugin has dependencies, verify that all necessary dependencies can be updated or installed.

    If any dependencies are categorized as **Needs to be procured from store**, procure the necessary dependencies and sync the Application Manager with the ServiceNow Store before continuing. For more information about unavailable dependencies that block updates, see [Updating applications](../concept/updating-apps-app-manager.md).

6.  Install the update now or schedule installation for a later time.

<table id="choicetable_a33_l3m_yfc"><thead><tr><th align="left" id="d75632e191">

Installation option

</th><th align="left" id="d75632e194">

Procedure

</th></tr></thead><tbody><tr><td id="d75632e200">

**Install now**

</td><td>

1.  Leave the default option to **Install now** selected.
2.  Select **Install**.


</td></tr><tr><td id="d75632e224">

**Install later**

</td><td>

1.  Select the option to **Install later**.
2.  Enter a start date and start time.
3.  Select **Schedule**.


</td></tr></tbody>
</table>
## Result

If you choose to install the update now, the application or plugin and its dependencies begin updating immediately. Scheduled updates begin at the chosen date and time.

