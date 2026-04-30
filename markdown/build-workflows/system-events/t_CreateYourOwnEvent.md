---
title: Create an event
description: If you do not find a suitable existing event, you can create your own.
locale: en-US
release: zurich
product: System Events
classification: system-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing system events, System Events, Build workflows]
---

# Create an event

If you do not find a suitable existing event, you can create your own.

## Before you begin

Role required: admin

## About this task

The gs.EventQueue function works directly with the backend and therefore business rules that are called by gs.EventQueue\(\) are not invoked.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Events** &gt; **Registry**, and then select **New**.

2.  On the form fill in the fields.

<table id="table_hbv_pg3_j1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event name

</td><td>

Name of your new event.

</td></tr><tr><td>

Table

</td><td>

Database table for this event. **Note:** Only tables and database views that are in the same scope as the event appear on the listing.

</td></tr><tr><td>

Queue

</td><td>

Name of the queue that the event is placed into when triggered.Use only lowercase letters, no spaces, and no special characters except underscore \(\_\). For example, `my_queue`. See [Using custom queues to process events](https://www.servicenow.com/docs/access?context=useful-server-side-scripts&version=zurich&pubname=zurich-api-reference&section=queues-create&ft:locale=en-US).

</td></tr><tr><td>

Priority

</td><td>

Order in which messages will be processed. Lower values have higher priority.**Note:** The com.glide.sysevent.priority.enabled system property is enabled by default. If you disable it, events processing is not done by priority.

</td></tr><tr><td>

Caller Access

</td><td>

Restricted caller access settings.-   Caller Restriction: calls to the resource must be manually approved.
-   Caller Tracking: Calls to the resource are automatically approved.


</td></tr><tr><td>

Fired by

</td><td>

Name of the business rule that runs the event. This field is for reference only and is not used by any process. Make sure that there is enough information to locate your event again.

</td></tr><tr><td>

Description

</td><td>

Short description of the purpose of the event.

</td></tr></tbody>
</table>3.  Click the **Business Rules** related link.

4.  If you are creating an event for a base system table, select the existing event business rule for the table.

    For example, select the **sc request events** business rule to create a custom Request event.

5.  If you are updating an existing event business rule, add a new condition to the **Script**.

    The following sample script adds a **request.commented** event with the user's Sys ID as parm1 and the user's user name for parm2.

    ```
    if (current.operation() != 'insert' && current.comments.changes()) {
    gs.eventQueue('request.commented', current, gs.getUserID(), gs.getUserName());
    }
    ```

6.  If you are creating an event for a custom table, create a new business rule that runs after database operations.

    For example, this business rule defines several events for a custom application called Marketing Events.

<table id="table_st1_hzs_wy"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Attendee Events

</td></tr><tr><td>

Table

</td><td>

Attendee \[x\_snc\_marketing\_ev\_attendee\]

</td></tr><tr><td>

Application

</td><td>

Marketing Events

</td></tr><tr><td>

Advanced

</td><td>

Selected

</td></tr><tr><td>

When

</td><td>

after

</td></tr><tr><td>

Insert

</td><td>

Selected

</td></tr><tr><td>

Update

</td><td>

Selected

</td></tr><tr><td>

Delete

</td><td>

Selected

</td></tr><tr><td>

Script

</td><td>

Add custom script that:

-   Checks for one or more conditions on the current record.
-   Calls the gs.eventQueue\(\) method and specifies an event name.
 See code sample.

</td></tr></tbody>
</table>    **Note:** If you add **Filter Conditions**, **Role conditions**, or a **Condition** value, verify it runs the business rule when expected.

    ```
    (function executeRule(current, previous /*null when async*/) {
       //This function will be automatically called when this rule is processed.
            //Add event when attendee inserted
            if(current.operation() == 'insert' && current.marketing_event.changes()) {
                    gs.eventQueue('x_snc_marketing_ev.attendee.added', current,
    current.marketing_event, current.email);
            }
            //Add event when marketing event changes
            if(current.operation() == 'update' && current.marketing_event.changes()) {
                    gs.eventQueue('x_snc_marketing_ev.attendee.deleted', previous,
    previous.marketing_event, previous.email);
                    gs.eventQueue('x_snc_marketing_ev.attendee.added', current,
    current.marketing_event, current.email);
            }
            //Add event when attendee deleted
            if(current.operation() == 'delete') {
                    gs.eventQueue('x_snc_marketing_ev.attendee.deleted', current,
                  current.marketing_event, current.email);
    }
    })(current, previous);
    ```

7.  Register the event.


## What to do next

Create a script action or notification to process the event.

**Related topics**  


[Register an event](t_RegisterAnEvent.md)

[Script actions](../reference/r_ScriptActions.md)

