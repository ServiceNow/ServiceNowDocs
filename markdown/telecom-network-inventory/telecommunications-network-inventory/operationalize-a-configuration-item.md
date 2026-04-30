---
title: Operationalize a configuration item
description: Operationalize a Configuration Item so that you can finalize the changes and apply them on the original CI.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Design &amp; Assign Network, Use, Telecommunications Network Inventory]
---

# Operationalize a configuration item

Operationalize a Configuration Item so that you can finalize the changes and apply them on the original CI.

## Before you begin

-   Ensure to have a revised CI.
-   Role required: sn\_ni\_core.inventory\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the desired change request.

    To create a change request, see [Create a change request from Network Inventory Workspace](create_a_change_request_in_tni.md).

4.  Select the **Change Tasks** tab.

5.  Select **New**.

6.  Choose a change task type:

    -   Planning
    -   Implementation
    -   Testing
    -   Review
7.  Select **Create**.

    A change task form based on the selected change model is displayed.

8.  Select **Operationalize CI** in the **Request type** field and fill other fields.

    To learn more about other fields, see [Change request and change task forms](../concept/change_request_forms.md).

9.  Select **Save**.

10. On the **Task Attributes** form, either select a CI from the list of **CI to be operationalized** field or select a change request from the **Change request ID** field.

11. Select **Submit**.

    The **State** of the change task changes to Closed. The work notes are updated with the details of operationalized CIs.

    **Note:** On selecting a change request, all the revised Configuration Items \(CIs\) listed under the **Affected CIs** tab are operationalized and the work notes are updated accordingly.


**Parent Topic:**[Instantiating inventory using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

