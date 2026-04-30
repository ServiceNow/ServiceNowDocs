---
title: Mapping recovery tasks to phases
description: Starting with BCM, version 9.x.x, BCM administrators set up active phases for plans and events, enhancing recovery and event task management. BCM managers then map these phases to recovery and event tasks, executing them in a desired, logical sequence.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-10-06"
reading_time_minutes: 5
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Mapping recovery tasks to phases

Starting with BCM, version 9.x.x, BCM administrators set up active phases for plans and events, enhancing recovery and event task management. BCM managers then map these phases to recovery and event tasks, executing them in a desired, logical sequence.

## Implementing phases in recovery

Organizing recovery and event tasks into logical phases provides a structure and context to the recovery activities. The logical grouping of phases helps you to understand the progression of plans, exercises, and crisis events, maintain flexibility in execution, and navigate complex recovery processes effectively.

Phases act as indicators of the current status of plans, exercises, or crisis events, and they provide clarity while reviewing the recovery and event tasks. You can tag the recovery tasks and event tasks to an appropriate phase such as Preparation, Recovery, Post incident review, and so on as part of the recovery process. This mapping ensures structured and efficient handling of recovery tasks and event tasks.

## Default active phases

Recovery involves a series of phases, which are configured within the BCM core application. The base version of the application includes a set of default active phases, provided as seed data.

1.  Preparation
2.  Recovery
3.  Recovery validation
4.  Return to normal
5.  Return to normal validation
6.  Post-incident review

These predefined phases serve as a foundation for the recovery process.

BCM administrators have the flexibility to configure these phases to meet their organization's unique requirements.

-   **Phase column**

    Recovery and event tasks now include the Phase column in both list and form views, indicating association with specific phases within the recovery process. By default, the phase list view only displays active phases, streamlining the user experience.


## Benefit of mapping phases to plans or events

By setting up active phases in the BCM application and mapping them to relevant plans or events, BCM managers can efficiently manage their workflows.

## Phases for task classification

BCM Administrators can configure phases using the Active Phases module, which is accessible through the **General administration** menu in the Core UI. For more information on setting up the phases, see [Set up the phases](../task/set-up-phases.md).

## Execution of the phases

While phases are executed in a sequence, the application doesn’t enforce a strict sequential execution. However, certain phase transitions require completion of all tasks in the current phase before proceeding to the next phase.

For example, all tasks in the Preparation phase must be completed before moving to the Recovery phase, and all tasks in the Recovery validation phase must be completed before proceeding to the Return to normal phase.

-   Preparation → Recovery
-   Recovery validation → Return to normal

In contrast, phases such as Return to normal validation and Post-incident review can progress in parallel without requiring full task completion. For example, the Recovery and Recovery validation phases, or the Return to normal and Return to normal validation phases, can run in parallel.

By default, phases serve as a tagging mechanism, and the application doesn’t enforce task dependencies across them. If strict enforcement is needed—for example, ensuring Task 2 in Phase 1 starts only after Task 1 in Phase 2 is completed—a customization is required.

## Flexibility to exclude tasks and assets from time calculation

In previous releases, the total time calculation included the time required to complete all recovery tasks. The newly introduced **Do not include in time calculation** field in the recovery task form provides greater flexibility in time calculations, enabling you to exclude specific recovery or event tasks from these calculations.

How it works: When creating a recovery task, you can select the **Do not include in time calculation** check box to exclude specific tasks from time calculations. The actual time taken is then calculated based on the minimum start time and maximum end time of the included tasks. The total effort is the sum of the effort for each task, excluding those with the check box checked.

Excluding time calculation at asset level: You can also apply the exclude time calculation functionality at the asset level, allowing you to exclude specific assets from time calculations for individual tasks. This functionality enables accurate tracking of time and effort for relevant assets, helping you focus on critical tasks and assets. By providing this flexibility, the feature enhances the accuracy of time and effort calculations.

## UI changes and table updates

The user interface \(UI\) has been updated to include the phase column in both recovery tasks and event tasks. Additionally, a phase navigation module has been added under Business Continuity &gt; General Administration.

Recovery task and event task tables: The Recovery task table \(in BCM Planning\) and Event task table \(in BCM Exercises\) have been updated to include the phase column, which is a reference field.

These changes enhance the overall functionality and security of the BCM system, providing a robust and controlled environment for managing phases and related tasks.

## Information on setting up and mapping the phases

For information on setting up the phases, see [Set up the phases](../task/set-up-phases.md).

For information and steps on mapping recovery tasks to phases, see [Add recovery tasks](../task/add-a-recovery-task.md).

For information on mapping event tasks to phases, see [Mapping event tasks to phases](mapping-event-tasks-to-phases.md).

**Parent Topic:**[Structured workflows for BCPs](bcp-tasks-performed-by-bcp-owner.md)

