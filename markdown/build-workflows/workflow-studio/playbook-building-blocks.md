---
title: Understanding the playbook components
description: Understand the building blocks of a playbook and how to configure them when you create a playbook.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Understanding the playbook components

Understand the building blocks of a playbook and how to configure them when you create a playbook.

Each playbook consists of the triggers, stages, and activities. You can use variants to use one playbook for multiple scenarios.

## Triggers

A trigger is an operation that tells your playbook to start a run. Each trigger has a type and conditions that must be met. Triggers only fire for record operations that are interactive or made by users. For more information, see [Triggers](process-automation-designer-triggers.md).

## Stages and activities

An activity represents one step in your business process, and the record for an activity is called an activity definition. Group activities by the stages of your business process, and sequence activities in an order that makes sense for your cross-enterprise workflow. For more information on stages, see [Stages and activities](process-automation-designer-lanes-activities.md).

## Variants

Create different variations on top of a base playbook for multiple use cases instead of duplicating and modifying playbooks, or relying on one-time workarounds that use complex run conditions and branching. For more information about variants, see [Playbook variants](playbook-variants.md).

-   **[Triggers](process-automation-designer-triggers.md)**  
Triggers specify when to start running your playbook.
-   **[Stages and activities](process-automation-designer-lanes-activities.md)**  
In Playbook, an activity represents one step in your overall business process. You can sequence many activities together in the stages of your process.
-   **[Playbook variants](playbook-variants.md)**  
Use one playbook for multiple scenarios.

**Parent Topic:**[Building Playbooks](building-a-process.md)

