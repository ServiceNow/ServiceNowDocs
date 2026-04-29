---
title: Release for a product or service
description: A release groups all the tasks \(projects, epics, stories, enhancements, defects, problems, incidents, and so on\) planned for a specific version of a product or service. Digital Product Release provides two different processes: timeline-oriented and stage-oriented, to help you in executing your releases.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Explore, Digital Product Release, IT Service Management]
---

# Release for a product or service

A release groups all the tasks \(projects, epics, stories, enhancements, defects, problems, incidents, and so on\) planned for a specific version of a product or service. Digital Product Release provides two different processes: timeline-oriented and stage-oriented, to help you in executing your releases.

A release is divided into a series of phases. During each phase, a defined list of tasks, approval processes, and policies must be fulfilled.

A defined release process ensures that the work items in releases are built, tested, and are ready for deployment.

## Timeline-oriented release process

Timeline-oriented process is suitable for creating releases that have fixed deadlines and follow a strict schedule.

This process helps you prioritize tasks, allocate resources, and track progress against the timeline so you can make adjustments as needed to stay on track. Use this release process to:

-   Set clear deadlines for each stage of your deployment, so you can plan and execute your rollout smoothly.
-   Keep your team on track by defining clear goals, so you can manage your resources effectively.
-   Track your progress against key dates, and adjust your plans as needed to stay on schedule.

The following is the general flow that a timeline-oriented release goes through:

-   The flow starts with the first phase in the Pending state, which is the default state. The state of the phase moves to In Progress when it starts on the planned start date.

    Tasks in the phase are processed based on the system property **sn\_dpr.sequential\_task\_execution**:

    -   **true**: Tasks in the phase are processed in sequential order. At the start of a phase, the task with the lowest order in it is set to the Open state. After this task is completed, the next task in the order is opened. This process continues for the remaining tasks in the phase. If the task is an approval task, the state is moved to the Requested state.
    -   **false**: Tasks in the phase are not processed in a sequence. Instead, all its tasks are set to the Open state at the start of the phase.
-   When all tasks are completed and policies are compliant, the phase ends automatically on its planned end date. The phase state updates to the Completed state.
-   After the current phase is completed, the next phase moves to the In Progress state. Only one phase can be in progress at a given time.
-   When all phases in the release are completed, the release moves to the Review state.
-   When the review of the release is completed, the release moves to the Completed state.

## Stage-oriented release process

Stage-oriented process is suitable for creating releases that prioritize completing objectives and features over following a strict timeline.

Certain products are not constrained by a specific time frame for how long they should remain in a particular phase. Releases for those products can follow the stage-oriented release process. This process focuses on making sure that the product is ready to be released, rather than following a strict schedule or phase.

You can finish a release as soon as the product meets the set criteria, instead of waiting for a specific timeline or phase to end. However, you must ensure that all aspects of the release, including development, testing, and quality assurance, are done well to keep the product high quality.

Use this release process to:

-   Set priorities for features and goals, instead of deadlines, so that you can adjust your plans throughout the development process.
-   Restart the release from any of the previous phases to adjust goals and features based on testing results and user feedback.
-   Track your progress by ensuring features are completed and the goals are met for a high-quality result.

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

## System properties to control the release processes

The following system properties control the initiation of automated actions during various stages of the release process.

-   sn\_dpr.stage\_workflow\_auto\_transition
-   sn\_dpr.auto\_transition\_release\_to\_review
-   sn\_dpr.auto\_transition\_release\_to\_completed

For more information about these properties, see [Digital Product Release properties](../reference/digital-product-release-properties.md).

## Single product or service release

A single product or service release enables you to release one product or service at a time. This release approach can be useful for smaller or less complicated products or services, as it makes the release process more focused and easier to manage. For more information, see [Work on a timeline-oriented release for a single product or service](../task/dpr-work-release.md#) and [Work on a stage-oriented release for a single product or service](../task/dpr-work-stage-release.md#).

## Multi-product release

A multi-product release enables you to release different products at the same time. You can do this by including several individual releases for each product, all tied to a main release of a primary product or service. You manage the phases and release readiness from the main release and track the collective progress. However, you can set the scope, track approvals, and run policies for each individual product or service release.

This release approach differs from release bundles, where you monitor the progress of multiple releases together but manage them independently.

For more information, see [Work on a timeline-oriented release for multiple products](../task/dpr-work-release-timeline-multi.md) and [Work on a stage-oriented release for multiple products](../task/dpr-work-release-stage-multi.md).

-   **Adding or removing a product from a multi-product release**

    You can add and remove products from a multi-product release after it is created. When you add a product, a child release is created with phases, tasks, and policies aligned to the main release. When you remove a product, the child release is cancelled and removed from the main release.

-   **Phase management in a multi-product release**

    In a multi-product release, the following phase synchronization rules apply:

    -   Individual releases cannot advance past main release: An included product cannot complete a phase that is ahead of the main release's current phase.
    -   Main release cannot advance past individual releases: The parent release cannot advance to the next phase if any included product has not yet reached the parent's current phase. All included products must be at the current phase before the main release can advance.

        These rules ensure that all products in a multi-product release progress through phases in a coordinated manner.

    When a product is added to a release that is already in progress, the newly added product starts at the earliest phase. The system automatically executes the policies mapped to each phase sequentially:

    -   If all policies for a phase are compliant, the phase is completed and the release advances to the next phase.
    -   This process repeats through each phase until the product either catches up to the parent release's current phase or a policy evaluation fails.
    -   If a policy evaluation fails, the product's phase remains at the non-compliant phase and the status shows as Non Compliant — policy execution failed. You must resolve the non-compliance before the product can advance further.This can be done by either making the policies compliant or using the **Complete phase** action to force completion.
-   **Policy execution lifecycle and status aggregation**

    Policies mapped to release phases follow a defined lifecycle during execution:

    -   **Not run**: The policy has not been executed yet.
    -   **In progress**: The policy execution is underway.
    -   **Compliant**: The policy passed validation.
    -   **Non-compliant**: The policy failed validation.
    -   **Compliant with exception**: The policy failed but an approved exception is in place.
    The policy run status for all primary and included products is aggregated to determine the overall policy status of the main release. The aggregation follows a priority hierarchy where a non-compliant status in any product results in an overall non-compliant status for the release.

    For more information, see [Policy status aggregation in a multi-product release](../reference/dpr-policy-status-aggregation.md).


**Parent Topic:**[Exploring Digital Product Release](dpr-exploring-digital-product-release.md)

**Related topics**  


[Create a release for a product or service](../task/dpr-create-release.md)

[Managing timeline-oriented releases](dpr-working-timeline-release.md)

[Managing stage-oriented releases](dpr-working-stage-release.md)

[Managing multiple releases through release bundles](dpr-release-bundle.md)

