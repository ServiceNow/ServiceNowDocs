---
title: Import data into the account onboarding playbook
description: As part of the Account Lifecycle Events process, you can import, configure, and publish data.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Data capture and validation, Set up the account onboarding playbook, Configuring account onboarding, Account onboarding, Account Lifecycle Events]
---

# Import data into the account onboarding playbook

As part of the Account Lifecycle Events process, you can import, configure, and publish data.

## Before you begin

-   Role required: admin

## About this task

After completing the first stage in the Account Lifecycle Events playbook, you can continue with the **Data Capture &amp; Validation** stage. Several default tables have been configured with the base system. To import data into these default tables, follow these steps:

## Procedure

1.  Open the first table and click **Open record**.

2.  In the Data Import page, click the **Details** tab.

    In the Contact field, select the customer contact who is working on this case.

3.  Click the **Attachment** icon in the right-hand panel.

4.  In the Attachments section, click the **Actions** icon and click **Download**.

5.  Open the XLSX file and enter all records you wish to upload.

    **Note:** Ensure that the XLSX file contains the accurate data that will pass all the pre-defined validation checks or any custom validations that have been defined.

6.  Click the plus icon to select one or more Excel files from the list and click **Upload**.

7.  Click **Import from attachments** and select the files to be imported.

8.  Click **Import** to upload the data and move it to the staging table.

9.  When the `Data has been successfully validated! Please check the staging table.` message appears, the records are moved into one of the following states:

    -   Ready to publish: The records have no validation errors and can be published.
    -   Needs attention: Records in this state have some issues that must be addressed.
    -   Yet to validate: Records in this state haven’t been validated.
10. Review the records in the **Needs attention** state, verify the information in the Comment column, and modify the record if required.

11. After editing the record, navigate to the **Yet to validate** list, and click **Validate**.

12. When all the records are in the **Ready to publish** list, select the records to be published, and click **Publish**.

    **Note:**

    -   If you are importing multiple files at a time, the data import process may slow down.
    -   While the data is being validated, you can click **Add more** to import more files and process them in parallel.
    -   If the imported data is corrupted or has several errors, select **Restart**. This action clears all the uploaded data in the staging table and restarts the process from the beginning. Data in the **Ready to publish** state will also be cleared.
13. Select **Close**.

14. Review the Data Import Summary, enter Close Notes for each task, and select **Mark complete** to continue with the next stage in the playbook.


