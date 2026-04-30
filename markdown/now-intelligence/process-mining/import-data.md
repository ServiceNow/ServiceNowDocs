---
title: Import data into the audit table
description: Import external dataset into the audit table to start working with the data in Process Mining.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with external datasets, Using Process Mining, Process Mining, Platform Analytics]
---

# Import data into the audit table

Import external dataset into the audit table to start working with the data in Process Mining.

## Before you begin

-   [Create an audit table](create-table.md)

You can import using ServiceNow Integration Hub or any other application. This section describes how to import data using ServiceNow Integration Hub.

Role required: sn\_process\_optimization\_admin

## Procedure

1.  Select **Import using Integration Hub**, in the Import Data section.

    ![Import using Integration Hub](../image/ext-dataset-3.png)

    A dialog box appears requesting you to confirm your selection, and reminding that after importing data from Integration Hub, you must come to this page again.

2.  Select **Proceed to Integration Hub**.

    Integration Hub opens in a new tab.

3.  Select **Create new integration**.

4.  On the NEW DATA IMPORT INTEGRATION page fill the fields.

    **Note:** Ensure to specify `Process Mining for external data` in the **Application** field.

    ![New data import integration](../image/ext-data-inthub1.png)

5.  Select **Save &amp; continue**.

6.  Select and configure your data source.

    1.  Select **File** as a source type from the drop-down list.
    2.  Select either Excel or CSV depending on how your data is stored.

        **Note:** It is good if you have the date formatted as jjjj-mm-dd uu:mm:ss. This reduces the transformation time in Integration Hub. Also, it is recommended that you use a CSV file for ease of import.

7.  You must now map source to target.

    1.  Select **Add a table**.
    2.  Select a target table. This must be the same table that you created.
    3.  Map the target fields with the source fields.
    ![Map the source and target fields](../image/ext-data-inthub2.png)

8.  Schedule your imports.

    For detailed information, see [Integration Hub - Import](https://www.servicenow.com/docs/access?context=integrationhub-imports&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).


**Parent Topic:**[Working with external datasets](../concept/external-dataset.md)

