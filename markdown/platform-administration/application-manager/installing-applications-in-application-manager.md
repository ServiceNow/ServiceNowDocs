---
title: Install an application or plugin
description: Install, update, or schedule multiple application installations to your instance using the Application Manager.
locale: en-US
release: xanadu
product: Application Manager
classification: application-manager
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installing apps, plugins, and products, Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Install an application or plugin

Install, update, or schedule multiple application installations to your instance using the Application Manager.

## Before you begin

For domain-separated instances:

-   applications must be installed and updated from the global domain.
-   The `sys_user` table record for the admin who completes the task must also be in the global domain.

Role required: admin, sn\_appclient.app\_client\_user, or sn\_appclient.app\_client\_company\_installer

**Note:**

Some applications and plugins can't be uninstalled after they've been installed.

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **Application Manager**.

2.  Select an application from the dashboard to install.

3.  Select the **Install** button on the application details page.

4.  Select the **Install** button.

    1.  Select the **Install Later** option and choose a start date and time to schedule your application for installation.

    **Note:** Multiple installations can be scheduled at the same time with the support of queued installation.

5.  To update an application that is installed do the following:

    1.  Select the **Updates** section on the homepage.

    2.  Select an application with an update available.

    3.  On the details page, select **Proceed to update**.

    4.  Select **Install** to update the application.

    5.  To schedule the update for a later time, select **Install later**, choose a date and time for the update, and select **Schedule**.

    6.  To update dependencies if available, select **Update Dependencies**.

    7.  Select the dependency applications and versions to update and select **Proceed**.

    8.  Review the installation details and select **Install**.


