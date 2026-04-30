---
title: Associate activity groups and activity types to activity contexts
description: Add the activity groups and activity types you created to an activity context, depending on who you want to display the information for.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure the Customer Activity view, Configure Customer Central, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Associate activity groups and activity types to activity contexts

Add the activity groups and activity types you created to an activity context, depending on who you want to display the information for.

Associate an activity group to an activity context

Learn more about associating an activity group to an activity context from the following video tutorial.

Associate an activity type to an activity context

Learn more about associating an activity type to an activity context from the following video tutorial.

## Before you begin

Role required: admin

## About this task

An activity context is the person or user who is interacting with the customer service agent. There are two predefined activity contexts: consumer and contact. Add the activity groups and activity types you created to the activity context, depending on who you want to display the information for.

## Procedure

1.  Navigate to **All** &gt; **Customer Central** &gt; **Customer Activity** &gt; **Activity Contexts**.

2.  Open the contact or consumer record that you want to add your configuration to.

3.  On the Activity Context Groups related list, select **New**.

4.  Add the activity group.

5.  On the Activity Context Types related list, select **New**.

6.  Fill out the fields, as required.

    |Field|Description|
    |-----|-----------|
    |Activity type|Add the activity type.|
    |Fetch from activities|Deselect Fetch from Activities if a business rule is not defined for this activity type.|
    |Filter conditions|Add filter criteria to apply filter conditions on the source table.|
    |Source mapping field|Select the field in the Source table that is related to the context.|
    |Context mapping field|Select the field in the Context table to map to the field selected in **Source mapping** field.|
    |Advanced mapping|Select Advanced Mapping and write a script in the **Advanced mapping script** field if the source and context mapping is not sufficient.|

7.  Select **Submit**.


