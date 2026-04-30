---
title: Activate the CI Lifecycle Management scheduled job
description: When starting to use the CI Lifecycle Management module, ensure to activate the CI Lifecycle Management - Restore Internal State Management Tables scheduled job which is disabled by default. This scheduled job continuously checks and maintains the data integrity of all internal CI Lifecycle Management tables.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CMDB CI Lifecycle Management \(legacy\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Activate the CI Lifecycle Management scheduled job

When starting to use the CI Lifecycle Management module, ensure to activate the **CI Lifecycle Management - Restore Internal State Management Tables** scheduled job which is disabled by default. This scheduled job continuously checks and maintains the data integrity of all internal CI Lifecycle Management tables.

## Before you begin

Role required: none

## About this task

When CI Lifecycle Management operations do not complete properly, for example due to a failure of the requestor or a requestor whose lease has expired, the integrity of tables related to CI Lifecycle Management might be compromised. The **CI Lifecycle Management - Restore Internal State Management Tables** scheduled job scans tables related to CI Lifecycle Management, and does the following:

-   De-activates or removes all internal lifecycle management records with invalid requestors, and closes any corresponding Renew Lease Tasks if present.
-   Detects records associated with a valid requestor whose lease has expired, and automatically creates a Renew Lease Task to notify the user and to provide details for extending the lease. If the requestor takes no action and the lease remains expired for a specified grace period \(default 15 days\), automatically de-activates the corresponding CI action record, and closes any corresponding Renew Lease Task if present.

## Procedure

1.  Navigate to **System Definition**, and click **Scheduled Jobs**.

2.  Search for the **CI Lifecycle Management - Restore Internal State Management Tables** job.

3.  In the respective **Active** column, double-click the value **false**, and select **true**.

4.  Click the **Save** icon.


**Parent Topic:**[CMDB CI Lifecycle Management \(legacy\)](../concept/cmdb-ci-lifecycle-mgmt.md)

