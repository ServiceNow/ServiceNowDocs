---
title: Install an application or plugin
description: Install an application or plugin to make its features available on your instance.
locale: en-US
release: zurich
product: Application Manager
classification: application-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Installing apps, plugins, and products, Application Manager, Administering applications, Get started, Administer]
---

# Install an application or plugin

Install an application or plugin to make its features available on your instance.

## Before you begin

For domain-separated instances:

-   applications must be installed and updated from the global domain.
-   The `sys_user` table record for the user who completes the task must also be in the global domain.

Role required: admin, sn\_appclient.app\_client\_user, or sn\_appclient.app\_client\_company\_installer

**Note:** Some applications and plugins can't be uninstalled after they've been installed.

## About this task

This topic describes how to install an application or plugin. For information about updating applications or plugins, see [Update an application or plugin](../../../administer/application-manager/task/update-application-app-mgr.md).

## Procedure

1.  Navigate to the **Available for you** tab of the Application Manager in one of the following ways.

    -   Navigate to **Admin** &gt; **Application Manager** &gt; **Available for you**
    -   Navigate to **All** &gt; **Admin Center** &gt; **Application Manager** &gt; **Available for you**.
2.  Find and select the application or plugin you want to install.

    You can search for an application or plugin by name, or use the sort and filter options available in the Application Manager.

3.  Select **Install**.

4.  Select the application version that you want to install from the **Version** drop-down menu.

5.  If the application or plugin has dependencies, verify that all necessary dependencies can be updated or installed.

    If any dependencies are categorized as **Needs to be procured from store**, procure the necessary dependencies and sync the Application Manager with the ServiceNow Store before continuing. For more information about unavailable dependencies that block installation, see [Evaluating version requirements and dependencies](../../../administer/servicenow-store/concept/versions-dependencies.md).

6.  Install the application now or schedule installation for a later time.

<table id="choicetable_kkl_v3m_yfc"><thead><tr><th align="left" id="d214379e205">

Installation option

</th><th align="left" id="d214379e208">

Procedure

</th></tr></thead><tbody><tr><td id="d214379e214">

**Install now**

</td><td>

1.  Leave the default option to **Install now** selected.
2.  Select **Install**.


</td></tr><tr><td id="d214379e238">

**Install later**

</td><td>

1.  Select the option to **Install later**.
2.  Enter a start date and start time.
3.  Select **Schedule**.


</td></tr></tbody>
</table>
## Result

If you choose to install the application or plugin now, it and its dependencies begin to install immediately. Scheduled installations begin at the chosen date and time.

**Parent Topic:**[Installing applications, plugins, and products](../../../administer/application-manager/concept/installing-apps-app-manager.md)

