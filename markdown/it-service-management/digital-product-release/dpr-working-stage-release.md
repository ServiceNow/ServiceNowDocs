---
title: Managing a stage-oriented release
description: Managing a stage-oriented release involves completing objectives and closing the release when the work is done and meets the defined release criteria, rather than waiting for the planned end date.
locale: en-US
release: xanadu
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2025-04-25"
reading_time_minutes: 2
breadcrumb: [Manage releases for digital products and services, Using Digital Product Release, Digital Product Release, IT Service Management]
---

# Managing a stage-oriented release

Managing a stage-oriented release involves completing objectives and closing the release when the work is done and meets the defined release criteria, rather than waiting for the planned end date.

## Stage-oriented release process

Stage-oriented process is suitable for creating releases that prioritize completing objectives and features over following a strict timeline.

The following is the general flow that a stage-oriented release goes through:

-   The flow starts with the first phase in the Pending state, which is the default state. The state of the phase moves to In Progress when you manually start it.

    Tasks in the phase are processed based on the system property **sn\_dpr.sequential\_task\_execution**:

    -   **true**: Tasks in the phase are processed in sequential order. At the start of a phase, the task with the lowest order in it is set to the Open state. After this task is completed, the next task in the order is opened. This process continues for the remaining tasks in the phase. If the task is an approval task, the state is moved to the Requested state.
    -   **false**: Tasks in the phase are not processed in a sequence. Instead, all its tasks are set to the Open state at the start of the phase.
-   When the all tasks are completed and all policies are compliant or compliant with exceptions for the current phase, it automatically moves to the Completed state.
-   After the current phase is completed, the next phase moves to the In Progress state. Only one phase can be in progress at a given time.
-   If you encounter any issues at any point, you can restart from a previously completed phase. That phase and later phases are reset, including tasks and policy status.
-   When all phases in the release are completed, the release moves to the Review state.
-   When the review of the release is completed, the release moves to the Completed state.

For more information, see [Release for a product or service](dpr-product-release.md).

## Working on a stage-oriented release

<table id="table_g42_jt4_kyb" class="nav-card"><tbody><tr><td>

 

</td><td>

[Work on a release for a single product or service![](../image/dpr-icon-rls-single.png)Learn about working on a stage-oriented release to deliver a single product or service.](../task/dpr-work-stage-release.md#)

</td><td>

[Work on a release for multiple products![](../image/dpr-icon-rls-multi.png)Learn about working on a stage-oriented release to deliver multiple products.](../task/dpr-work-release-stage-multi.md)

</td><td>

 

</td></tr></tbody>
</table>