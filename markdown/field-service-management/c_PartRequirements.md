---
title: Part requirements
description: After all work order tasks are qualified and the parent work order state automatically changes to Qualified, you can request more information from the qualifier, if necessary, and source any parts required for the tasks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing inventory in Field Service Management, Using Field Service Management, Field Service Management]
---

# Part requirements

After all work order tasks are qualified and the parent work order state automatically changes to **Qualified**, you can request more information from the qualifier, if necessary, and source any parts required for the tasks.

If a work order was created from a [work order template](../../it-services/concept/c_WorkOrderTemplates.md), the part requirements are automatically added to the work order task. Part requirements can be used with any [Service Management application](https://www.servicenow.com/docs/access?context=c_ServiceManagement&version=xanadu&pubname=xanadu-service-management-for-the-enterprise&ft:locale=en-US).

To create part requirements and source parts, enable the **Part requirements are needed by agents** configuration option on the Field Service Configuration screen.

To automatically reserve the required parts in agent stockroom, enable the **Reserve parts in agent stockroom** configuration option on the Field Service Configuration screen.

**Note:** The required parts must be available in the agent personal stockroom or group stockroom to reserve them for a work order task.

-   **[Create a part requirement](../task/t_CreateAPartRequirement.md)**  
Create a part requirement for a work order task.
-   **[Source parts](c_SourceParts.md)**  
Sourcing a part is the process of reserving and obtaining an asset described in a part requirement record by transferring it from one stockroom to another.
-   **[Source a part and assign an agent](../task/t_SourceAPartAndAssignAnAgent.md)**  
The work order sourcing option is useful when you want to assign a work order task to agents who already have the required parts in their stockroom or to a specific agent who needs you to obtain the parts for them.
-   **[Source parts for work order tasks](../../field-service-management/task/source-parts-for-work-order-tasks.md)**  
Source parts from your preferred stockrooms or assignment groups to ensure work order tasks are completed promptly.

**Parent Topic:**[Managing inventory in Field Service Management](../../field-service-management/concept/sourcing-parts.md)

