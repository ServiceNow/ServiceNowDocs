---
title: Use consumable assets in Enterprise Asset Workspace
description: To use consumable assets, ensure that they are in the In stock state and Available substate.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise assets, Managing enterprise assets and models, Enterprise Asset Management, IT Asset Management]
---

# Use consumable assets in Enterprise Asset Workspace

To use consumable assets, ensure that they are in the **In stock** state and **Available** substate.

## Before you begin

**Note:** Only consumables created from models in the Enterprise Asset Management application can be used if the **Asset strategy tracking** for the model is set to **create consumable asset**.

Role required: asset

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Enterprise asset estate** &gt; **Consumable assets**.

2.  Select a consumable asset with a state of **In Stock** and a substate of **Available**.

3.  Select **Consume**.

    The Consume dialog box appears.

4.  Enter the quantity to consume in the **Quantity** field.

5.  In **Asset** list, select the lookup icon and select the asset associated with the consumable.

    For example, a mouse tracked as a consumable asset can be associated with a non-consumable asset such as a computer.

6.  In **User** list, select the lookup icon and select a user associated with the consumable.

7.  Select **OK**.

    On the **Consumable** form, the **Quantity** field shows the reduced number. The Consumables list contains two records for the consumable in the specific stockroom: one with a state and substate of **In Stock** and **Available** \(if you did not consume the entire quantity\), and one with a state of **Consumed**. If a consumable is not in the process of being transferred to a different stockroom and information in the data record is the same, similar records merge automatically. After a consumable is consumed, the record remains in the system for reporting purposes.


**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

