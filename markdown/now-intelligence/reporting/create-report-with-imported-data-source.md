---
title: Create a Core UI report from an imported Microsoft Excel document
description: You can import Excel spreadsheets \(.xlsx files\) of data maintained outside of your instance and create reports from those files.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a Core UI report from an imported Microsoft Excel document

You can import Excel spreadsheets \(`.xlsx` files\) of data maintained outside of your instance and create reports from those files.

## Before you begin

Role required: pa\_admin, report\_admin

You must have the subscription version of Performance Analytics to create reports with imported data. See [Activate your Performance Analytics subscription](../../performance-analytics/concept/c_PremiumPerformanceAnalytics.md#).

The following restrictions apply to imported data:

-   The maximum file size is 2 MB.
-   The maximum number of rows is 10,000. The maximum number of columns is 25.

    **Note:** You can import `.xlsx` files of up to 50,000 rows, but only the first 10,000 rows appear in your data set.

-   Only the first sheet of an `.xlsx` file with multiple sheets is imported.
-   The first row and first column of the imported file must not be empty. The first row is used to identify the column names.
-   It is not possible to join columns, calculate fields, or make other changes to the table after import. These changes must be made before import.
-   The imported `.xlsx` file must have a specified expiration date.
-   If the owner deletes the table after import, reports based on the imported table are also deleted.

**Note:** Report\_view access control lists \(ACLs\) have to be defined for users to view these reports. For more information, see [Report\_view access control](../concept/report-view-access-control.md).

## About this task

Importing report data in this way is useful when you have information that is maintained outside of your instance, for example, recurring third-party data. To import an external data set into your instance permanently, see [Importing data using import sets](https://www.servicenow.com/docs/access?context=c_ImportDataUsingImportSets&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

## Procedure

1.  Navigate to `sys_reports.list` and select **New**.

2.  On the **Data** tab, give the report a name that reflects the information being grouped.

3.  In the **Source type** list, select **External import**.

    ![Source type menu, External import option selected](../image/source-type-ext-import.png)

    **Note:** The **External import** menu option is only available if the subscription for Performance Analytics is enabled.

4.  Choose an existing imported report source, or select the **Upload** icon \(![Upload icon](../image/upload-icon.png)\) icon to import a file.

5.  If you selected **Upload**, follow these steps:

    1.  Select and drag the file onto the drop zone that opens, or select **Browse files** to choose it from your file system.

    2.  In the Upload external source dialog that opens, specify a name for the report source being created from the uploaded file.

        Note this name. You need it later to set the report\_view Access Control Lists \(ACLs\).

        ![Importing the file 'asset inventory.xslt' as the new report source "External asset inventory."](../image/excel-file-upload.png)

    3.  Set the expiration of the report source.

        After this date, the imported file is deleted and reports based on it are no longer available.

    4.  Select who can see the report source:

        -   Only you
        -   All users
        -   Specified users, groups of users, or roles
        **Note:** This setting does not affect report\_view ACLs.

    5.  Select **Upload**.

    6.  Select **Done**.

        The file is saved as a new table on your instance.

6.  Select **Next**.

7.  Complete report creation as normal.

    For information on specific report types, see [Report types](../reference/report-types-creation-details-rd.md). For general information about creating reports, see [Create a report](t_CreateYourOwnReport.md#).

8.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.

9.  Create report\_view ACLs for the table you created when you uploaded the external data in Step 4.

    To view the report you created, users must have report\_view access to this table.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  Search for a table whose name contains the name of the report source you specified in Step 4b.

        For example, if you uploaded a file named 'External asset inventory,' you would search for `*external_asset` and find the table u\_rep\_snc\_global\_admin\_external\_asset\_inventory, reflecting that it was created in the global scope by an admin user.

        ![The table that was created by the external file import, in the list of tables.](../image/aanbouw-table.png)

    3.  Copy the table name.

    4.  Navigate to **All** &gt; **System Security** &gt; **Access Control \(ACL\)**.

        The admin role with the elevated security\_admin role is required. If you are not an admin, consider passing the table name to a ServiceNow AI Platform administrator along with a request for the desired roles to have report\_view read permission.

    5.  Create report\_view ACLs for roles that you want to be able to read the report, as described in [Report\_view access control](../concept/report-view-access-control.md).


## Result

The report is created from the external source. On a dashboard, this report has an icon to show that the report is temporary and expires when the external data source expires.

## What to do next

Share the report, as described in [Distribute reports](../concept/c_DistributeReports.md).

-   **[Edit an imported data source](edit-config-external-data-source.md)**  
You can edit imported Excel spreadsheets \(`.xlsx` files\) of data maintained outside of your instance.

**Parent Topic:**[Advanced Core UI reporting topics](../concept/c_AdvancedReporting.md)

