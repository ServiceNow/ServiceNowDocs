---
title: Get started with CI Lifecycle Management
description: Follow these high level steps to get started and to track activities of the CI Lifecycle Management module of the CMDB application.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CMDB CI Lifecycle Management \(legacy\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Get started with CI Lifecycle Management

Follow these high level steps to get started and to track activities of the CI Lifecycle Management module of the CMDB application.

## Before you begin

Role required: none

## Procedure

1.  Activate the base system [CI Lifecycle Management - Restore Internal State Management Tables](enable-cilifecyclemgmt-job.md) scheduled job that continuously checks and maintains data integrity of all internal CI Lifecycle Management tables.

2.  [Define CI actions](define-cmdb-ci-action.md).

3.  [Define compatible CI actions](dfn-cmptbl-cmdb-ci-action.md) rules.

    Navigate to **All** &gt; **Configuration** &gt; **CI Lifecycle Management** &gt; **CMDB CI Actions** to display currently active/inactive CI actions in the CMDB.

4.  [Define not-allowed CI actions](non-allowed-cmdb-ci-action.md) rules.

5.  [Define not-allowed operational state transitions](not-allowed-oprtionl-trnston.md) rules.

6.  Define new operational states by modifying the **operational\_status** field in the \[cmdb\_ci\] table in the system dictionary.

    Navigate to **All** &gt; **Configuration** &gt; **CI Lifecycle Management** &gt; **View Internal Operational States** to display available operational states set by each requestor.

7.  [Set priority for operational states](set-priority-operational-state.md).

8.  Call APIs to apply CI actions.

    Navigate to **All** &gt; **Configuration** &gt; **CI Lifecycle Management** &gt; **CMDB CI Actions** to display which actions were submitted and thier active/inactive state in the CMDB.

9.  Navigate to **All** &gt; **Configuration** &gt; **CI Lifecycle Management** &gt; **View CI State Registered Users** to display currently registered operators that were registered via the registerOperator API.

10. Review Renew Lease tasks and extend leases as needed: Navigate to **All** &gt; **Configuration** &gt; **CI Lifecycle Management** &gt; **Renew Lease Tasks**. These tasks are created automatically by the **CI Lifecycle Management - Restore Internal State Management Tables** scheduled job for CI action records in which the lease for a valid requester has expired. The Requestor should use the lifecycle management API **ExtendCIActionLease** to extend the lease. Otherwise, if the lease remains expired for a specified grace period, the **CI Lifecycle Management - Restore Internal State Management Tables** scheduled job marks the respective CI action record as ‘inactive'.

    The grace period for expired lease time is configurable by the system property **glide.cmdb.statemgmt.max\_lease\_expired\_days**.

11. Navigate to **All** &gt; **Configuration** &gt; **CI Lifecycle Management** &gt; **State Management Logs** to display logs of CI Lifecycle Management operations.


**Parent Topic:**[CMDB CI Lifecycle Management \(legacy\)](../concept/cmdb-ci-lifecycle-mgmt.md)

