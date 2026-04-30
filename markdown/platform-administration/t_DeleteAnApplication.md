---
title: Delete an application
description: As an administrator, you can delete custom applications that are no longer needed. Generally, you only delete applications that have never been shared with other instances.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Rolling back and removing applications, Installation considerations, Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Delete an application

As an administrator, you can delete custom applications that are no longer needed. Generally, you only delete applications that have never been shared with other instances.

## Before you begin

-   To ensure that you can reinstall the application later, first publish a backup of your application to the ServiceNow application repository, ServiceNow Store, or an update set. See [Application sharing](https://www.servicenow.com/docs/access?context=c_SharingApplications&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

Role required: admin

## About this task

This process ensures that the system can support any published applications. When you delete an application, all the records that are associated with the application, such as tables, business rules, and menus, are also deleted.

## Procedure

1.  Log in to the instance from which you want to delete the installed application.

2.  Navigate to **All** &gt; **System Applications** &gt; **My Company Applications**.

3.  Select the application that you want to delete.

4.  In the application record, select **Delete**.

    A confirmation message indicates if any application files are associated with the application you’re deleting.

5.  Select the appropriate option.

    |Option|Description|
    |------|-----------|
    |**Show Files**|Navigate to a listing of files associated with the application record. Review this listing and determine how to remove the files before deleting the application itself.|
    |**Delete**|Delete the selected application.|
    |**Cancel**|Cancel deletion of the files associated with the selected application.|

6.  In the confirmation message box, enter `delete` and select **OK**.

    If any remaining metadata files are associated with the application record, the system prevents its deletion until all associated files are removed.


## Result

Unless the application extends other applications, or files are still associated with the application, the system deletes the application.

**Note:** If an application is linked to Source Control \(that is, the Git repository\), you must also delete the Git configuration record for an application in the Repository Configurations \(sys\_repo\_config\) table. Without deleting this record, the application can't be reimported from Source Control on this instance.

**Parent Topic:**[Rolling back and removing applications](../concept/c_RemovingApplications.md)

