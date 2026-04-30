---
title: Create a new case form
description: The Create a new case form allows you to create a new case in Agent Workspace for HR Case Management.
locale: en-US
release: yokohama
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent Workspace for HR Case Management reference, Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# Create a new case form

The Create a new case form allows you to create a new case in Agent Workspace for HR Case Management.

<table id="table_abc_p2z_bbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

COE

</td><td>

Select the **Center of Excellence** associated with the HR case you are creating. Selecting a COE filters the choices for HR service. For more information, see [HR Centers of Excellence data model](../concept/hr-centers-of-excellence-coes.md).**Note:** You can also select an HR service first and the associated COE automatically populates.

</td></tr><tr><td>

HR Service

</td><td>

The HR service based on the COE selected or what you select based on communication with the employee request. What HR services are available to an employee filter by:-   COE selected.
-   HR criteria for the **Subject person** based on the HR service configuration.

Limit services filter on the **Case Creation Configuration** form. If the HR service field is empty, ensure that you did not remove the Opened for field.


</td></tr><tr><td>

HR service description

</td><td>

Description of the HR service selected in the **HR Service** field.For more information on configuring the HR service description, see [Configure an HR service](../task/configure-hr-service.md).

</td></tr><tr><td>

Opened for

</td><td>

The employee who the case is created for. This person can be different than the subject person. For example, it could be the subject person's manager.

</td></tr><tr><td>

Subject person

</td><td>

The recipient/beneficiary of the HR service fulfilled through the HR Case.**Note:** Advanced reference qualifiers on a reference field is not supported in the case creation configuration page. When the limit user search filter is applied to the employee search, it will not be applied to **Opened for** and **Subject person**.

</td></tr><tr><td>

Work notes

</td><td>

Information related to the case that can help other HR agents. Work notes are not visible to the Opened for person.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Workspace for HR Case Management reference](agent-ws-reference.md)

**Related topics**  


[Page Configurations reference](configuration-settings.md)

[Highlighted value condition form](highlighted-value-form.md)

[Bulk case request form](bulk-case-request-form.md)

