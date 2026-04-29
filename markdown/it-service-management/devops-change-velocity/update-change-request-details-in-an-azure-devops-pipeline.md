---
title: Get and update change request details in Azure DevOps pipeline
description: Get and update the change request details associated with an Azure DevOps pipeline.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Get and update change request details in Azure DevOps pipeline

Get and update the change request details associated with an Azure DevOps pipeline.

## Before you begin

Ensure that you meet the following prerequisites before you perform this procedure:

-   Connect, configure the Azure DevOps tool and discover existing repositories, orchestration tasks, and pipelines.
-   Install the following custom extension tasks on your Azure DevOps instance.
    -   ServiceNow extension to integrate Azure Pipelines with DevOps Change Velocity. For more information, see [Use the ServiceNow DevOps extension for Azure DevOps and Azure DevOps custom actions](config-dev-ops-extensions-azure.md#).

Role required:

-   admin or sn\_devops.admin in DevOps Change Velocity
-   admin in Azure DevOps

## About this task

When you update the **state** parameter in a change request, only the following transitions are supported:

-   cancel: Change request state must be **implement** to move the state to **cancel**. **reason** is a mandatory input to update the state to canceled.
-   closed: Change request state must be **implement** or **post implement** to move the state to **close**. **close\_code** and **close\_notes** are mandatory input to update the state to closed.

Specify the change request state as an integer value:

-   4 - Cancel \(Value set in the sn\_devops.change\_request.cancel\_state property\)
-   3 - Closed \(Value set in the sn\_devops.change\_request.closed\_state property\)

When you update a choice field, you must specify a valid choice value that is available in the corresponding choice list. For example, the choice list values for the **Close code** field are successful, successful\_issues, and unsuccessful.

![Choice values for the Close code field](../image/choice-field-update-change.png)

## Procedure

1.  In the Azure DevOps console, navigate to **Organization** &gt; **Pipelines** &gt; **Jobs**.

2.  Select the **Add Tasks** icon \(![Add additional tasks](../image/add-task-ado-sonar.png)\), and search for the ServiceNow extensions in the **Add tasks** search bar.

3.  Add the following extension tasks for get and update functions based on whether you are using a server or agent job.

<table id="table_zkf_vth_cbc"><tbody><tr><td>

Get function

</td><td>

-   ServiceNow DevOps Server Get Change
-   ServiceNow DevOps Agent Get Change


</td></tr><tr><td>

Update function

</td><td>

-   ServiceNow DevOps Server Update Change
-   ServiceNow DevOps Agent Update Change


</td></tr></tbody>
</table>4.  In the task, update the following input parameters based on the function you are using.

<table id="table_ntk_j5h_cbc"><tbody><tr><td>

Get function

</td><td>

-   Project Name
-   Pipeline Name
-   Stage Name
-   Job Name
-   Build ID
-   Attempt Number
-   Branch Name \(only for multi-branch pipeline\)
**Note:** If you do not provide the change request details as input parameters, the change request number associated with the current pipeline and stage will be retrieved.

Enter a reference name for the get change request task, which will be used to reference the change request number in the update task. See the following example.

![ServiceNow DevOps Agent Get Change task](../image/ado-get-change.png)

</td></tr><tr><td>

Update function

</td><td>

-   Change request number whose details need to be updated.
-   Change request attributes to be updated as Key:Value pairs.
```
{ "short_description": "Test description", "priority": "1", "start_date": "2021-02-05 08:00:00", 
"end_date": "2022-04-05 08:00:00", "justification": "test justification", "description": "test description", 
"cab_required": <true/false>, "comments": "This update for work notes is from ADO file", "work_notes": "test work notes", 
"assignment_group": "<SYS_ID>", "state":"<STATE_CODE>", "close_code":"<successful/successful_issues/unsuccessful>", "reason":"<As per Choice List>" }
```

![ServiceNow DevOps Agent Update Change Details](../image/ado-update-change.png)The changeRequestNumber value must be referenced using the get task reference name in the "&lt;task\_name&gt;.&lt;changeRequestNumber&gt;" format. See the following example.

![Get and Update scripts for agent.](../image/ado-script-getupdate-change.png)![Get and Update scripts for server.](../image/azure-get-and-update-script-server.png)**Note:** Attempt number is optional. If not specified, the latest CHG number from the current pipeline execution is retrieved. Otherwise, you can explicitly specify the attempt number without using any environment variables.

</td></tr></tbody>
</table>5.  Save the changes.


**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)

