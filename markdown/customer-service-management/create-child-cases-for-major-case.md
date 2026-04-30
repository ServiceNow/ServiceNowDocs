---
title: Create child cases for a major case
description: Users with the customer service manager role can create a child case for each of the customers included in the major case recipients list.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Major issue management overview, Administer Customer Service Management, Customer Service Management]
---

# Create child cases for a major case

Users with the customer service manager role can create a child case for each of the customers included in the major case recipients list.

## Before you begin

Role required: sn\_majorissue\_mgt.major\_issue\_manager, sn\_customerservice\_manager

## About this task

The **Create Child Cases** button on the Major Case form creates a child case for each account or consumer in the recipients list selected in the **Affected Customers** field. If a child case for an account or consumer already exists, the system does not create a duplicate child case.

**Note:** Use caution when selecting the recipients list for a major case. Selecting the wrong recipients list can have a serious impact by creating a large number of cases for incorrect accounts or consumers. Ensure that you have selected the correct recipients list before clicking **Create Child Cases**.

You can also create child cases for a major case from Agent Workspace.

Once child cases have been created, you cannot change the recipients list. Any additional recipients must be added manually. After manually adding recipients to the list, click **Create Child Cases** again to create child cases for these new recipients.

Creating child cases copies information from the major case to each of the child cases. The field values that are copied to the child cases are identified by the **sn\_customerservice.case\_fields\_to\_sync system** property.

## Procedure

1.  Open the desired major case.

2.  In the Major Issue Management form section, select a recipients list in the **Affected Customers** field.

3.  Click **Update**.

4.  Click **Create Child Cases**.

5.  In the Create Child Cases pop-up window, enter information about the major case

    This information is added as additional comments to each of the newly created child cases. If child cases for this major case already exist, these child cases are not updated.

6.  Click **Continue**.

    The child cases are created and added to the **Child Cases** related list.


**Related topics**  


[Recipients lists](../concept/major-issue-recipient-lists.md)

