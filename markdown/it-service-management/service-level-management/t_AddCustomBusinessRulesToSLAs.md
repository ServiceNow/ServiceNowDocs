---
title: Add custom business rules to Service Level Agreement \(SLA\)
description: You can add custom business rules to your SLAs.
locale: en-US
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Service Level Management, IT Service Management]
---

# Add custom business rules to Service Level Agreement \(SLA\)

You can add custom business rules to your SLAs.

## Before you begin

Role required: admin

## Procedure

1.  Select one of the following methods to add custom business rules.

<table id="choicetable_rhy_4yf_4v"><tbody><tr><td id="d232479e63">

**Use setWorkflow\(false\)**

</td><td>

Prior to updating your task, add a call to `setWorkflow(false)` on the GlideRecord object for the task within the business rule that is updating the task. This prevents the business rules from being processed.**Note:** The setWorkflow\(false\) disables processing of all engines and the update does not appear in the audit history of the task.

 For example, a script that copies the breach time to a custom field on the task.

```
(function(){ 
            if (current.planned_end_time.changes()) { 
               var taskGr = current.task.getRefRecord(); 
               taskGr.u_sla_breach_time = current.planned_end_time; 
               taskGr.setWorkflow(false); 
               taskGr.update(); 
            } )
          ();
```

</td></tr><tr><td id="d232479e83">

**Create a sys\_trigger \(Schedule job\) to update the task**

</td><td>

In your custom business rule, use the **Script** field to generate a scheduled job to update the task. To ensure that the scheduled job is queued for processing immediately, it must be of type Run once, and have next action time of Now.**Note:** The `ScheduleOnce` script include includes functions to specify the target record and when to run the scheduled job. This enables you to specify the script to be executed and call another function to create the appropriate record in the `sys_trigger` table.

 For example, a script to create a scheduled job that copies the breach time from the task SLA to a custom field on the task.

```
(function(){
            if (current.planned_end_time.changes()) { 
               var scheduleJob = new ScheduleOnce(); 
               scheduleJob.setDocument(t.task.getRefRecord()); 
               scheduleJob.script = 
                   "current.u_sla_breach_time.setValue('" + 
                   current.getValue('planned_end_time') + 
                   "');current.update();"; 
               scheduleJob.schedule(); 
            } 
          )();
```

</td></tr></tbody>
</table>
**Parent Topic:**[Using Service Level Management](../concept/using-service-level-management.md)

