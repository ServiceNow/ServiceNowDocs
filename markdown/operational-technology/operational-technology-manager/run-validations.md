---
title: Run Validations
description: Run validations on records to find missing, duplicate, and invalid data.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing Validations, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Run Validations

Run validations on records to find missing, duplicate, and invalid data.

## Before you begin

Role required: ot\_staging\_user, cmdb\_ot\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager** &gt; **Import OT Devices - Staging table**.

2.  Select Run Validations to trigger validations in the staging table.

    Validations are run in the background for all records.

    The time that it takes to validate the data depends on the number of records present in the staging table.

3.  After the validation is complete, check the status of the record in the Validation state column in the staging table.

4.  If the status of the record is partially valid or invalid, do the following:

    1.  Check for the missing data in the record.

    2.  Make corrections in the record.

        The record can be edited in the staging table list view and in the record for view.

    3.  Update the record.

    4.  Run the validations.

5.  If the missing data is not available, do the following to override the state for the specific record to manually set that record as valid:

    1.  Select the record to open the form.

    2.  Select **Set to Valid**.

    **Note:**

    If any record is manually set as valid, it may cause reconciliation issues and a CI might not get created.


**Parent Topic:**[Managing Validations](../concept/managing-validations.md)

