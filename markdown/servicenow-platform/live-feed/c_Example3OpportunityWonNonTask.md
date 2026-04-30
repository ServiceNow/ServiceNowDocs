---
title: Opportunity won \(non-task\)
description: This example demonstrates a table notification on a non-task table. It generates an automatic message on Live Feed whenever a sales opportunity is won, if you have activated the Sales Force Automation plugin.
locale: en-US
release: yokohama
product: Live Feed
classification: live-feed
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Live Feed table notification examples, Live Feed table notifications, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Opportunity won \(non-task\)

This example demonstrates a table notification on a non-task table. It generates an automatic message on Live Feed whenever a sales opportunity is won, if you have activated the Sales Force Automation plugin.

Create a [business rule](../task/t_SetUpTableNotifNonTaskTables.md) on the Opportunity \[sales\_opportunity\] table that matches the **Live Feed events** business rule on the task table.

Create a table notification with the following values:

-   **Table**: Opportunity \[sales\_opportunity\]
-   **Active**: Select the check box.
-   **Update**: Select the check box.
-   **Post to Live Feed**: Select the check box.
-   **Conditions**: \[State\] \[is\] \[Closed Won\]
-   **Description**: `Opportunity won`
-   **Message**:

    ```
    ${owner} closed a sale with ${account}!
    ```

-   **Before script**:

    ```
    //make the message appear to come from the assigned salesperson if there is one if ( !current. owner. nil ( ) )
    profileSource  = current. owner. getRefRecord ( ) ; //need GlideRecord object
    ```

    ![Example opportunity won message](../image/TableNotificationSales.png "Example opportunity won message")


**Parent Topic:**[Live Feed table notification examples](c_LFTableNotifiExamples.md)

**Related topics**  


[Live Feed table notifications](c_SetUpLiveFeedTableNotifications.md)

