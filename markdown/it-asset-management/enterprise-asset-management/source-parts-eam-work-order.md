---
title: Source parts for an Enterprise Asset Management work order or work order task
description: If the enterprise asset that is associated with your work order or work order task is missing any required assets or parts, source them using a catalog request.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Managing work for your enterprise assets, Manage work orders for your enterprise assets, Enterprise Asset Management, IT Asset Management]
---

# Source parts for an Enterprise Asset Management work order or work order task

If the enterprise asset that is associated with your work order or work order task is missing any required assets or parts, source them using a catalog request.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager or wm\_agent

**Important:** Although you can use either the sn\_eam.enterprise\_asset\_manager or wm\_agent role to create catalog requests, you can use only the sn\_eam.enterprise\_asset\_manager role to source those requests.

## About this task

You can verify which assets or parts are missing using the **Part Requirements** tab on the work order or work order task. For more information on part requirements, see [Create a part requirement for an Enterprise Asset Management work order or work order task](create-part-requirement-eam-work-order.md).

You can specify parts requirements that you want to source instead of sourcing all parts requirements.

## Procedure

1.  From the Enterprise Asset Workspace, open the Work management view.

2.  Open the record for either the work order or work order task that you want to source parts for.

    -   To open a work order record, select the **Work orders** tab. From the list of available work orders, select the work order that you want to source parts for.
    -   To open a work order task record, select the **Work order tasks** tab. From the list of available work order tasks, select the work order task that you want to source parts for.
3.  On the work order or work order task record, select **Source Parts Request**.

    The Source parts request dialog box opens. All part requirement models that have still not been requested are listed and selected by default.

4.  Enter the quantity that you want to request in the **Request quantity** field.

    The quantity you enter can be greater than the required quantity.

5.  Select **OK**.

    A confirmation message appears, indicating that a corresponding catalog request has been created only for the selected parts requirement.

6.  From the left navigation menu of the Enterprise Asset Workspace, open the Asset operations view.

7.  On the **Lists** tab of the Asset operations view, navigate to **Procurement** &gt; **Requests**.

8.  Select the request for the assets or parts that you need to source.

    The catalog request record opens. You can verify the assets or parts that you need to source by using the **Requested Items** tab of the catalog request record.

9.  On the **Catalog Tasks** tab of the catalog request record, select the task number for the Source Request Items catalog task.

    The Source Request Items catalog task opens.

10. Select **Source request**.

    You are automatically redirected to the corresponding source request.

11. Source the required assets or parts using one or more of the following options:

    **Note:** The source request displays all assets and parts that need to be sourced. However, you must source each asset and part separately.

    -   **Local stock**: Option to consume assets or parts from a local stockroom.

        To use this option, click **Consume** on the Local stock widget. When prompted, specify the consumption details for the source request.

    -   **Transferable stock**: Option to transfer assets or parts between available stockrooms or to a location where the requester can receive those assets or parts.

        To use this option, click **Transfer** on the Transferable stock widget. When prompted, specify the transfer details for the source request.

    -   **Vendor purchase**: Option to purchase additional assets or parts from a supported asset vendor.

        To use this option, click **Purchase** on the Vendor purchase widget. When prompted, specify the purchase details for the source request.

12. Select **Submit**.

    The Source Request dialog box opens.

13. In the dialog box, select **OK**.

    The dialog box closes and you automatically return to the catalog request record.


**Parent Topic:**[Managing work for your enterprise assets](../concept/managing-work-enterprise-assets.md)

