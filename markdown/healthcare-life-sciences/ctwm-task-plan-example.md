---
title: Example - Task plans for care teams
description: Understand how task plans are designed and executed using Care Team Work Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/ctwm-task-plan-example.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Example - Task plans for care teams

Understand how task plans are designed and executed using Care Team Work Management.

In a large hospital system, operational leaders need a reliable way to run across rounding activities consistently many departments without manually coordinating work unit by unit. The **Operational rounding playbook** is designed for this purpose, providing a standardized and repeatable workflow that initiates, coordinates, and tracks rounding activities across multiple care units.

When the task plan is executed, the system begins by creating one **healthcare orchestration case** that represents the entire rounding cycle across the hospital. This healthcare Orchestration case serves as the hospital‑wide coordination record, allowing leadership to manage the effort as a single initiative regardless of how many units are involved.

As part of this orchestration layer, the system generates **healthcare orchestration tasks** for rounding coordinators and operational leaders. These tasks typically include activities such as preparing rounding checklists and communications, reviewing submitted assessments from all units, and compiling exceptions or escalating findings. These healthcare orchestration tasks are visible only to leadership roles and don’t involve frontline staff, confirming that coordination and oversight remain separate from unit‑level execution.

For each selected unit or department, the system then creates a **care team case**, providing a unit‑specific container for frontline rounding work. Each care team case includes a clear description of the rounding activity and sets expectations for what must be completed during the rounding cycle. Within each care team case, the system generates **care team tasks** that guide unit‑level execution, such as environmental assessments, equipment checks, and patient safety checklists. These tasks are assigned to care team managers or care team agents within the appropriate unit and may include documentation requirements or smart assessments as needed.

As care team staff complete their assigned tasks, progress is tracked at both the unit and hospital levels. Unit‑level completion is captured within care team cases and tasks, while overall progress across all units is monitored from the healthcare orchestration case. This enables rounding coordinators to quickly identify which units are complete, which are still in progress, and where exceptions or compliance gaps may exist.

Once all units have completed their required tasks and assessments, the rounding coordinator closes the healthcare orchestration case, completing the rounding cycle. This multi‑unit task plan approach improves operational reliability, reduces manual coordination, and supports compliance with internal policies and regulatory requirements across the health system.

## Example - Care team activities task plans for care teams

A care team task plan author can use the **Care team activities playbook** to standardize recurring unit-level work. This includes shift readiness checks or routine equipment inspections, without coordinating each unit manually.

When the author creates the plan, a plan details form appears. It contains the same short description, priority, and description fields used by the Operational rounding playbook's Care team case stage. The author then defines the individual **care team tasks** that make up the plan, including the task name, instructions, an owner, and the expected outcome.

When a task should capture standardized evidence, the author can associate a smart assessment to the task. The assessment can be scoped with a conditional execution rule so it only appears when specified conditions are met.

The author then selects the **eligible care teams and units** that should receive the plan. When the plan is saved, the system generates a care team case and its associated care team tasks for each selected team or unit.

Finally, the author configures the plan's **schedule** as immediate, one time, or recurring using the same scheduling stage as the Operational rounding playbook.

The author then reviews the complete plan on the Plan Summary stage before publishing. Once published, care team cases and tasks are generated automatically according to the configured schedule.

Progress can be tracked the same way as any other care team task plan.

