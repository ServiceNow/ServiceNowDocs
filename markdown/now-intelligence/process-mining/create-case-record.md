---
title: Create case records for the imported data
description: Create case records for the imported data as it is important for creating a project and mining it. Without a record table, a project can’t be created.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/create-case-record.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with external datasets, Using Process Mining, Process Mining, Platform Analytics]
---

# Create case records for the imported data

Create case records for the imported data as it is important for creating a project and mining it. Without a record table, a project can’t be created.

## Before you begin

-   [Create an audit table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/create-table.md)
-   [Import data into the audit table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/import-data.md)
-   [Verify the imported data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/verify-data.md)

Role required: sn\_process\_optimization\_admin

## Procedure

1.  After you’ve validated your imported data, create a record table from the Record Data section.

2.  Select an option under **How do you wish to add the record table?**.

    If your audit table has custom fields, then the two options are grayed out. By default, **Generate record data table** is selected.

3.  Select **Create record table**.

    \[Omitted image "ext-dataset-recordtable.png"\] Alt text: Create case records for external dataset

    After the record table is created, a tab opens displaying details of the audit and record tables.

    \[Omitted image "ext-data-edit.png"\] Alt text: External dataset created


**Parent Topic:**[Working with external datasets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/external-dataset.md)

