---
title: Edit an imported data source
description: You can edit imported Excel spreadsheets \(.xlsx files\) of data maintained outside of your instance.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a report from an imported spreadsheet, Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Edit an imported data source

You can edit imported Excel spreadsheets \(`.xlsx` files\) of data maintained outside of your instance.

## Before you begin

Role required: None, but only the person who imported the data source can edit it.

## About this task

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run**.

2.  Click the name of a report that uses to imported data source to open the report in the Report Designer.

3.  On the **Data** tab, click the pencil icon \(![](../../dashboards/image/EditWidgetButton.png)\) next to the name of the external import.

4.  In the **Edit external import** dialog box you can make these changes:

    -   **Change file**

        Select this option to upload a new `.xlsx` file with the same name and structure.

    -   **Name**

        Provide a new name for the external import. This name appears on the **Data** tab of the Report Designer in the **External Import** list.

    -   **Expire**

        Set a new expiry date for the external import.

        After this date, the imported file is deleted and reports based on it are no longer available.

    -   **Visible to**

        Change the visibility for the uploaded file: Only you, Everyone, or Custom. Select **Custom** to specify users, groups, or roles.

        If you select **Custom**, click **Next** to choose who can use the data in the imported file and click **Submit**.

5.  Click **Submit**.


## Result

If you changed the file, the data from the new file replaces that of the old in any reports that are based on the imported file. Changed name, expiry date, and visibility apply to the imported file.

**Parent Topic:**[Create a Core UI report from an imported Microsoft Excel document](create-report-with-imported-data-source.md)

