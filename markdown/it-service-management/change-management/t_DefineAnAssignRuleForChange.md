---
title: Create a change request assignment rule
description: You can define assignment rules to automate the process of assigning change requests to the appropriate group or individual.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Create a change request assignment rule

You can define assignment rules to automate the process of assigning change requests to the appropriate group or individual.

## Before you begin

Role required: admin

## About this task

You can define an assignment rule either for the change request or for the change tasks that are generated for change requests. In the following example, you create an assignment rule to assign change requests for configuration items in the database class to the **Database** group.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Assignment**, and then click **New**.

2.  Enter the name: `Database Change`.

3.  In the Applies To form section, select the table **Change Request \[change\_request\]** and add a condition **\[Configuration Item.Class\] \[is\] \[Database\]**.

4.  In the Assign To section, select the group **Database**.

5.  Click **Submit**.


## What to do next

To test the assignment rule, navigate to **Change** &gt; **Create New** and enter a Normal change. Complete the form, selecting **bond\_trade\_ny**, or another CI in the database class, in the **Configuration Item** field.

Save the change and see that it was automatically assigned to the **Database** group.

**Parent Topic:**[Configuring Change Management](../concept/configure-change-management.md)

