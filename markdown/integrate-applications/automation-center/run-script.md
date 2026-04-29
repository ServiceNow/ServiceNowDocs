---
title: Run fix script to view results
description: Run a fix script in ServiceNow to view the results of the automation explorer.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 1
breadcrumb: [Use, Now Assist for Automation Center, Use, Automation Center, Workflow Data Fabric]
---

# Run fix script to view results

Run a fix script in ServiceNow to view the results of the automation explorer.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Definition** &gt; **Fix Scripts**.

2.  Locate the fix script with the following sys\_id:

    ```
    21a11b363ba4321037da9f7e53e45a50
    ```

    Use the list filter or the search bar to find the record by sys\_id if it is not immediately visible.

3.  Open the fix script record, and select **Run Fix Script**.

4.  Review the output logs that appear after the execution completes.

    Confirm the following statistics are present in the output:

    -   Total Processed — the total number of records evaluated by the script.
    -   Records Created — the number of new records generated during processing.
    -   Records Skipped — the number of records that did not meet processing criteria.
    -   Errors — any errors encountered during execution. Investigate and resolve before re-running the script if errors are present.

**Parent Topic:**[Using Now Assist for Automation Center](../concept/use-now-assist.md)

