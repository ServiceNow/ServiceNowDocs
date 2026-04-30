---
title: Associate a record with an interaction
description: As an agent, you might need to create a record on another table to work on an interaction. You can associate the record with the interaction.
locale: en-US
release: zurich
product: Interaction Management
classification: interaction-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Interaction Management, Interaction Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Associate a record with an interaction

As an agent, you might need to create a record on another table to work on an interaction. You can associate the record with the interaction.

## Before you begin

Role required: interaction\_agent

**Note:** You must also have the roles required to access the records that you want to associate with the interaction.

## Procedure

1.  Navigate to **All** &gt; **Interaction** &gt; **Assigned to me**.

2.  Open the interaction you want to associate with another record.

3.  Select **Associate Record**.

    ![Interaction with Associate record button highlighted.](../image/associate-record.png)

4.  In the Interaction Related Record form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Document table|Select the table where the association is saved.|
    |Record Type|Select the type of record that you are associating with the interaction. Record type can be **Task** or **Knowledge**.|
    |Task|Select the task you want to associate with the incident. Task field becomes available when the record type is selected as Task.|
    |Knowledge article|Select the knowledge article you want to associate with the incident. Knowledge article field becomes available when the record type is selected as Knowledge.|
    |ID of related record|Automatically updated with the task or knowledge number.|

5.  Save the form.

    ![Interaction related record form.](../image/interaction-related-record.png)


## Result

Task type records associated will appear in the Related Tasks related list for the interaction.

![Associated tasks are available under Related Tasks.](../image/associated-interaction.png)

**Parent Topic:**[Using Interaction Management](../concept/using-interaction-management.md)

