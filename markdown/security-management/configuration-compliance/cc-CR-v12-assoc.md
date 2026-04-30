---
title: Associate a remediation task to an existing change request
description: Associate a remediation task in Configuration Compliance application to an existing change request.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Remediation, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Associate a remediation task to an existing change request

Associate a remediation task in Configuration Compliance application to an existing change request.

## Before you begin

Role required: a user with the itil role

## About this task

As an IT or remediation specialist, avoid creating duplicate change requests \(CHG\) as you work to resolve your remediation tasks by associating a remediation task \(RT\) to a change request that is already available in your instance.

You can associate remediation tasks that are assigned to you or your assignment group to existing change requests directly from the remediation task records. The following image illustrates the basic flow for associating an existing change request to a remediation task. The detailed steps for this flow follow the image.

**Note:** You can associate an existing change request to a remediation task in any state other than **Canceled** \(**Open**, **Under Investigation**, **Awaiting Implementation**, **Closed**, and **Deferred**\). Change requests, including those closed within the last 90 days, are available to associate from the form. When you associate a change request to an existing remediation task, only the active test results and their configuration items are added to the change request.

![States for test result group (remediation task) and change request in state synchronization](../image/associate_vg_to_cr-01.png)

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Remediation Tasks** &gt; **My Open Tasks**.

    The list of remediation tasks assigned to your groups is displayed.

2.  In the Number column, click the remediation task you want to create a change request for.

    The remediation task record is displayed.

3.  In the upper right of the record, click **Create Change**.

    The change request form is displayed.

4.  Scroll to the Change Requests related list and select it.

    Any change requests associated with the remediation task are displayed along with the **Add** button.

5.  Click **Add**.

    The Add Existing Change Request to Remediation Task dialog is displayed.

6.  Click the search icon and select an item from the list.

    You can filter the list that is displayed to narrow your search.

7.  Click **Submit**.

    The TRG is displayed along with a message that indicates the change request was successfully associated to the remediation task. Under the change requests related list, the new change request is displayed. The CIs from the remediation task are by default added to the change request and are displayed on the Affected CIs related list. You can also add CIs to the change request from this related list. A message indicates the number of test results that have moved to the new remediation task, and the new RT is displayed.

    **Note:** For under 200 test results, the split operation is done synchronously, and the test results are displayed in the new remediation task.

    For over 200 test results, the split operation is done asynchronously in the background, and it may take a few seconds for the test results to appear in the new remediation task. The following message is also displayed: `n test results will be moved from TRGxxxxxxx to new remediation task GRCxxxxx shortly.`

    You can associate any change requests to the remediation task, with the following exceptions:

    -   Change requests in the **Canceled** state.
    -   Change requests in the **Closed** state older than 90 days.
    -   Change requests already associated with the RT. The system will not permit you to associate a change request that is already associated with the RT.
    After the change request for this remediation task is resolved, if there are no other open change requests associated with this remediation task, the remediation task is also moved to the**Resolved** state.

    **Note:** You can still manually move change requests and remediation tasks through the states of their life cycles on their respective records with state synchronization enabled, but when the system registers that a change request has changed its state, or you add a change request or remove it from a remediation task, state synchronization potentially can override your manual intervention. However, change requests states do not automatically move the remediation task from the `Closed` or `Deferred` states.

    For more information, see [State synchronization between change requests and remediation tasks](cc-cr-state-synch.md).


