---
title: Create a move project by uploading an Excel file
description: As a move manager, create a move project by uploading an Excel file that contains move-related information for the employees.
locale: en-US
release: xanadu
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2025-06-06"
reading_time_minutes: 4
breadcrumb: [Working with Move management, Use Workplace Central, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Create a move project by uploading an Excel file

As a move manager, create a move project by uploading an Excel file that contains move-related information for the employees.

## Before you begin

Verify that you have the following plugins installed:

-   Workplace Central
-   Workplace Move Management

Role required: sn\_wsd\_move.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center by navigating to **Workspaces** &gt; **Workplace Central**.

2.  Select the Move management \(![Move management icon.](../images/move-mgmt-icon-central.png)\) module.

3.  Select **Create project**.

    You can also create a move project from the following locations:

    -   Select **My active projects** tile and select **Create** in the list view.
    -   In the **All move projects** section, select **View all**. In the list view, select **Create**.
    -   You can also create a move project while deploying a scenario. After you select the **Deploy** action, in the dialog box, select **Create move project**.

        **Important:** The option is displayed only if there are any workplace user or workplace location moves in the scenario.

4.  On the Create a move project form, specify a name and short description for the project.

5.  Select **Create move cases via excel upload**, then select **Create**.

6.  Upload an Excel file that contains move-related information.

    The file must contain move-related information in the appropriate columns. You can download an Excel template by selecting **Download excel template**. For more information about the character limit of the Excel columns, see [Excel column lengths for move projects](../reference/move-excel-char-limit.md).

    1.  On the **Upload file** card, select **Attach file**.

    2.  On the **Attachments** pop-up, select **Select file**.

    3.  Select a file from your local system, then select **Upload**.

        To attach a different file, you must remove the existing file by using the context menu.

    4.  After the file is uploaded, close the pop-up window.

    The system takes some time to process the uploaded file and loads the data in a staging table. After the move information is processed, the system displays information about data issues and business conflicts.

7.  On the Move information page, review the information and resolve the conflicts.

    **Note:** Data stored in the Move staging table \(to process data conflicts\) is archived after seven days. Make sure that you create move cases before the data is archived.

    Conflicts like non-existent employee or same source and destination are stored as data conflicts. Conflicts like allocation mismatch or exceeding capacity are shown as business conflicts. For more information about the conflicts, see [Move conflicts for projects created via Excel upload](../reference/excel-upload-conflicts.md).

<table id="choicetable_ydj_ts3_tfc"><thead><tr><th align="left" id="d204843e257">

Action

</th><th align="left" id="d204843e260">

Steps

</th></tr></thead><tbody><tr><td id="d204843e266">

**Resolve data conflicts**

</td><td>

1.  On the Data conflicts card, select the view move data conflicts icon.
2.  On the Move Data Conflicts tab, resolve the conflicts by editing or deleting the records.
    -   You can delete records by selecting the check boxes, then selecting **Delete**.
    -   You can edit a record by selecting the edit icon \(![Edit icon in the shape of a pencil.](../../../reuse/icons/product-icons/pencil-outline-24.svg)\) for the record.
    -   You can edit multiple records by selecting the check boxes, then selecting **Edit**.
3.  After resolving the conflicts, select **Reprocess**.

The system reprocesses the records and displays any remaining data conflicts. If all the conflicts are resolved, the conflict list is empty.

</td></tr><tr><td id="d204843e315">

**\[Optional\] Resolve the business conflicts**

</td><td>

-   **Edit**: You can edit the move information in the move information table to fix data issues or resolve business conflicts.
-   **Ignore**: You can ignore the conflict and resolve it after the move cases are created.
-   **Remove**: You can remove the move information record from the move information table. Move cases aren't created for removed records.


</td></tr></tbody>
</table>8.  Create the move cases by selecting **Create move cases**.

    The system takes some time to create move cases based on the move information records. You can view the progress by opening the move project.


If you accidentally close a move project after uploading an Excel file, the system displays a loading screen when the move project is opened. To close the loading screen and edit the project, select **Edit Move Project**.

## What to do next

-   Review the created cases on the **Move cases** tab:
    -   The **List** view displays details like the status and move dates for the cases.
    -   The **Calendar** view displays the planned move dates for the move cases. You can schedule the cases by moving them on the calendar.
-   Review the move tasks that are created for the move cases. The **Move tasks** tab displays details like the priority and status of the move tasks.
-   View the project details, comments, work notes, and activity on the **Move project details** tab.

**Note:** The move project isn't marked complete even if all the child cases are closed. You can add more cases to the project from the Schedule View or the List View.

For more information about working on a move project, see [Work on a move project](work-on-a-move-project.md).

**Parent Topic:**[Working with Move management](../concept/working-with-move-management.md)

**Related topics**  


[Create a move project from existing move requests](create-move-project.md)

[Work on a move project](work-on-a-move-project.md)

