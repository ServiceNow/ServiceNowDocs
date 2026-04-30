---
title: Use Auto-Close Stale Test Results in Configuration Compliance
description: Activate Auto-Close Stale Test Results \(TRs\) to automatically close older test results based on filter conditions that you set.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-08-08"
reading_time_minutes: 2
breadcrumb: [Automatically closing stale test results in Configuration Compliance, Remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Use Auto-Close Stale Test Results in Configuration Compliance

Activate Auto-Close Stale Test Results \(TRs\) to automatically close older test results based on filter conditions that you set.

## Before you begin

For more information about this feature, key terms, and any setup that may be required for your third-party integrations that import test result data, see [Automatically closing stale test results in Configuration Compliance](../concept/cc-autoclose-tr-overview.md).

Role required: sn\_vulc.admin

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Auto-Close Stale Test Results**.

2.  Fill in the fields

    |Field|Value|
    |-----|-----|
    |Name|Name for this configuration record.|
    |Active|If selected, this record is active and it will automatically close any test results that match its filter criteria.|
    |Ignore stale TRs for deferred TRs|If selected, any TRs that are mapped to the **In-review** or **Deferred** states are ignored and not closed. If you clear this option, any TRs that match your criteria will be closed.|
    |Execution order|100 is the default value. This value determines the order of execution in ascending order for each configuration record used for locating and marking test results that are stale.|
    |Description|A description for this record. This text might help you easily find it again if you create a larger number of records.|
    |Condition|The filtering conditions used for finding TRs that you want closed. The default filter is **Discovered Item** &gt; **Last scan**.|

3.  Click **Submit**.

    The scheduled job, **Auto-Close Stale Test Results**, runs daily. This job identifies the TRs based on the conditions that you provided and transitions the ones that match to State: **Closed**.

    After TRs are marked as State: **Closed-Stale**, if the scanner finds these TRs again, the test results are reopened and the states transition back to**Open**.

    If a TR is marked as State: **Closed-Stale**, and the scanner finds that it has been fixed \(Resolution: **Fixed**\), the TR transitions to State: **Closed** Resolution: **Fixed**. TRs that have **Result**: **Pass** remain as State: **Closed** Resolution: **Fixed**. States also roll up to remediation tasks as described in the following list:

    1.  If any TRs in a remediation task are **Open**, the remediation task state is not changed.
    2.  If at least one TR is State: **Closed** Resolution: **Fixed** and the rest are **Closed-Stale**, the remediation task state transitions to **Closed** Resolution: **Fixed**.
    3.  If all the TRs in a remediation task are **Closed** Resolution: **Fixed**, the TRG state transitions to State: **Closed** Resolution: **Canceled**.
    For more information about state transitions, see [Test result and remediation task state transitions in the Configuration Compliance application](../concept/cc-state-transition.md).


