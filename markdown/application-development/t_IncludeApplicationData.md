---
title: Create application files to include sample data
description: Include sample records from an application data table when sharing a custom application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Create application files to include sample data

Include sample records from an application data table when sharing a custom application.

## Before you begin

Role required: admin, or delegated\_developer

## About this task

The system can export selected records as application files that are included as part of the application update set when you share it. Including application files in an update set is not intended for the export and import of large numbers of records between instances. If you are trying to move data between instances, see [Import from another instance](https://www.servicenow.com/docs/access?context=c_ImportingFromAnotherSNInstance&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) instead.

The application data only includes the version of the records that existed when the records were shared. The system does not update this snapshot of the application data when the records change. Application designers can include data on a table by table basis.

## Procedure

1.  Navigate to the list for an application data table.

2.  Filter the list to display the records you want to include.

3.  Perform the appropriate action for the list version.

    |Version|Action|
    |-------|------|
    |**List v2**|Open any column context menu and select **Create Application Files**.|
    |**List v3**|Open the list title menu and select **Create Application Files**.|

4.  For **Load When**, select when the application record includes application data.

<table id="choicetable_amy_wdd_br"><tbody><tr><td id="d51078e133">

**__New Install and Upgrades__**

</td><td>

Includes application data whenever the application is installed or upgraded.

</td></tr><tr><td id="d51078e145">

**__New Install__**

</td><td>

Includes application data only when the application is installed.

</td></tr><tr><td id="d51078e157">

**__New Install with Demo Data__**

</td><td>

Includes application data only when the application is installed with demo data.

</td></tr></tbody>
</table>5.  Click **OK**.

    The system adds the records to the application files related list.

    ![Include application data](../image/IncludeApplicationData.png)

6.  Repeat steps 1–5 for each application data table you want to include.


**Parent Topic:**[Application sharing](../concept/c_SharingApplications.md)

