---
title: Logical connection modification request form
description: The Logical connection modification request form enables you to modify endpoints of a logical connection record in the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Logical connection modification request form

The Logical connection modification request form enables you to modify endpoints of a logical connection record in the Telecommunications Network Inventory application.

<table id="table_fzh_ksr_nzb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

A end Site

</td><td>

Starting network \(Site A field\) site where this selected logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

Z end Site

</td><td>

Ending network site \(Site Z field\) where this selected logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

A end Equipment

</td><td>

Starting network \(Site A field\) equipment where this logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

Z end Equipment

</td><td>

Ending network \(Site Z field\) equipment where this logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

A end interface

</td><td>

Starting interface \(Site A field\) point where this logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

Z end interface

</td><td>

Ending interface \(Site Z field\) point where this logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

Logical Connection

</td><td>

Select a logical connection from the list that needs modification.**Note:**

-   The list includes both logical connection and their revisions. On selecting the revision of a logical connection, the **Create Revision** check box disappears.
-   This field is auto populated based on the selected site or equipment or interface.

</td></tr><tr><td>

Create Revision

</td><td>

Option to enable or disable revision process.**Note:**

1.  On selecting this check box, the following occurs:
    1.  The revision process is initiated. To learn more, see [Revision, operationalization, and decommission of a Configuration Item](../concept/revision-of-a-confiuguration-item.md).
    2.  Two change tasks for modification and revision are created with the open and closed status respectively.
2.  Open the Modify Logical or Physical connection change task to start modifying the duplicated logical or physical connection and operationalize further. To learn more, see [Operationalize a configuration item](../task/operationalize-a-configuration-item.md).
3.  In the process of revision of physical connection modification, the logical connections associated with physical connection ports are updated during the operationalization process.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Modify logical connection endpoints model](../task/create-a-change-request-by-using-modify-logical-connection-endpoints-model.md)

