---
title: Import data into the account onboarding playbook
description: As part of the Customer Success Management process, you can import, configure, and publish data.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data capture and validation, Set up playbook, Account onboarding, Customer Success Management, Customer Success Management]
---

# Import data into the account onboarding playbook

As part of the Customer Success Management process, you can import, configure, and publish data.

## Before you begin

-   Role required: admin

## About this task

After completing the first stage in the Customer Success Management playbook, you can continue with the **Data Capture &amp; Validation** stage. In the header section, you can see the account name, the person it’s assigned to, days remaining, account status, and the data import status. Several default tables have been configured with the base system.

To import data into these default tables, follow these steps:

## Procedure

1.  In the `Upload & process files` tab, select **Upload files**.

2.  In the Upload files window, select **Add file**, select the file and then select **Upload**.

    **Note:** Verify that the XLSX file contains the accurate data that passes all the pre-defined validation checks or any custom validations that have been defined.

    The uploaded file appears in the Upload &amp; process file page.

    ![Account onboarding: uploaded files](../image/account-onboarding-data-upload.png)

    You can upload multiple files. For each uploaded file, the name of the file, the date on which it was uploaded, the person who uploaded the file, and upload status \(Unprocessed\) is displayed.

3.  Select one or more files to be uploaded, and select **Process files**.

    If any of the files being uploaded contains validation errors, none of the files get uploaded to the staging table, and an error message is displayed. You must fix all the errors before uploading the files. If there are no validation errors, you’ll see a message indicating that files are being uploaded and once the process is complete, the upload status changes to `Processed`.

4.  Navigate to the `Validate records` tab.

5.  When the `Data has been successfully validated! Please check the staging table.` message appears, the records are moved into one of the following states:

    -   Ready to publish: The records have no validation errors and can be published.
    -   Needs attention: Records in this state have some issues that must be addressed.
    -   Yet to validate: Records in this state haven’t been validated.
6.  Review the records in the **Needs attention** state, verify the information in the Comment column, and modify the record if necessary, and select **Save**.

7.  After editing the record, navigate to the **Yet to validate** list, and select **Validate**.

8.  When all the records are in the **Ready to publish** list, select the records to be published, and select **Publish**.

    **Note:**

    -   If you’re importing multiple files at a time, the data import process may slow down.
    -   While the data is being validated, select **Add more** to import more files and process them in parallel.
    -   If the imported data is corrupted or has several errors, select **Restart**. This action clears all the data in the staging table and restarts the process from the beginning. Data in the **Ready to publish** state is also cleared.
    -   Select the **View details** toggle icon to view the record details.
    -   Select **Close task**. Enter the Close notes and select **Close Task**. The State field is updated to `Closed` and the Progress field is updated to **Finished** and the data import task is closed.
9.  Select **Close**.

10. Review the Data Import Summary, enter Close Notes for each task, and select **Mark complete** to continue with the next stage in the playbook.


## What to do next

-   Select **Discuss** to start a sidebar discussion about this data import task. In the pop-up window, select the participants for the discussion, enter a brief message, and select **Start discussion**. A window appears with a link to the record for this onboarding case. Select **Open record** to open the record and start the discussion. When the discussion has been completed, you can see the details in the Activity stream.
-   Open the Activity stream and select **Email** from the More drop down list. Enter the required details and select **Send email**.

    **Note:** You can send emails only to the team members associated with the account.


**Parent Topic:**[Data capture and validation](../concept/account-lifecycle-use-playbook-data-capture.md)

