---
title: Revise a configuration item
description: Revise a CI \(Configuration Item\) of the connection to update a CI in the Telecommunications Network Inventory application.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Instantiating your network inventory by using design and assign, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Revise a configuration item

Revise a CI \(Configuration Item\) of the connection to update a CI in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the desired change request.

    To create a change request, see [Create a change request from Network Inventory Workspace](../task/create_a_change_request_in_tni.md).

4.  Select the **Change Tasks** tab.

5.  Select **New**.

6.  Choose a change task type:

    -   Planning
    -   Implementation
    -   Testing
    -   Review
7.  Select **Create**.

    A change task form based on the selected change model is displayed.

8.  Select **Revise CI** in the **Request type** field and fill other fields.

    To learn more about other fields, see [Change request and change task forms](change_request_forms.md).

9.  Select **Save**.

10. On the **Task Attributes** form, select a CI from the list of **CI to be revised** field.

11. Select **Submit**.

    A record is created in the Inventory Revision Histories table. The selected CI and related tables are cloned and the cloned CI name is populated in the **Configuration item** field. Also, both the original and cloned CIs are added under the **Affected CIs** tab.

    **Note:**

    -   To customize the cloning process and the related tables that must be cloned, see [../task/clone-and-revise-a-ci.md](../task/clone-and-revise-a-ci.md).
    -   The revision data is automatically archived to the revision history archival rule \(Archive Rules → Inventory Revision History Archival Rule\[sn\_ni\_core\_inventory\_revision\_history\]\) table after a period of one year of the CI creation. Subsequently, all data within the archival table is permanently deleted \(ar\_sn\_ni\_core\_inventory\_revision\_history\) after an additional year. Customization can be achieved by modifying the relevant tables.
    -   The revision history currently captures only Configuration Item \(CI\) attributes, related data, and CI relationships. To include additional data from other tables, logical connection \(audit\_reference\_tableinfo\_logical\_connection\) and physical connection \(audit\_reference\_tableinfo\_logical\_connection\) system properties can be updated. The format for specifying table and column names within these properties is - table1\_name:column1\_name, table1\_name:column2\_name.
12. Navigate to a change task and select **Validate Revision** to validate both original and revised CI.

    -   Before operationalization, you can validate to track the changes performed on the cloned CIs. If the data isn’t matching with the original CI, the validation fails and a message is displayed that the cloned CI is updated after the cloning.
    -   To customize the validation process, update the Validate CI Revision action flow. To learn more, see [Customize the Validation of Revision CI](customize-the-validation-of-revision-ci.md).
    -   To skip a field in the validation process, edit \(sn\_ni\_core.revision\_val\_ignore\_fields\_logical\_connection\) table for logical connection CIs and \(sn\_ni\_core.revision\_val\_ignore\_fields\_physical\_connection\) table for physical connection CIs.

## What to do next

You can update the cloned CI and operationalize the CIs. To learn more about operationalization, see [Operationalize a configuration item](../task/operationalize-a-configuration-item.md).

**Parent Topic:**[Instantiating your network inventory by using design and assign](instantiate-asset-using-template-relationship-model.md)

**Related topics**  


[Revision, operationalization, and decommission of a Configuration Item](revision-of-a-confiuguration-item.md)

