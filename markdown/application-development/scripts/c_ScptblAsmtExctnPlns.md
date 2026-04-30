---
title: Scriptable assignment of execution plans
description: Each catalog item has an associated execution plan, used whenever an item of that type is ordered; if no plan is specified, the default plan is used. This default is effective for most organizations, but your execution plan may need to vary based on additional criteria.Execution plan scripts have limitations that need to be considered during their implementation.Follow these guidelines when writing execution plan scripts.You can add a script to a catalog item so that the script runs each time a user requests that item.You can use an approval rule script to approve an execution plan.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Scriptable assignment of execution plans

Each catalog item has an associated execution plan, used whenever an item of that type is ordered; if no plan is specified, the default plan is used. This default is effective for most organizations, but your execution plan may need to vary based on additional criteria.

For example, in the base system service catalog, a request for a new PC always uses the PC Delivery Plan. However, this plan may need to vary for unusual circumstances - such as when a requester is working from home, at a remote location.

To provide this flexibility, you can use a script to override the default execution plan on a specific catalog item.

**Parent Topic:**[Server-side scripting](c_ServerScripting.md)

## Limitations during script execution

Execution plan scripts have limitations that need to be considered during their implementation.

While the execution plan script runs:

-   You cannot interact with any catalog tasks as catalog tasks are only created after the execution plan is selected.
-   Some fields such as **total delivery time** and **due date** are not yet calculated, although the request itself is available within the script via current.request\(\).
-   Approvals have not yet been generated.

## Writing the scripts

Follow these guidelines when writing execution plan scripts.

Execution plan scripts can access the same global variables and other functions as in any other server side execution plan.

-   current is the currently-requested catalog item, `sc_req_item`.
-   current.delivery\_plan\(\) is the assigned execution plan for this catalog item.

The evaluated value from the script is used as the `sys_id` of the execution plan.

Simple example:

```
current.delivery_plan.setDisplayValue('PC Delivery Plan')
```

If an invalid value is returned, such as undefined or not found, then the existing assigned value is used.

More complex example:

```
getexecutionplan();
function getexecutionplan() {
var location = current.request.requested_for.location.getDisplayValue();
// if we're in Atlanta
if (location == 'Atlanta') {
   // use the remote pc delivery plan instead of the normal one
   var remote_plan = new GlideRecord('sc_cat_item_delivery_plan');
   remote_plan.addQuery('name', 'Remote PC Delivery Plan');
   remote_plan.query();
   remote_plan.next();
   current.delivery_plan = remote_plan.sys_id;
   return remote_plan_sys_id;
   } 
   return current_delivery_plan;
}
```

In this example, any time a request is for a user in Atlanta, ServiceNow uses the Remote PC Delivery Plan. Otherwise, the execution plan is not overridden and ServiceNow uses the catalog item's normal execution plan, the PC Delivery Plan.

## Add a script to a catalog item

You can add a script to a catalog item so that the script runs each time a user requests that item.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Maintain Items**.

2.  Select the relevant catalog item to which you wish to add the script.

3.  Configure the catalog item form to add the execution plan script field, often named **Delivery Plan Script**.

4.  Fill in the script details.

    ![Delivery plan script](../image/DeliveryPlanScript.png)

5.  Update the item form with your changes.


### Result

The script runs each time that item is requested, selecting the execution plan to run with that item.

## Use a script to approve an execution plan

You can use an approval rule script to approve an execution plan.

### Procedure

1.  Retrieve an approval execution plan task.

2.  View the **Approval Script** field.

3.  Fill in an approval script using the same syntax and rules you would use on an approval rule.


### Example

For example, in the script below, the requester’s manager is the approver.

![Execution plan approval script](../image/ApproveExecPlan.png "Script specifying the approver")

