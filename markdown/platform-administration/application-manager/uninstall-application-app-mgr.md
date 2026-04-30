---
title: Uninstall an application
description: Uninstall an unused application to remove unnecessary or conflicting scripts, background jobs, and roles from your instance.
locale: en-US
release: yokohama
product: Application Manager
classification: application-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Uninstalling apps, Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Uninstall an application

Uninstall an unused application to remove unnecessary or conflicting scripts, background jobs, and roles from your instance.

## Before you begin

Role required: admin, sn\_appclient.app\_client\_user, or sn\_appclient.app\_client\_company\_installer

## About this task

**Note:** Some applications and plugins can't be uninstalled after they've been installed.

## Procedure

1.  Navigate to the **Installed** tab of Application Manager in one of the following ways.

    -   Navigate to **Admin** &gt; **Application Manager** &gt; **Installed**.
    -   Navigate to **All** &gt; **Admin Center** &gt; **Application Manager** &gt; **Installed**.
2.  Find and select the application or plugin you want to uninstall.

    You can search for an application or plugin by name, or use the sort and filter options available in the Application Manager.

3.  From the Quick Actions section of the details page, select **Uninstall**.

4.  If you want to delete fields and metadata associated with the application from your instance, clear the check box labeled **Retain fields and data**.

    If the application can't be uninstalled, clearing the **Retain fields and data** check box might resolve the issue.

5.  Select **OK**.


**Parent Topic:**[Uninstalling applications](../concept/uninstalling-apps-app-manager.md)

