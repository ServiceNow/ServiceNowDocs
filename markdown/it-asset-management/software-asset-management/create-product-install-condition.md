---
title: Create product install conditions
description: Create product install conditions in the Software Asset Workspace that apply across all software models of a product during reconciliation.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [License operations view, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create product install conditions

Create product install conditions in the Software Asset Workspace that apply across all software models of a product during reconciliation.

## Before you begin

Installs that do not meet the required product install conditions will be included in the reconciliation process; however, they are likely to be flagged as unlicensed.

To create product install conditions, you must request and activate the Software Asset Workspace \(com.sn\_sam\_workspace\) plugin. For details on requesting and activating the Software Asset Workspace \(com.sn\_sam\_workspace\) plugin, see [Request Software Asset Management](t_RequSoftwareAssetMgmt.md).

Role required: sam\_admin

## About this task

Install conditions define where a software product can be installed. Product install conditions account for all the software model installations of a product during reconciliation.

**Note:** If you want to set up install conditions for specific software models and not the entire software product suite, you can choose to add software install conditions. For details on adding software install conditions, see [Create software models in workspace](create-swmodels-workspace.md).

## Procedure

1.  Navigate to **Software Asset** &gt; **Software Asset Workspace** &gt; **License operations** &gt; **Licensing**.

2.  Select **Product install condition**.

3.  Select **New**.

4.  From the list of available products, select a product.

5.  Select **Set conditions**.

6.  Add filter conditions that contain a field, operator, and value.

    You can add multiple install conditions to a software product using the following options:

    -   **or**: Enables you to specify any of the conditions that a software installation can meet to be included in reconciliation.
    -   **and**: Enables you to specify all the conditions that a software installation must meet to be included in reconciliation.
    -   **+ New condition set**: Enables you to specify additional sets of conditions that a software installation can meet to be included in reconciliation.
7.  Select **Set**.

8.  After setting up the install conditions successfully, select **Save**.

    The install conditions are added for the complete suite of the software product. You can view the install conditions you have created on the Product install condition landing page.


