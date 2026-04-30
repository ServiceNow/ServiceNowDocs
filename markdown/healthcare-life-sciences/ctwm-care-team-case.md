---
title: Care team cases and tasks
description: Care team cases group related operational work for a care team, while care team tasks represent the individual, actionable steps that users complete to fulfill that work.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Care team cases and tasks

Care team cases group related operational work for a care team, while care team tasks represent the individual, actionable steps that users complete to fulfill that work.

## Care team case

Care team cases are generated from task plans and have associated care team tasks.

The care team case \[sn\_cto\_case\] table contains cases pertaining to Care Team Work Management at the unit level.

Once a task plan is executed, the system generates care team cases and care team tasks for each impacted unit.

A care team task is the unit‑level container for work. It includes:

-   The unit’s task list
-   Required assessments or checklists
-   Evidence capture fields
-   Assignment details for the care team agent manager

## Care team task

The care team task \[sn\_cto\_task\] table contains tasks attached to care team cases.

Care team tasks represent the hands‑on work care team agents must complete, such as:

-   Conducting room or equipment checks
-   Performing shift readiness steps
-   Documenting safety concerns
-   Completing Smart Assessments

Tasks are fulfilled in the Healthcare Operations Workspace.

Care team agent managers monitor progress and complete the case once all tasks are finished.

