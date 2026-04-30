---
title: Change flows
description: The Change Management Change flows provide a library of reusable actions and end-to-end implementations of the Change models provided in the base system.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference section for Change Management, Change Management, IT Service Management]
---

# Change flows

The Change Management Change flows provide a library of reusable actions and end-to-end implementations of the Change models provided in the base system.

You can use ServiceNow® Workflow Studio to create, operate, and troubleshoot flows. Workflow Studio is a single interface that provides:

-   Natural language descriptions.
-   Runtime information.
-   Consolidated configuration.

The provided flows are read-only to ensure that they can be upgraded. To change the behaviour of these flows, make a copy of the read-only flow, and contact Support to deactivate the read-only flow. Deactivating the read-only flow ensures that the copied flow is the only version that is triggered.

If you need to activate the change flows in the base system, you must contact the support to log a case to activate the change flows.

By default, these Change flows are provided:

|Flow|Description|
|----|-----------|
|Change - Cloud Infrastructure - Authorize|Process cloud infrastructure changes for approvals.|
|Change - Emergency - Authorize|Process an emergency change that is in authorize state and is not on hold.|
|Change - Emergency - Implement|Process an emergency change that is in the implement state.|
|Change - Emergency - Review|Process an emergency change in the review state.|
|Change - Implementation tasks|Process to create implementation and post implementation change tasks for change request and wait until completion.|
|Change - Normal - Assess|Process a normal change that is in the assess state and is not on hold.|
|Change - Normal - Authorize|Process a normal change that is in the authorize state and is not on hold.|
|Change - Normal - Implement|Process a normal change that is in the implement state.|
|Change - Standard|Process a standard change.|
|Change - Standard - Implement|Process a standard change that is in the implement state.|
|Change - Unauthorized - Authorize|Process an unauthorized change for approvals.|

-   **[Change Management Workflow Studio actions](change-flow-actions.md)**  
Use Workflow Studio actions as building blocks to handle the Change models and types. The flow actions are available under the ITSM spoke in Workflow Studio.

**Parent Topic:**[Reference section for Change Management](reference-change-management.md)

