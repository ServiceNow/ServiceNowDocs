---
title: Enable list actions based on dynamic conditions
description: Configure declarative actions for a list or related list to be enabled if the record satisfies dynamic conditions.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customizing Configurable Workspace with declarative actions, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Enable list actions based on dynamic conditions

Configure declarative actions for a list or related list to be enabled if the record satisfies dynamic conditions.

## Before you begin

Role required: admin

The system propertyglide.list.actions\_conditional\_evaluation\_enabled

controls whether the action for a list is enabled. This property is available by default.

## Procedure

1.  In the navigation filter, enter `List` or `Related List` for the action you want to configure.

2.  Enable dynamic evaluation of a list or related list action by enabling **Record Selection Required** and **Experience Restricted** in the Action Assignment record.

3.  Define the dynamic evaluation of a list or related list by applying the following configurations to the **Condition** tab within the Action Assignment.

    |Field|Configuration|
    |-----|-------------|
    |**Enable Dynamic Evaluation**|Set to true to use dynamic evaluation.|
    |**Dynamic Script Condition**|Write a scripted condition for dynamic evaluation.|
    |**Dynamic Record Conditions**|Add conditions for dynamic evaluation if you don't want to write a scripted condition.|

    ![Configurations for dynamic evaluation](../image/list-conditions.png)

    **Note:** You may experience slowness and unresponsiveness if this feature is used in combination with the **Select All**, which selects all records in a list, as conditions must be evaluated for all the selected records.


