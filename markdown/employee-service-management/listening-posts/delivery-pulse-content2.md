---
title: Delivering pulse surveys in Listening Posts
description: Deliver pulse surveys to employees from various applications such as Listening Posts, Content Automation, and Content Delivery.After you create content of type Pulse Content in Content Automation, use campaigns to create pulse instances.
locale: en-US
release: xanadu
product: Listening Posts
classification: listening-posts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Creating and delivering pulse surveys, Listening Posts, HR Service Delivery, Employee Service Management]
---

# Delivering pulse surveys in Listening Posts

Deliver pulse surveys to employees from various applications such as Listening Posts, Content Automation, and Content Delivery.

-   **Listening posts**

    After you create pulse surveys in the Listening Posts application and define the required pulse surveys fields such as **Start date** and **End date**, the Listening Posts: Create Group Pulse Instance schedule job performs the following tasks:

    -   selects all the pulse surveys that are in published state and creates survey instances. If the end date of a survey has passed, the survey is automatically moved to closed state.
    -   selects all the pulse surveys that are in ready state. If the start date of a pulse survey has passed, the scheduled job creates instances for that pulse survey. If the end date of a pulse survey has passed, the schedule job changes the state of the pulse survey to closed.
-   **Content Automation**

    After you create content of type **Pulse Content** in Content Automation, use campaigns to create pulse instances. For more information, see [Deliver pulse content using campaigns](delivery-pulse-content2.md#).

-   **Content Delivery**

    After you create content of type **Pulse Content** in Content Delivery, use schedule content to create pulse instances. For information on how to create a schedule content, see [Schedule the delivery for content](../../employee-center/concept/ec-content-publishing-schedule.md).

    The Listening Posts: Create Group Pulse Instance schedule job considers the availability state date of the schedule content and creates instances for published surveys.


**Parent Topic:**[Creating and delivering pulse surveys](create-deliver-surveys.md)

**Related topics**  


[Create a pulse question in Listening Posts](../task/create-pulseq.md)

[Create a pulse theme in Listening Posts](../task/create-pulse-theme.md)

[Create a pulse survey in Listening Posts](../task/create-pulse-survey.md)

[Create a pulse survey as content in Listening Posts](../task/create-survey-content.md)

## Deliver pulse content using campaigns

After you create content of type **Pulse Content** in Content Automation, use campaigns to create pulse instances.

### Before you begin

Role required: sn\_ca.campaign\_manager

### Procedure

1.  [Create a campaign](../../employee-center/task/ecpro-manage-campaigns.md).

2.  Create a campaign bundle of a trigger type **Fixed Date** or **To dos completion**.

    For more information, see [Create a campaign bundle](../../employee-center/task/ecpro-manage-campaign-bundles.md)

3.  Create content of type **Pulse Content**.

    For more information, see [Create a pulse survey as content in Listening Posts](../task/create-survey-content.md).

4.  Add the Content Type **Pulse Content** to the campaign bundle.

5.  After completing all the parts of a campaign, click the **Publish** button.

    The schedule job **Content Automation: Create LP Pulse survey** creates pulse surveys for campaigns that are in Published state with Content Type **Pulse Content**. The scheduled job verifies if the **Re-evaluate campaign** check box is enabled. Depending on the reevaluation frequency, the scheduled job creates or cancels pulse survey instances for the users who are added or removed from the campaign.


