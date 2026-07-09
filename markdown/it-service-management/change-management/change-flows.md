---
title: Change flows
description: The Change Management Change flows provide a library of reusable actions and end-to-end implementations of the Change models provided in the base system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/change-management/change-flows.html
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Workflow Editor, Workflow, Flow]
breadcrumb: [Reference, Change Management, IT Service Management]
---

# Change flows

The Change Management Change flows provide a library of reusable actions and end-to-end implementations of the Change models provided in the base system.

Starting with the Yokohama release, the new base system flows replace the existing workflows for Change Management. However, you can continue to create custom workflows or use the existing ones. To migrate your existing workflows to flows, check the new base system flows available in Workflow Studio for guidance. For any new requirements, use flows.

You can use ServiceNow® Workflow Studio to create, operate, and troubleshoot flows. Workflow Studio is a single interface that provides:

-   Natural language descriptions.
-   Runtime information.
-   Consolidated configuration.

You can deactivate an out-of-box change flow directly after you copy it, without logging a support case. To activate the change flows in the base system, contact Support to request activation. For more information on the plugin activation, see

.

By default, these Change flows are provided:

|Flow|Description|
|----|-----------|
|Change - Cloud Infrastructure - Authorize|Process cloud infrastructure changes for approvals.|
|Change - Emergency - Authorize|Process an emergency change that is in authorize state and is not on hold.|
|Change - Emergency - Implement|Process an emergency change that is in the implement state.|
|Change - Emergency - Review|Process an emergency change in the review state.|
|Change - Normal - Assess|Process a normal change that is in the assess state and is not on hold.|
|Change - Normal - Authorize|Process a normal change that is in the authorize state and is not on hold.|
|Change - Normal - Implement|Process a normal change that is in the implement state.|
|Change - Standard|Process a standard change.|
|Change - Standard - Implement|Process a standard change that is in the implement state.|
|Change - Standard - Proposal|Propose a new standard change template. Handles approvals from draft to published state.|
|Change - Unauthorized - Authorize|Process an unauthorized change for approvals.|
|Change - Unauthorized - Review|Review an unauthorized change.|

-   **[Change Management Workflow Studio actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/change-flow-actions.md)**  
Use Workflow Studio actions as building blocks to handle the Change models and types. The flow actions are available under the ITSM spoke in Workflow Studio.

**Parent Topic:**[Reference section for Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/reference-change-management.md)

