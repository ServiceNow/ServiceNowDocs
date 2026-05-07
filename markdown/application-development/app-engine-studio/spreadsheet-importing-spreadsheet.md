---
title: Import a spreadsheet
description: Upload a Microsoft Excel spreadsheet and use it to create your application data model.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use a spreadsheet, Create a data model, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Import a spreadsheet

Upload a Microsoft Excel spreadsheet and use it to create your application data model.

## Before you begin

Check that the spreadsheet meets the following requirements:

-   Formatted with horizontal columns and a header label for each
-   Saved as an XLSX file type

**Note:** The Excel spreadsheet you upload can have multiple worksheet tabs, each of which you might use to create a data table. If multiple worksheets are present, you will be prompted to select which worksheet tab to create the table from after you upload the file.

Role required: admin, sn\_app\_eng\_studio.user or delegated developer permissions. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Next to the Data heading, select the Add icon \(![Add icon](../image/plus-icon.png)\).

4.  Select **Import a spreadsheet**, and then select **Continue**.

5.  Upload your spreadsheet and then select **Continue**.

    You can drag the spreadsheet file onto App Engine Studio or browse your computer.

6.  You will be presented with one of the following paths:

    -   If your spreadsheet only has a single worksheet tab, proceed to the next step.
    -   If the spreadsheet has multiple worksheet tabs, you will have a list of sheets to choose from. From this list of sheets, you can select which worksheet tab to add as a table to your application first.
    1.  In the **Enter a row number for the table header** field, enter the row number in which the sheet column headers are located.

        For example, if the headers are in the second row, enter `2`.

    2.  To upload the information below the column headers in the sheet \(e.g., the data in your spreadsheet\), select the **Import spreadsheet data** option.

        To upload only the column headers, leave the check box cleared. You may want to upload only the headers if you intend to use this table as a template and don't want any of the other data added to your AES table.

7.  Make one of the following selections.

    -   If you have uploaded an Excel file with multiple worksheet tabs, select **Convert to table** to proceed with converting the selected worksheet tab to a table, and then proceed to next step.
    -   If you have uploaded an Excel file with a single worksheet tab, select **Continue**.
    Options display for where to import your file into.

8.  Based on what you would like to do with your spreadsheet data, navigate to one of the following procedures to continue.

<table id="choicetable_f24_f5g_vvb"><tbody><tr><td id="d103067e224">

**Create a new table directly from the spreadsheet import**

</td><td>

Refer to [Create new table from spreadsheet import](spreadsheet-create-new-table.md) for next steps.

</td></tr><tr><td id="d103067e243">

**Create a new table by extending an existing table, and then using the spreadsheet import to update it**

</td><td>

Refer to [Create new table from extensible table and spreadsheet import](spreadsheet-create-new-ext-table.md) for next steps.

</td></tr><tr><td id="d103067e262">

**Use spreadsheet import to update an existing application table**

</td><td>

Refer to [Modify existing table using spreadsheet import](spreadsheet-import-existing-table.md) for next steps.

</td></tr></tbody>
</table>
**Parent Topic:**[Use a spreadsheet to add data](upload-multi-sheets.md)

