---
title: Delete intelligence records
description: Delete records from Threat Intelligence library.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-23"
reading_time_minutes: 1
breadcrumb: [TISC Data Archival, Use, Threat Intelligence Security Center, Security Operations]
---

# Delete intelligence records

Delete records from Threat Intelligence library.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click **Threat Intel Library** icon on the workspace.

3.  Open any record.

4.  Go to **Source Records** section.

5.  Select **Delete** to delete the source records.

6.  Delete the library record.

    **Note:**

    1.  If a library record with associated source records is deleted, then the source records will be reprocessed, and a new library record will be created by aggregating the field values from the source records.
    2.  To permanently delete the data from the threat intel library, use archival rules instead of deleting the library records. For more information, see [TISC Data Archival](tisc-data-archival.md).

