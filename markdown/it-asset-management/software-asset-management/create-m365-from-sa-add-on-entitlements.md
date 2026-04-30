---
title: Create Microsoft 365 From SA and Add-on entitlements in Software Asset Management classic
description: Create a Microsoft 365 From SA or Add-on entitlement in the Software Asset Management classic application so that you can track and manage the From SA or Add-on licensing terms for your Microsoft 365 subscription software products and services.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Creating Microsoft 365 From SA and Add-on entitlements, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create Microsoft 365 From SA and Add-on entitlements in Software Asset Management classic

Create a Microsoft 365 From SA or Add-on entitlement in the Software Asset Management classic application so that you can track and manage the From SA or Add-on licensing terms for your Microsoft 365 subscription software products and services.

## Before you begin

Role required: sam\_user or sam\_admin

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **Software Entitlement**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For a detailed description of each field, see [Software entitlement fields](../reference/software-entitlement-fields.md).

    **Important:** To create a Microsoft 365 From SA or Add-on entitlement, set the **Software model** field to a Microsoft 365 software model and then set the **License type** field to either **From SA** or **Add-on**.

    **Tip:** If you’re using both Full and Add-on USLs for the same Microsoft 365 subscription software product or service, associate the corresponding entitlements with different software models to avoid licensing conflicts.

4.  Select **Save**.

5.  After the form reloads, select **Publish**.

    The State of the entitlement changes from Build to In use, and the entitlement is ready to be used in the reconciliation process.

6.  Assign the From SA or Add-on entitlement to the entitlement for the corresponding Microsoft software product or service that you want to transition from or add on to.

    **Note:** You can assign a From SA or Add-on entitlement to multiple corresponding Microsoft entitlements.

    **Note:** By default, the software model for your From SA or Add-on entitlement includes the corresponding Microsoft software product or service as a suite component. If the product or service isn’t already included as a suite component, you can include it manually. See [Create software models in Software Asset Management classic](record-terms-software-licenses.md) for detailed instructions.

    1.  Select the **Related Entitlements** tab.

    2.  In the Related Entitlement column of the Related Entitlements list, double-click **Insert a new row**.

    3.  When prompted, search for and select the corresponding Microsoft entitlement that you want to assign the From SA or Add-on entitlement to.

        **Important:** This entitlement must use either the Per User or Per Device license metric. In addition, it can’t already be assigned with another entitlement or have any active allocations.

        **Note:** If a corresponding Microsoft entitlement isn’t available for the given From SA or Add-on entitlement, you can create one.

    4.  Select the Save \(Enter\) icon \(![Save icon.](../image/save-icon.png)\).

    5.  Double-click the corresponding field in the **Active rights** column of the Related Entitlements list.

    6.  When prompted, enter the number of From SA or Add-on rights that you want to grant to the corresponding Microsoft entitlement.

        **Important:**

        -   For From SA rights, you must enter the total number of rights that you purchased for the corresponding Microsoft entitlement. For example, if you purchased 100 rights for the corresponding Microsoft entitlement, you must grant 100 From SA rights to that entitlement.
        -   For Add-on rights, you can enter any number of rights equal to or less than the total number of rights that you purchased for the given Add-on entitlement.
    7.  Select the Save \(Enter\) icon \(![Save icon.](../image/save-icon.png)\).

    8.  Select **Save** on the Software Entitlement form header.

    The From SA or Add-on entitlement is assigned to the specified Microsoft entitlement.


**Parent Topic:**[Creating Microsoft 365 From SA and Add-on entitlements](../concept/creating-m365-from-sa-add-on-entitlements.md)

**Related topics**  


[Software entitlement fields](../reference/software-entitlement-fields.md)

