---
title: Test result and remediation task state transitions in the Configuration Compliance application
description: The states of configuration test records and their associated remediation tasks \(RTs\) are impacted if test result records are deferred, resolved, reopened, and transferred to other remediation efforts \(REs\).
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Test result and remediation task state transitions in the Configuration Compliance application

The states of configuration test records and their associated remediation tasks \(RTs\) are impacted if test result records are deferred, resolved, reopened, and transferred to other remediation efforts \(REs\).

## State transition scenarios between test results and remediation tasks

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

The following table details how states and sub-states transition between configuration test results and remediation tasks.

<table id="table_eyp_43m_w1c"><thead><tr><th>

If a remediation task state transitions from...

</th><th>

...to state/sub-states

</th><th>

Its associated test results states transition from...

</th><th>

...to state/sub-states

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open

</td><td>

Under Investigation

</td><td>

Open

</td><td>

Under Investigation

</td><td>

States transition bi-directionally.

</td></tr><tr><td>

Open

</td><td>

In Review

</td><td>

Open

</td><td>

In Review

</td><td>

States transition bi-directionally.

</td></tr><tr><td>

Open

</td><td>

Deferred/with any reason selected for Resolution

</td><td>

Open

</td><td>

Deferred

</td><td>

Test results keep the same reason for Resolution as the remediation task.

</td></tr><tr><td>

Deferred/with any reason for Resolution

</td><td>

Open

</td><td>

Test results remain Deferred

</td><td>

 

</td><td>

Test results keep the same Resolution as the remediation task.

</td></tr><tr><td>

Open

</td><td>

Resolved/ Fixed

</td><td>

Open

</td><td>

Resolved

</td><td>

States/sub-states transition bi-directionally.

</td></tr><tr><td>

Open

</td><td>

Resolved and Resolved to Closed/Fixed

</td><td>

Open

</td><td>

Resolved

</td><td>

If a remediation task transitions to Closed/Fixed, it can transition back to Open. If the task transitions to Open, its associated test results transition from Resolved back to Open.

</td></tr><tr><td>

Open

</td><td>

Resolved

</td><td>

Open

</td><td>

Resolved

</td><td>

States/sub-states transition bi-directionally.

</td></tr><tr><td>

Open

</td><td>

Resolved/Cancelled

</td><td>

Open

</td><td>

Resolved

</td><td>

States/sub-states transition bi-directionally.

</td></tr><tr><td>

Open

</td><td>

Resolved and Resolved to Closed

</td><td>

Open

</td><td>

Resolved

</td><td>

If a remediation task transitions to Closed automatically, its associated test results can transition back to Open.

</td></tr><tr><td>

Open

</td><td>

Resolved and Resolved to Closed/Result Invalid

</td><td>

Open

</td><td>

Resolved and Resolved to Closed/Result Invalid

</td><td>

If a remediation task transitions to Resolved it can transition back to Open.

 If a remediation task transitions to Closed/Result Invalid, it and its associated test results cannot be reopened.

</td></tr><tr><td>

Open

</td><td>

Closed/Fixed

</td><td>

Test results remain Open

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>**Note:**

-   Starting with v14.12 of Configuration Compliance, the **Result invalid** option is removed in the **Resolution** field in the Close modal.
-   Starting with v14.12 of Configuration Compliance, the **Remediation Task State Approval** workflow is deprecated and replaced by the flow Remediation Task State Approval in the flow designer.

