---
title: Asset work order plans in Enterprise Asset Management
description: Work order plans organize sequential asset tasks — such as shutdowns, safety inspections, calibrations, asset condition assessments, and restarts — under a single unified plan, enabling repeatable and scalable execution.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-02-23"
reading_time_minutes: 1
breadcrumb: [Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Asset work order plans in Enterprise Asset Management

Work order plans organize sequential asset tasks — such as shutdowns, safety inspections, calibrations, asset condition assessments, and restarts — under a single unified plan, enabling repeatable and scalable execution.

**Important:** Work order plans are available with Enterprise Asset Management version 10.0 and later.

## Key benefits

-   Increased operational efficiency: Organize complex asset-centric tasks under a single plan with support for technician assignment and scheduling.
-   Guided experience: Create, assign, track, and complete work order plans through a structured Playbook interface.
-   Asset-centric workflows: Sequence maintenance operations across multiple assets or asset groups for consistent and repeatable execution.

## Roles

The following roles are involved in the work order plan workflow:

-   Asset manager \(sn\_eam.asset\_manager\): Creates and manages work order plans, defines the scope of work, assigns work order tasks to technicians, and schedules and tracks tasks.
-   Asset technician \(sn\_eam.asset\_technician\): Receives assigned tasks with all instructions and completes tasks using the Mobile Agent application with real-time status updates.

## Work order plan workflow

The work order plan workflow involves the following stages:

1.  Details: Create a work order plan by providing the details of the assets or asset groups in scope, and the work order tasks to be performed. Tasks can include safety preparation, shutdown, maintenance, calibration, asset condition assessment, and restart.
2.  Review affected assets: Confirm the assets to include in the work order plan.
3.  Review assignments: Assign work order tasks to assignment groups or technicians.
4.  Review schedule: Set the scheduled start and end times for each work order task.
5.  Track status: Track task status updated by the assigned technicians and review the available work order plan reports.

For details on creating work order plans, see [Manage asset-centric work tasks using work order plans](manage-work-order-plans.md).

