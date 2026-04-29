---
title: Managing timeline-oriented releases
description: Managing a timeline-oriented release involves following a series of deadlines and milestones and adjusting as necessary to keep your release on track.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Managing timeline-oriented releases

Managing a timeline-oriented release involves following a series of deadlines and milestones and adjusting as necessary to keep your release on track.

## Timeline-oriented release process

Timeline-oriented process is suitable for creating releases that have fixed deadlines and follow a strict schedule.

The following is the general flow that a timeline-oriented release goes through:

-   The flow starts with the first phase in the Pending state, which is the default state. The state of the phase moves to In Progress when it starts on the planned start date.

    Tasks in the phase are processed based on the system property **sn\_dpr.sequential\_task\_execution**:

    -   **true**: Tasks in the phase are processed in sequential order. At the start of a phase, the task with the lowest order in it is set to the Open state. After this task is completed, the next task in the order is opened. This process continues for the remaining tasks in the phase. If the task is an approval task, the state is moved to the Requested state.
    -   **false**: Tasks in the phase are not processed in a sequence. Instead, all its tasks are set to the Open state at the start of the phase.
-   When all tasks are completed and policies are compliant, the phase ends automatically on its planned end date. The phase state updates to the Completed state.
-   After the current phase is completed, the next phase moves to the In Progress state. Only one phase can be in progress at a given time.
-   When all phases in the release are completed, the release moves to the Review state.
-   When the review of the release is completed, the release moves to the Completed state.

For more information, see [Release for a product or service](dpr-product-release.md).

## Working on a timeline-oriented release

<table id="table_g42_jt4_kyb" class="nav-card"><tbody><tr><td>

[Work on a release for a single product or service![Single product release icon.](../image/dpr-icon-rls-single.png)Learn about working on a timeline-oriented release to deliver a single product or service.](../task/dpr-work-release.md#)

</td><td>

[Work on a release for multiple products![Multi-product release icon.](../image/dpr-icon-rls-multi.png)Learn about working on a timeline-oriented release to deliver multiple products.](../task/dpr-work-release-timeline-multi.md)

</td></tr></tbody>
</table>