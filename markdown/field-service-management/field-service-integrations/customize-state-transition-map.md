---
title: Customize the work order state transition map
description: Users with the system administrator role can customize the work order state transition map, which maps work order states to project task states.
locale: en-US
release: xanadu
product: Field Service Integrations
classification: field-service-integrations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration with Project Portfolio Management, Integrating Field Service Management with other applications, Configuring Field Service Management, Field Service Management]
---

# Customize the work order state transition map

Users with the system administrator role can customize the work order state transition map, which maps work order states to project task states.

Updating the state of a work order also updates the state of the linked project task. The FieldServicesProjectTaskStateHandler script maps the work order states to the project task states. Users with the system administrator role can customize this state transition map as needed based on the following examples.

## Examples

Setting the status of a work order to **Close complete** should not close the project task. To make this change, remove the following line in the initialize\(\) function:

```
this.workOrderProjectTaskStateMap[FieldServiceProjectTaskStateHandler.WORK_ORDER_STATE_CLOSE_COMPLETE] =
      FieldServiceProjectTaskStateHandler.PROJECT_TASK_STATE_CLOSE_COMPLETE;
    
```

To map the work order **Pending dispatch** state to the project task **Open** state, add the following line to the initialize\(\) function:

```

    this.workOrderProjectTaskStateMap[FieldServiceProjectTaskStateHandler.WORK_ORDER_STATE_PENDING_DISPATCH] = FieldServiceProjectTaskStateHandler.PROJECT_TASK_STATE_OPEN;
    
```

To qualify a task automatically once the project task is changed to **Open**, change the FieldServiceProjectUpdateHandler process function that listens on project task updates and change the linked work order to **Qualified**. Add the following line after this section:

if\(taskJSON.change\_map &amp;&amp; taskJSON.change\_map.state\)\{

```

    If(taskJSON.change_map.state == FieldServiceProjectTaskStateHandler.PROJECT_TASK_STATE_OPEN
    workOrder.state = FieldServiceProjectTaskStateHandler. WORK_ORDER_STATE_PENDING_DISPATCH
    workOrder.update();
    
```

**Parent Topic:**[Integration with Project Portfolio Management](project-management-integration.md)

