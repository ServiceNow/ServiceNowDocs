---
title: Part requirements
description: After all work order tasks are qualified and the parent work order state automatically changes to Qualified, you can request more information from the qualifier, if necessary, and source any parts required for the tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/field-service-management/work-order-management/c\_PartRequirements.html
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage inventory in Field Service Management, Manage work order tasks, Prepare work orders, Using Field Service Management, Field Service Management]
---

# Part requirements

After all work order tasks are qualified and the parent work order state automatically changes to **Qualified**, you can request more information from the qualifier, if necessary, and source any parts required for the tasks.

If a work order was created from a [work order template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/c_WorkOrderTemplates.md), the part requirements are automatically added to the work order task. Part requirements can be used with any [Service Management application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/service-management-for-the-enterprise/service-management-legacy/c_ServiceManagement.md).

To create part requirements and source parts, enable the **Part requirements are needed by agents** configuration option on the Field Service Configuration screen.

To automatically reserve the required parts in agent stockroom, enable the **Reserve parts in agent stockroom** configuration option on the Field Service Configuration screen.

**Note:** The required parts must be available in the agent personal stockroom or group stockroom to reserve them for a work order task.

-   **[Create a part requirement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/t_CreateAPartRequirement.md)**  
Create a part requirement for a work order task.
-   **[Source parts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/c_SourceParts.md)**  
Sourcing a part is the process of reserving and obtaining an asset described in a part requirement record by transferring it from one stockroom to another.
-   **[Source a part and assign an agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/t_SourceAPartAndAssignAnAgent.md)**  
The work order sourcing option is useful when you want to assign a work order task to agents who already have the required parts in their stockroom or to a specific agent who needs you to obtain the parts for them.
-   **[Source parts for work order tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/source-parts-for-work-order-tasks.md)**  
Source parts from your preferred stockrooms or assignment groups to ensure work order tasks are completed promptly.

**Parent Topic:**[Manage inventory in Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/work-order-management/sourcing-parts.md)

