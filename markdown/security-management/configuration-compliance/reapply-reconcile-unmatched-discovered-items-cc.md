---
title: Reconcile unmatched discovered items for Configuration Compliance
description: Create a schedule job to reconcile unmatched discovered items. When a test result is created, the configuration item \(CI\) added to it at the time of creation might be an outdated one.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Discovered Items for Configuration Compliance, Configuration Compliance imported data, Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Reconcile unmatched discovered items for Configuration Compliance

Create a schedule job to reconcile unmatched discovered items. When a test result is created, the configuration item \(CI\) added to it at the time of creation might be an outdated one.

## Before you begin

Role required: admin

## About this task

If the information in the CMDB changes, unmatched CI information is not reconciled. To reconcile, apply CI lookup rules on the test results that are in an unmatched state when the CMDB is updated with the latest CIs.

A schedule job is run on demand to reapply the CI matching rule for the discovered items in an unmatched state. If the CI changes after reapplying the lookup rules, the discovered items are updated with the new CI. Impacted test results are also updated. For details, see [CI changes for discovered items for Configuration Compliance](../concept/reapply-discovered-items-ci-changes-cc.md).

**Note:**

Starting with Configuration Compliance v24, you can skip the reapplication of CI lookup rules on discovered items with the substate ‘CI Decommissioned’ by enabling the system property **sn\_sec\_cmn.skipItemsWithCIDecommissioned**.

## Procedure

1.  Navigate to **All** &gt; **Security Operations &gt; Reconcile Unmatched Discovered Items**.

2.  On the Background Jobs page, click **Create reconciliation job**.

3.  On the form, fill in the fields.

    **Note:** You can only edit the Parameters field.

<table id="table_tqk_fb3_4mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique job number.

</td></tr><tr><td>

Created by

</td><td>

User who created the job.

</td></tr><tr><td>

Parameters

</td><td>

Parameters to reconcile the unmatched discovered items:-   limit: Maximum number of discovered items to be reconciled. If you do not enter a value, 10,000 discovered items are reconciled.
-   firstDiscovereditem: First discovered item that must be reconciled. If you do not enter a value, the reconciliation process starts from the first discovered item.


</td></tr><tr><td>

State

</td><td>

Current state of the background job.

</td></tr><tr><td>

State description

</td><td>

Description of the current state of the background job.

</td></tr><tr><td>

Job type

</td><td>

Type of job. The value is **Reconcile unmatched discovered items**.

</td></tr><tr><td>

Started at

</td><td>

Time when the job started.

</td></tr><tr><td>

Ended at

</td><td>

Time when the job was completed.

</td></tr><tr><td>

Job duration

</td><td>

Total time taken to complete the job.

</td></tr><tr><td>

Substate

</td><td>

Substate for the selected state.

</td></tr><tr><td>

Notes

</td><td>

Number of records processed.

</td></tr></tbody>
</table>4.  Click **Submit**.

    **Note:**

    -   To stop running the job, click **Cancel**.
    -   You cannot reconcile unmatched CIs or reapply CI lookup rules while importing hosts or test results.

