---
title: Roll back an application
description: As an administrator, you can roll back the last installation of a selected application. When you roll back an application, you remove all code, table, and file updates from the initial installation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Rolling back and removing applications, Installation considerations, Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Roll back an application

As an administrator, you can roll back the last installation of a selected application. When you roll back an application, you remove all code, table, and file updates from the initial installation.

## Before you begin

-   Publish one or more applications to the application repository.
-   The selected application must have been installed in the application repository or the application store. See [Install a ServiceNow Store application](t_InstallApplications.md).

Role required: admin

## About this task

You can roll back the last installation or upgrade of all applications that are installed from the application store or repository. Rolling back an installation enables you to make needed changes to artifacts associated with an application before you publish and install it again.

**Note:** This rollback does not affect the global application record. To remove the global application record, you must instead perform an uninstall of the application. See [Uninstall an application](t_UninstallApplications.md).

## Procedure

1.  Log in to the instance in which you want to roll back the installed application.

2.  Navigate to **System Applications** &gt; **My Company Applications**.

3.  Click the name or icon of the application that you want to roll back.

4.  In the custom application record, click the **Rollback** related link.


**Parent Topic:**[Rolling back and removing applications](../concept/c_RemovingApplications.md)

**Related topics**  


[Uninstall an application](t_UninstallApplications.md)

