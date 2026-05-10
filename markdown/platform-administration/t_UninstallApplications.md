---
title: Uninstall an application
description: As an administrator, you can uninstall applications that are no longer needed. Typically, you uninstall applications that have been shared with other instances and you want to remove them.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Rolling back and removing applications, Installation considerations, Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Uninstall an application

As an administrator, you can uninstall applications that are no longer needed. Typically, you uninstall applications that have been shared with other instances and you want to remove them.

## Before you begin

**Note:** For global scoped applications, you must first remove the associated files from the application before you delete the application record. These actions help protect the integrity of the instance by preventing the accidental deletion of files in the global scope. See [Legacy - Remove a file from a global application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/delete-files-global-application.md) and [Legacy - Move an application file between global applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/t_MoveAppFilesBetweenGlobalApps.md).

Role required: admin

## About this task

When you uninstall an application, all application files associated with the application are also removed.

## Procedure

1.  Log in to the instance on which you want to uninstall an application.

2.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Click the name or icon of the application that you want to uninstall.

    **Note:** You cannot uninstall applications on the **In Development** tab, but you can delete them. To learn more about what happens when you perform an application deletion, see [Delete an application](t_DeleteAnApplication.md). You also cannot uninstall base system applications.

4.  In the custom application record, click the **Uninstall** related link.

    The following information is displayed in the pop-up window:

    -   List of dependent applications.
    -   List of in-development applications.
    -   Tables and records in the required application.
    -   Option to retain the application tables and data.

        **Note:** If one of the dependent applications is uninstalled after retaining the tables and data, the **Uninstalled applications with retained tables** list is also displayed. In this case, the **Retain tables and data** check box is selected by default and can't be cleared.

        When customers upgrade to this new version of your application, the Deletes in your author\_elective\_update folder will be written as Skips in the Upgrade History entry for this application upgrade. Your users can browse the Skip list, and apply the changes on a case-by-case basis. Your customers have the option of setting com.glide.apps.include\_my\_deletes to false, which will skip writing Skip records as well.

5.  In the Uninstall confirmation dialog box, review the tables and records associated with the application before you uninstall that application.

6.  To delete all data associated with this application, clear the **Retain tables and data** check box.

    Leave this check box selected to remove only application files.

7.  Click **OK**.

8.  In the confirmation dialog box, enter `uninstall` and click **OK**.

9.  Click **Done**.


**Parent Topic:**[Rolling back and removing applications](../concept/c_RemovingApplications.md)

