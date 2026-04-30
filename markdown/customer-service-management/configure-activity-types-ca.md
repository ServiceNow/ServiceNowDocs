---
title: Configure activity types for the Customer History view
description: Create an activity type to display in the activity feed on the Customer History view.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-02-04"
reading_time_minutes: 2
breadcrumb: [Configure the Customer History view, Configure Customer Central, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure activity types for the Customer History view

Create an activity type to display in the activity feed on the Customer History view.

## Before you begin

Role required: admin

**Note:** Customer Activity has been renamed to Customer History, with no changes to its functionality. References to the previous name will be updated in a future release.

## About this task

An activity type is an action that a contact or consumer performs. These actions are displayed in the activity feed on the Customer History view.

Activity types are displayed in the Customer History view in Agent Workspace.

![Agent Workspace displaying activity types in Customer Activity view. In this example, cases are highlighted on the Customer Activity tab.](../image/activity-type.png)

## Procedure

1.  Navigate to **All** &gt; **Customer Central** &gt; **Customer Activity** &gt; **Guided Setup**.

2.  Select **Get Started** under Activity Feed.

3.  Select **Configure** beside Activity Types.

4.  Select **New**.

5.  Fill out the fields, as required.

<table id="table_vzg_jcs_mlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Enter a name for the activity.

</td></tr><tr><td>

Activity message

</td><td>

Enter the message that is displayed on the activity tile in the activity feed.**Note:** If the message is not yet defined, you can create a message. Refer to the video above on how to create a message.

</td></tr><tr><td>

Activity source

</td><td>

Enter the table on which the activity is performed. For example, if creating a case is the activity, the Case table is the Activity Source.

</td></tr><tr><td>

Actor

</td><td>

Enter the person performing the activity.

</td></tr><tr><td>

Object

</td><td>

Select an Object, which is the unique key that identifies the object on which the activity is performed.

</td></tr><tr><td>

Filter conditions

</td><td>

Specify any condition that must be met for the activity to be displayed in the activity feed.

</td></tr><tr><td>

Active

</td><td>

Deselect the **Active** check box to not display the activities corresponding to this type in the activity feed.

**Note:** If you deselect this check box, deselect the corresponding facet. If not, the facet displays with no data.

</td></tr><tr><td>

Verb

</td><td>

Select a verb that describes the activity performed.**Note:** If the verb is not yet defined, you can create a verb. Refer to the video above on how to create a verb.

</td></tr><tr><td>

Target

</td><td>

Select the second person involved in the activity. Not all activities have a second person.

</td></tr></tbody>
</table>6.  Select **Submit**.

    **Note:** Once you create a new activity type, a new business rule is created.

7.  After submitting, you can configure the business rule in one of two ways:

    -   Select the link to the business rule in the notification message.
    -   Go to the Activity Feed page and select **Configure** beside the Business Rule section.
    **Note:** Configuring the business rule is optional. The business rule is required to create a record in a central activity table each time the action is performed. The central activity table improves the performance of rendering the feed during runtime. Create a business rule for each activity type.

8.  In the Advanced tab, update the script.

    The following is an example script.

    ```
    var actSubCtx = global.ActivitySubscriptionContext.getContext();
    if (current.contact) {
        actSubCtx.getActivityService().createActivity(current, verb, "", "", "", module);
    }
    current: current variable in business rules holds the GlideRecord of the table on which the business rules is triggered. If this business rule is on Case table, current will hold the GlideRecord of the case. 
    verb: verb that is configured in the Verb field of the created activity type
    module: module that is configured in the Module field of the created activity type
    Note: If there is already a Create Activity business rule, a notification message will also be displayed. You can update the script as required.
    ```


