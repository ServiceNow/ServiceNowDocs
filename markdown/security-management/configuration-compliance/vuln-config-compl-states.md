---
title: Configuration Compliance states
description: With Configuration Compliance, you can see a state model to learn what the status of the remediation task is at any given time. The remediation task states control the test result states by precedence.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Configuration Compliance reference information, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance states

With Configuration Compliance, you can see a state model to learn what the status of the remediation task is at any given time. The remediation task states control the test result states by precedence.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Remediation Task States

Remediation tasks \(RTs\) have many possible states. Automatic transition is available from the Resolved state based on the next scan results. If all test results pass on the next scan, the remediation task is closed. Otherwise, it transitions to the Under Investigation state. The system verifies this closed state, but it re-evaluates the remediation task state if a test result is added to or deleted from the remediation task. The work notes are updated to reflect the transition.

The following figure shows how the state of a remediation task transitions from the Open state to the Closed state.

![Configuration Compliance state flow.](../image/CC-State-Flow.png "Configuration Compliance state flow (prior to v15.0)")

**Note:**

-   Each remediation task form contains **Follow** and **Update** buttons, which are standard for ServiceNow tasks.
-   Starting with v15.0 of Configuration Compliance, the following have been removed:
    -   **Close** button
    -   the **Resolution** field in the Resolve modal.

The following table lists the Configuration Compliance states.

<table id="table_hsr_mfq_hbb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open

</td><td>

State upon creation.

</td></tr><tr><td>

Under Investigation

</td><td>

Triggered by the **Start Investigation** button. From this state, you can:-   **Create a Change Request**

For more information, see [Create a change request in Configuration Compliance](../task/cc-CR-v12-create.md).

-   **Request exception**

Provide a reason and select a reopen date.

-   **Delete**

Confirm the deletion. Removes the remediation task.

-   **Mark as false positive**

Provide a reason and notes. Marks the remediation task as false positive.


</td></tr><tr><td>

In Review

</td><td>

Triggered when the remediation task is being assessed for the next action. Typically used to validate investigation outcomes or approve proposed changes/exceptions before implementation. From this state, you can transition to any of the following based on your approval or rejections:-   **Awaiting Implementation**

Transition to awaiting implementation if approved

-   **Under Investigation**

Transition back to under investigation if further analysis is required.

-   **Delete**

Confirm the deletion. Removes the remediation task.


</td></tr><tr><td>

Deferred

</td><td>

Triggered by the **Defer** button. From this state you can:-   **Reopen**

Transition back to an Open state.

-   **Delete**

Confirm the deletion. Removes the group.


Deferment information appears under the **Defer/Close** related tab. On the defer date, the group reopens for remediation.

</td></tr><tr><td>

Awaiting Implementation

</td><td>

Triggered by the **Awaiting Implementation** button. From this state you can:-   **Create a Security Incident**

