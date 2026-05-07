---
title: Monitor the integration status of the SLO inbound data import
description: Monitor the status of the integration after a transform runs and completes successfully.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Load supplier data, SLO integration framework, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Monitor the integration status of the SLO inbound data import

Monitor the status of the integration after a transform runs and completes successfully.

## Before you begin

Role required: admin

## Procedure

1.  After you run a transform and it completes successfully, do one of the following under the Next steps section:

    -   Import set number: Select the import set number link to view the import sets for this data load.

        Transform History: Select this option to view the transform history, related errors, and log.

    -   Import log: Select this option to view the import log.
2.  Select **All**.

3.  In the navigation filter, enter the name of the SLO inbound table for which you want to check the integration status.

    For example, to check the integration status of the Supplier location inbound table, enter **sn\_fcms\_intg\_supplier\_location\_inbound\_list.do**.

    The Supplier location inbounds page appears.

4.  Verify the following:

    -   If the primary tables were successfully updated, the Integration status column displays **New** for the import set.
    -   If the update to the primary tables was unsuccessful, the following occurs:
        -   The Integration status column displays **Failed** for the import set.
        -   The Processing message column displays the issue that occurred during the transformation. You must fix the error and run the transform again. For example, if any of the mandatory fields are missing, the integration fails and displays the missing data to aid you in fixing the error.

**Parent Topic:**[Load supplier data](load-supplier-data.md)

**Related topics**  


[Run transform to update supplier primary data](run-transform-supplier.md)

