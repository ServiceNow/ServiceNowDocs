---
title: Industrial Failure Modes
description: Use Industrial Failure Modes to manage failure modes in the Industrial Connected Workforce.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Industrial Failure Modes

Use Industrial Failure Modes to manage failure modes in the Industrial Connected Workforce.

## Failure mode overview

A failure mode describes an anomalous condition that you may encounter in an industrial environment. The failure mode model defines a hierarchy of faults related to the ISA-95 equipment model. This hierarchy consists of the following two levels.

-   Failure mode categories
-   Failure modes

Failure mode categories are independent of the equipment model and serve as a grouping method for failure modes. They’re defined across an instance and in relation to an element of the equipment model. They’re related to the process or machine state. Each failure mode has a planning status that classifies how time spent in the failure mode is categorized.

## Industrial Failure Modes benefits

You can define failure mode categories to group and organize failure modes. Grouping and organizing failure modes makes it easier to manage and understand different types of failures across your equipment. These categories are defined across an instance, which provides consistency across your system.

You can define failure modes with categories, making it easier to pinpoint issues related to your equipment. Each failure mode can be associated with an element of the equipment model, helping you to identify exactly where the problem lies.

Each failure mode can be optionally associated with a code or other identifier from the related equipment, which helps to reference and track specific failures.

You can associate each failure mode with a process or machine state \(running, stopping, stopped, or starting\) to understand the context of the failure better. Also, each failure mode can be associated with a planning status \(planned, unplanned, or excluded\), which helps you classify and manage downtime more effectively.

Failure modes are inherited from the parent equipment model level to every level below where they’re initially assigned. This organization helps you verify that all levels of your equipment hierarchy are covered and provides a comprehensive view of potential issues.

You can edit fields directly in the tabular view with inline editing. You only have to select the field and change it as necessary.

## Using Industrial Failure Modes

Failure modes can be used to do the following.

-   Trigger workflows as reactive or corrective measures.
-   Show guidance in recommended actions.
-   Describe features of process or equipment anomalies.
-   Classify time intervals when calculating availability.

The following image shows the **Failure Modes** tab available when viewing part of the equipment model.

![Overview of failure modes for the selected functional location with the highlighted Failure Modes tab](../image/failure-modes.png)

-   **[Create a failure mode from a functional location](../task/create-failure-mode.md)**  
Create a failure mode from a functional location in the Digital Factory Workspace to help identify and organize equipment or process issues.

**Parent Topic:**[Using Digital Factory Workspace](using-digital-factory-workspace.md)

