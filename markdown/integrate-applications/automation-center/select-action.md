---
title: Select an action
description: Select an action suitable for your data import into ServiceNow instance.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring data import, Create an automation source, Working with Connection manager, Use, Automation Center, Workflow Data Fabric]
---

# Select an action

Select an action suitable for your data import into ServiceNow instance.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

Proceed from the **Select a spoke** section. For information on selecting a spoke, see [Select a spoke](select-spoke.md).

**Important:**

-   Only actions that include a REST step and that are active and published are listed.
-   Select an action that has the output type as "array.output". Else, the data is not available for import.

## Procedure

1.  Select an action.

    If you want to create a new action, select **Create action**. For detailed information, see [Creating an action](../concept/creating-action.md).

    -   Select a spoke from the **Spoke** list to view only those actions that are associated with the selected spoke.
    -   Sort the list alphabetically using the **Sort** field.
    -   Search an action by its name from the **Search** field.
2.  Select **Save and continue**.

    The **Configure batch import** section is displayed.


**Parent Topic:**[Configuring data import](../concept/configure-data-import.md)

