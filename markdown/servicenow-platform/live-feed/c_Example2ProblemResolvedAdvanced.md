---
title: Problem resolved \(advanced\)
description: This advanced example demonstrates a table notification that generates an automatic message on Live Feed whenever a problem is closed.
locale: en-US
release: zurich
product: Live Feed
classification: live-feed
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Live Feed table notification examples, Live Feed table notifications, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Problem resolved \(advanced\)

This advanced example demonstrates a table notification that generates an automatic message on Live Feed whenever a problem is closed.

It also adds a message about the assigned user and posts the message from the assignment group profile instead of the problem record.

-   **Table**: Problem \[problem\]
-   **Active**: Select the check box.
-   **Update**: Select the check box.
-   **Post to Live Feed**: Select the check box.
-   **Conditions**: \[Problem State\] \[is\] \[Closed/Resolved\]
-   **Description**: `Problem Resolved`
-   **Message**:

    ```
    Problem ${number} - ${short_description} has been resolved. ${fixedByMsg}
    ```

-   **Before script**:

    ```
    //cancel if we didn't just change the problem state if ( !changedFields. contains ( "problem_state" ) )
    answer  = false ;
     
     //if we have an assigned_to value add a comment about who it was //create a new variable fixedByMsg that we can access from the message
    fixedByMsg  = "" ; if ( !current. assigned_to. nil ( ) )
    fixedByMsg  = " Thank you " + current. assigned_to. getDisplayValue ( ) ;
     
     //make the message appear to come from the assignment group if we have one if ( !current. assignment_group. nil ( ) )
    profileSource  = current. assignment_group. getRefRecord ( ) ; //need GlideRecord object
    ```


**Parent Topic:**[Live Feed table notification examples](c_LFTableNotifiExamples.md)

**Related topics**  


[Live Feed table notifications](c_SetUpLiveFeedTableNotifications.md)