For more information, see [Create a security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

-   **Create a Change Request**

For more information, see [Create a change request in Configuration Compliance](../task/cc-CR-v12-create.md).

-   **Resolve**

In the **Resolution notes**, add the reason why you are resolving the Remediation Task.

The state becomes Resolved. Notes appear under the **Resolution** related tab.

-   **Delete**

Confirm the deletion. Removes the remediation task.


</td></tr><tr><td>

Resolved

</td><td>

Triggered from the **Resolve** button. From this state you can:-   **Create a Security Incident**

For more information, see [Create a security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

-   **Reopen**

Transition back to an Open state.

-   **Delete**

Confirm the deletion. Removes the remediation task.


 Notes appear under the **Notes** related tab. Resolution information appears under the **Resolution** related tab. The notes reflects in the **Work notes** of all the test results associated with the Remediation Task.

</td></tr><tr><td>

Closed

</td><td>

Triggered from the **Close** button or **Mark as false positive** button. Starting from v14.12 of Configuration Compliance, you can close a remediation task by marking it as false positive.

From this state you can:

-   **Reopen**

Transition back to an Open state.

-   **Delete**

Confirm the deletion. Removes the group.


 Closure information appears under the **Defer/Close** related tab. The notes reflects in the **Work notes** of all the test results associated with the Remediation Task.

</td></tr></tbody>
</table>-   If the Remediation Task is marked as Closed or Fixed and if the test result added is not itself Closed or Fixed, the test result state does not change, and the remediation task state is changed to Open.
-   When you create a new remediation task or split a remediation task, the **Reason**, and **Until** fields are reevaluated for new and old remediation tasks. When the state of all test results is Deferred, the value in the **Reason** and **Until** fields are rolled up to the remediation task.

    -   If all the test results in a remediation task are deferred, and have the same **Reason**, then the remediation task is assigned the same **Reason**. Otherwise, the **Reason** field is changed to **None**.
    -   The date in the **Until** field is updated with the closest until date of all the remediation tasks to which the test results belong to.
    **Note:** This evaluation is done by the **Rollup test result values to test result RT1nd configuration test** scheduled job, which runs every one hour.

-   If the **Last Seen** is greater than the **Resolution date** for a resolved test result, then the test result is reopened. In a resolved Remediation Task, if at least one test result is reopened during ingestion, then the remediation task moves to the Under investigation state.

## Test Result States

The state of a remediation task also changes the state of its associated test results. This mechanism has two cases:

-   **Test results that belong to only one remediation task**

    Results match the state of the remediation task with three exceptions:

    -   If the remediation task changes its state to Closed and its resolution \(substate\) to Fixed, the item ignores that change and then falls back to the Open state.
    -   If the remediation task changes its state to Closed and its resolution \(substate\) to Cancelled, the item ignores that change and then falls back to the Open state.
    -   If the test result source status is Fixed \(updated by a scan or import\), then when the remediation task changes its state, the test result changes its state to Closed \(Fixed\) no matter what state the remediation task is in.
-   **Test results that belong to multiple remediation tasks**

    Test results do not match the state of the remediation task automatically. Instead, it searches among all the associated groups to find the state with the highest precedence to apply. This is the state of precedence:

    **Closed** &gt; **Closed \(substate: False positive\)** &gt; **Deferred** &gt; **Resolved** &gt; **In Review** &gt; **Awaiting Implementation** &gt; **Under Investigation** &gt; **Open** &gt; **Closed \(substate: Cancelled\)** &gt; **Closed \(substate: Fixed\)**

    **Note:** **Closed \(substate: Fixed\)** and **Closed \(substate: Cancelled\)** are two special cases.


**Note:** Starting with v15.0 of Configuration Compliance, the **Result Invalid** substate has been deprecated.

## Remediation Task state examples

For example:

<table id="table_yry_cbb_jbb"><thead><tr><th>

Remediation Tasks State

</th><th>

Test result State

</th></tr></thead><tbody><tr><td>

RT1: **Open** &gt; **Under Investigation** RT2: **Open**

</td><td>

**Under Investigation** When RT1 is Under Investigation and RT2 is Open, the test result changes to Under Investigation, since after the search, between RT1 and RT2, RT1 has the state with the highest precedence.

</td></tr><tr><td>

RT1: **Under Investigation** RT2: **Open** &gt; **Under Investigation**

</td><td>

**Under Investigation** When RT2 is Under Investigation and RT1 is Under Investigation, the test result stays as Under Investigation, since after the search, between RT1 and RT2, they have the state with the same precedence.

</td></tr><tr><td>

RT1: **Under Investigation** RT2: **Under Investigation** &gt; **Awaiting Implementation**

</td><td>

**Awaiting Implementation** When RT2 is Awaiting Implementation and RT1 is Under Investigation, the test result changes to Awaiting Implementation, since after the search, between RT1 and RT2, RT2 has the state with the highest precedence.

</td></tr><tr><td>

RT1: **Under Investigation** &gt; **Deferred** RT2: **Awaiting Implementation**

</td><td>

**Deferred** When RT1 is Deferred and RT2 is Awaiting Implementation, the test result changes to Deferred, since after the search, item 1 found out that between RT1 and RT2, RT1 has the state with the highest precedence

</td></tr><tr><td>

RT1: **Deferred** RT2: **Awaiting Implementation** &gt; **Closed \(Result Invalid\)**

</td><td>

**Closed \(Result Invalid\)** &gt; **Deferred** When RT2 is Closed and the resolution \(substate\) is Result Invalid, and RT1 is Deferred, the test result changes to Closed \(Result Invalid\), since after the search, between RT1 and RT2, RT2 has the state with the highest precedence.

</td></tr><tr><td>

RT1: **Deferred** RT2: **Closed \(Result Invalid\)** &gt; **Open \(via Reopen\)**

</td><td>

**Deferred** When RT2 is re-opened and its state changes to Open, and RT1 is Deferred, the test result changes to Deferred, since after the search, between RT1 and RT2, RT1 has the state with the highest precedence.

</td></tr><tr><td>

RT1: **Deferred** RT2: **Awaiting Implementation** &gt; **Closed \(False Positive\)**

</td><td>

**Closed \(False Positive\)**When RT2 is Closed and the resolution \(substate\) is False Positive and RT1 is Deferred, the test result changes to Closed \(False Positive\), since after the search, between RT1 and RT2, RT2 has the state with the highest precedence.

</td></tr></tbody>
</table><table id="table_qww_c2b_jbb"><thead><tr><th>

Remediation Task State

</th><th>

Test result state

</th></tr></thead><tbody><tr><td>

RT1: **Under Investigation** RT2: **Awaiting Implementation** &gt; **Closed \(Fixed or Cancelled\)**

</td><td>

**Under Investigation** When RT2 is Closed \(substate Fixed or substate Cancelled\), and RT1 is Under Investigation, the test result changes from Awaiting Implementation \(previously, the highest precedence\) to Under Investigation \(currently, the highest precedence\).

</td></tr><tr><td>

RT1: any stateRT2: any state

</td><td>

If the test result source status is Fixed \(updated by a scan or import\), then when the remediation task changes its state, the test result changes its state to Closed \(Fixed\) no matter what states the other associated remediation tasks are in. The test result search for remediation task state does not occur.

</td></tr></tbody>
</table>## State roll-up and roll-down scenarios

State roll-up and roll-down scenarios automatically sync the status of remediation tasks \(RTs\) and configuration test result \(CTR\), ensuring real-time updates across both. This dynamic interaction reduces manual tracking, enhances accuracy, and provides users with an up-to-date view of progress, making configuration compliance more efficient and helping users make informed decisions quickly.

## Roll-up behaviour

When configuration test result \(CTR\) state change, these changes may propagate up to the remediation task \(RT\) level.

The following table summarizes key roll-up scenarios where changes in configuration test result \(CTR\) state may influence the associated remediation task \(RT\) state, based on closure conditions, reassignments, and deferrals.

|CTR State|RT State|
|---------|--------|
|Open &gt; Closed-Fixed|Open &gt; Closed-Fixed|
|Open &gt; Closed-Stale|Open &gt; Closed-Cancelled|

## Roll-down behaviour

When the state of a remediation task changes, the state is often propagated to the associated CTRs unless overridden by manual updates or exceptions.

The following table summarizes key roll-up scenarios where changes in remediation task \(RT\) state may affect the associated configuration test result \(CTR\) state, based on precedence rules and special conditions.

|RT State|CTR State|
|--------|---------|
|Open &gt; Under Investigation|Open &gt; Under Investigation|
|Open &gt; In Review|Open &gt; In Review|
|Open &gt; Deferred|Open &gt; Deferred|
|Deferred &gt; Open|Remains Deferred|
|Open &gt; Resolved-Fixed|Open &gt; Resolved-Fixed|
|Open &gt; Resolved-Fixed &gt; Closed-Fixed|Open &gt; Resolved-Fixed &gt; Closed-Fixed|
|Open &gt; Resolved-Result Invalid|Open &gt; Resolved-Result Invalid|
|Open &gt; Resolved-Cancelled|Open &gt; Resolved-Cancelled|
|Open &gt; Resolved-Cancelled &gt; Closed|Open &gt; Resolved-Cancelled &gt; Closed|
|Open &gt; Resolved-Result Invalid &gt; Closed-Result Invalid|Open &gt; Resolved-Result Invalid &gt; Closed-Result Invalid|
|Open &gt; Closed-Fixed|Open &gt; Closed-Fixed|

**Parent Topic:**[Configuration Compliance reference information](../reference/cc-reference-info.md)

