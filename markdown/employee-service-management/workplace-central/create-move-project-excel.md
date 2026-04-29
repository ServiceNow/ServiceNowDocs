---
title: Create a move project by uploading an Excel file
description: As a move manager, create a move project by uploading an Excel file that contains move-related information for the employees.
locale: en-US
release: australia
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 5
breadcrumb: [Working with Move management, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
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

    You can download the Excel template required to create the move project by selecting the **Download excel template** link.

6.  Upload an Excel file that contains move-related information.

    The file must contain move-related information in the appropriate columns. The maximum supported file size is 10 MB.

    You can download an Excel template by selecting **Download standard excel template**. For more information about the character limit of the Excel columns, see [Excel column lengths for move projects](../reference/move-excel-char-limit.md).

    **Note:** If you have an existing file, you must delete it to upload a different file. You can delete the file by using the context menu.

    1.  In the **Attachments** section, select **Attach file**.

    2.  From your local system, select the file that you want to upload.

    3.  On the **Upload a file** pop-up, select **Upload**.

        You can edit the name of the uploaded file based on your preference.

    4.  After the file is uploaded, select **Next**.

    The system takes some time to process the uploaded file and loads the data in a staging table. After the move information is processed, the system displays information about data issues and business conflicts.

    **Important:** Data stored in the Move staging table \(to process data issues or conflicts\) is archived after seven days. Make sure that you create move cases before the data is archived.

7.  On the `Fix data issues` page, review the information and resolve the conflicts.

    Conflicts like non-existent employee or same source and destination are stored as data issues. You must resolve the issues or remove the conflicted records to continue. For more information about data issues, see [Move conflicts for projects created via Excel upload](../reference/excel-upload-conflicts.md).

    1.  Perform any of the following actions based on your requirement.

        -   You can delete records by selecting the check boxes, then selecting **Delete**.
        -   You can edit a record by selecting the edit icon \(![Edit icon in the shape of a pencil.](../../../reuse/icons/product-icons/pencil-outline-24.svg)\) for the record.
        -   You can edit multiple records by selecting the check boxes, then selecting **Edit**.
    2.  After resolving the conflicts, select **Reprocess and continue**.

        The system reprocesses the records and displays any remaining data conflicts. Repeat the steps to resolve all the conflicts.

        If all the conflicts are resolved, the system proceeds to the `Review conflicts` step.

8.  On the `Review conflicts` page, review the information and resolve the conflicts.

    Conflicts like allocation mismatch or exceeding capacity are shown as business conflicts. For more information about the conflicts, see [Move conflicts for projects created via Excel upload](../reference/excel-upload-conflicts.md).

    **Note:** You can ignore the conflicts and continue by selecting **Next**.

    1.  Perform any of the following actions based on your requirement.

        -   **Edit**: You can edit the move information in the move information table to fix data issues or resolve business conflicts.
        -   **Ignore**: You can ignore the conflict and resolve it after the move cases are created.
        -   **Remove**: You can remove the move information record from the move information table. Move cases aren't created for removed records.
    2.  After making the changes, select **Next**.

9.  Create the move cases by selecting **Create move cases**.

    You can go back and edit records in the conflicts table before creating the move cases.

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

