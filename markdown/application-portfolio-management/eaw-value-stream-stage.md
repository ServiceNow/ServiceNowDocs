---
title: Manage value stream stages
description: Value stream stages are a specific section within the overall value stream, encompassing a specific set of activities.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Working with business architecture, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Manage value stream stages

Value stream stages are a specific section within the overall value stream, encompassing a specific set of activities.

A value stream is made up of multiple value stream stages. The stages are organized in a sequence, ensuring that each stage add value to the overall value stream.

The following relationships define the value stream stage model in Enterprise Architecture:

-   Value stream to value stream stages: A value stream contains one or more value stream stages. Each stage represents a step in the end-to-end value delivery sequence and is assigned a numeric order that determines its position within the value stream.
-   Value stream stage to business processes \(many-to-many\): A value stream stage can be associated with one or more business processes. A business process can also be associated with multiple value stream stages across different value streams. This association helps you understand which workflows support each step of value delivery.
-   Value stream stage to business capabilities \(many-to-many\): A value stream stage can be associated with one or more business capabilities. A business capability can also support multiple value stream stages. This association helps you understand which organizational capabilities are required to deliver each stage.

In the Hire to Retire value stream, onboarding of new employees is a value stream stage.

-   **[View value stream stage details](../../task/eaw-task/eaw-view-all-value-stream-stages.md)**  
You can view the list of all available value streams stages in the Enterprise Architecture Workspace.
-   **[Add or edit a value stream stage](../../task/eaw-task/eaw-add-or-edit-a-value-stream-stage.md)**  
Create or edit a value stream stage to improve the efficiency of a value stream and verify each step adds value to the output of the value stream.
-   **[Add or remove a business process from a value stream stage](../../task/eaw-task/eaw-assoc-bp-with-vs-stage.md)**  
You can add an existing business process to a value stream stage to map your enterprise architecture workflows to the stages of your value streams. You can also remove associated business processes if they are no longer relevant for the value stream stage.
-   **[Add or remove a business capability from a value stream stage](../../task/eaw-task/add-or-remove-a-bc-from-vs-stage.md)**  
You can add an existing business capability to a value stream stage to map your organizational capabilities to the stages of your value streams. You can also remove associated business capability if they’re no longer relevant for the value stream stage.

**Parent Topic:**[Working with business architecture](eaw-business-architecture.md)

**Related topics**  


[View value stream stage details](../../task/eaw-task/eaw-view-all-value-stream-stages.md)

[Add or edit a value stream stage](../../task/eaw-task/eaw-add-or-edit-a-value-stream-stage.md)

