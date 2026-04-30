---
title: Remediate an unsuccessful enterprise asset calibration
description: Remediate a failed enterprise asset calibration event by initiating a new work order and corresponding work order tasks for that event.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-05-14"
reading_time_minutes: 2
breadcrumb: [Managing work for your enterprise assets, Managing work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Remediate an unsuccessful enterprise asset calibration

Remediate a failed enterprise asset calibration event by initiating a new work order and corresponding work order tasks for that event.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Work management view.

3.  Select the **Calibrations and conditions** tab.

4.  In the Calibration overview section, select either the **All calibration events** widget or the **Calibration pending verification** widget.

5.  From the list of available calibration events, select the event that you want to remediate.

    The corresponding service event record opens.

6.  Initiate the creation of a new work order by selecting **Remediate**.

7.  In the Select template to begin remediation dialog box, search for and select the template that you want to apply to the new work order.

    **Note:** The dialog box lists only the work order templates that have at least one work order task with a Work type of Calibration.

8.  Select **OK**.

    The dialog box closes and you are automatically redirected to the Create New Work Order form. The form is auto-populated with the following information:

    -   The asset that you want to calibrate
    -   The location of the asset
    -   The original work order
    -   All other mandatory fields
9.  Fill out any additional fields in the Create New Work Order form and then select **Save**.

    See [Create a work order for an enterprise asset](create-eam-work-order.md) for a detailed description of each field.

10. Add additional work order tasks to the new work order.

    See [Create a work order task for an Enterprise Asset Management work order](create-eam-work-order-task.md) for detailed instructions.

11. Create a checklist of all items that must be completed for the new work order or the associated work order tasks.

    See [Create a checklist for an Enterprise Asset Management work order or work order task](create-checklist-items-eam-work-order.md) for detailed instructions.

12. Specify any upstream or downstream dependencies for the associated work order tasks.

    See [Create dependencies for an Enterprise Asset Management work order task](create-dependencies-eam-work-order-task.md) for detailed instructions.

13. Select **Ready for Work** to initiate work for the new work order.


## What to do next

Work with the assigned agent to complete and close all subsequent tasks for the new work order. See [Managing work for your enterprise assets](../concept/managing-work-enterprise-assets.md) for detailed instructions.

**Parent Topic:**[Managing work for your enterprise assets](../concept/managing-work-enterprise-assets.md)

