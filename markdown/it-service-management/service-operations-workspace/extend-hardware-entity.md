---
title: Extend hardware inventory
description: Extend the hardware inventory to add the CMPivot entity on the CMPivot entity list in the Microsoft Endpoint Configuration Manager.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation, Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Extend hardware inventory

Extend the hardware inventory to add the CMPivot entity on the CMPivot entity list in the Microsoft Endpoint Configuration Manager.

## Before you begin

The Microsoft Endpoint Configuration Manager server must be logged in using the Microsoft Remote Desktop.

Role required: admin

## Procedure

1.  Open the Microsoft Endpoint Configuration Manager.

2.  On the Microsoft Endpoint Configuration Manager, select **Administration**.

3.  On the Administration section, click **Client Settings**.

4.  Double-click the **Default Client Settings** that is displayed on the right pane of the window.

    The Default Settings pop-up window is displayed.

5.  On the Default Settings window, select **Hardware Inventory**.

6.  Click **Set Classes**.

    A Hardware Inventory Classes pop-up window containing the list of Hardware Inventory Classes is displayed.

7.  On the Hardware Inventory Classes window, select the entity and required attributes from the list.

    ![Add hardware inventory](../image/add-hardware-inventory.png)

8.  Click **OK**.


## Result

The added hardware inventory is displayed in the CMPivot entity list to verify the required attributes. For more information on verifying the CMPivot entity and the required attributes, see [Verify a CMPivot entity](verify-cmpivot-entity.md).

**Parent Topic:**[Configuring CI metrics for Microsoft Endpoint Configuration Manager for Investigation](../concept/config-ci-metrics-mecm-adapter.md)

