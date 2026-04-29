---
title: Configure a sequence to fulfill items in order guides
description: Configure a sequence in Playbooks to fulfill items in order guides. Once you define a sequence, you don't have to manually check whether required items have been fulfilled before fulfilling their dependent items.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create an order guide, Order guides, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a sequence to fulfill items in order guides

Configure a sequence in Playbooks to fulfill items in order guides. Once you define a sequence, you don't have to manually check whether required items have been fulfilled before fulfilling their dependent items.

## Before you begin

The Order Guide Sequential Fulfillment \(com.glideapp.servicecatalog.order\_guide\_sequencing\) plugin must be installed. Navigate to **System Plugin** and search for this plugin. The plugin form allows you to activate or repair the plugin.

The order guide must contain at least one item in the rule base.

Role required: admin or both catalog\_admin and playbook.admin

## About this task

A sequence can be defined for an order guide so that all the items in the order guide do not move to the in-progress state immediately after order guide fulfillment is started. You can configure when an item must be fulfilled. The requested items will remain in the pending state until the time order guide fulfillment reaches the point where the requested item must be fulfilled. Any record generated through record producers will only be generated when order guide fulfillment reaches the point where the record is processed.

Sequence generated for order guides with only record producers as rule base items will not be considered.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Order Guides**.

2.  Select the order guide for which you want to create a sequence in which the items must be fulfilled.

3.  On the form, select the **Generate sequence** button in the top-right corner.

4.  Enter a name for the sequencing process in the **Process name** field.

5.  Select **Generate**.

    The Playbooks page is displayed on a new tab and items are added to **Lane 1** according to their sequence in the rule base.

    You can change the default name of the first lane, Lane 1, by selecting **Lane actions &gt; Configure lane** and modifying the name.

    ![Process Automation Designer page for sequencing](../image/SequencePad.png)

6.  In the lane, select an activity card for the item you want to configure.

7.  Configure the activity's properties.

    |Field|Description|
    |-----|-----------|
    |Label|Name of the rule base in the sequence.|
    |Description|Description of the activity.|
    |When to start|Determines whether the activity must be run immediately, with the previous activity, or after the previous activity.|
    |Order Guide Item|Item in the order guide for which the activity must be run.|
    |End the activity without waiting for the completion of task record|Option to end the activity before completion of the task record. For example, you can select this option for an incident activity when you want to end the activity before the incident is closed so that the next activity can be started.|

8.  Add a condition for an activity that is configured to run after the previous activity by selecting **Add Condition**.

    The outputs \(Generated Task Record, Record Id, Table\) of the previous activity are available as options on which you can apply a condition. The Generated Task Record output is only available for catalog items and record producers whose target table is an extension of the Task table.

9.  View the configured properties of the activity by selecting **View all properties**.

10. Add new items to the lane by selecting **Add another process activity** and then select an activity in the **Add activity** dialog box.

    If an order guide contains more than 20 rule base items, only the first 20 items are added to the first lane. You can manually add the remaining ones to the sequence by selecting the **Fulfill Order Guide** activity in the **Add activity** dialog box. Items added via order guide script also needs to be added manually.

11. Select **Save and close**.

    **Note:** If the same activity is added multiple times in a sequencing process, the activity runs only once when it occurs for the first time in the sequence.

12. Create a lane to group similar catalog items by selecting **Add another lane**.

13. Change the sequence of the activities by dragging the activity cards within or between the lanes.

14. Determine when the lane will run by selecting an option from the **When to start** drop-down menu.

15. View the properties of the configured sequence by selecting the **Properties** button in the top-right corner.

16. Publish the sequencing process by selecting **Activate**.

    Watch this six-minute video to understand how to configure a sequence to fulfill items in order guides.Configure a sequence to fulfill items in order guides


**Parent Topic:**[Create an order guide](t_CreateAnOrderGuide.md)

**Related topics**  


[Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

