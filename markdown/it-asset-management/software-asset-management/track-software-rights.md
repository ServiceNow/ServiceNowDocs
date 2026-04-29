---
title: Create entitlements in Software Asset Management classic
description: Create entitlements in the Software Asset Management application classic to record your license details and allocate purchased software rights to users or devices.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Create entitlements in Software Asset Management classic

Create entitlements in the Software Asset Management application classic to record your license details and allocate purchased software rights to users or devices.

## Before you begin

Role required: sam\_user

## About this task

These instructions are for manually creating software entitlements or maintenance entitlements one at a time. If you already have software entitlements recorded in a spreadsheet, you can [import](view-entitlement-import-errors.md) them.

To automate the process of creating a software entitlement, specify a publisher part number in the software entitlement form. Based on the publisher part number, the software model, metric group, agreement type, and software lifecycle data \(if it exists\) automatically appears in the form.

To better manage your existing entitlements, you can edit certain fields in entitlements. You can edit fields such as **Purchased rights**, **Software model**, **License type**, **Number of packs**, and **Publisher part number**. Entitlements that have related entitlements, upgrade history, entitlement history, or upgraded entitlement are not editable.

**Note:** Microsoft reserve entitlements and source entitlements are not editable.

If you installed SaaS License Management, a software model is generated automatically after you create an integration profile. Create an entitlement for the software model to track software used against software owned. For more information about tracking SaaS licenses and usage, see [Viewing your SaaS and SSO subscriptions](../concept/usage-summary-saas.md).

If you installed the SAP publisher pack, see [Record software rights for SAP](create-entitlement-sap.md).

If you installed the Citrix publisher pack, see [Record software rights for Citrix](create-entitlement-citrix.md)

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Licensing** &gt; **Software Entitlements**.

2.  Select **New**.

3.  On the form, fill in the fields to record your license information.

    For detailed descriptions of the fields, see [Software entitlement fields](../reference/software-entitlement-fields.md).

4.  Right-click the form header and select **Save**.

    Saving the form instead of submitting keeps you on the entitlement record so you can perform additional configuration.

5.  To specify users and devices that have software rights allocated to them, select the **User Allocations** or **Device Allocations** section.

    The **Device Allocations** section is not visible for the IBM Resource Value Unit \(RVU\) license metric. The Resource Value Unit \(RVU\) license metric is licensed at the product level and so rights are not used by individual devices. When you upgrade from a prior release, that had device allocations, to the Australia release, the existing device relocations are removed.

6.  To track your software downgrade rights, select the [Downgrade Rights related list](../reference/software-entitlement-fields.md#section_lc4_mcm_43b) and specify the version.

    Creating a new record allows you to set an entitlement to previous versions of software. For example, the purchase of Microsoft Office Professional Plus 2016 rights entitles you to Microsoft Office Professional Plus 2013 too\).

    For more information, see [Downgrade Rights](../concept/downgrade-rights.md).

7.  To track the cost of your software over its lifecycle, configure [expense lines](https://www.servicenow.com/docs/access?context=c_ExpenseLine&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

8.  To manage license keys, select the [License Keys related list](../reference/software-entitlement-fields.md#section_iqv_dcm_43b) and specify which licenses keys are allocated to entitlements.

9.  To view the history of all maintenance entitlements that you have purchased, select the Entitlement History related list.

    For example, if you purchased two maintenance entitlements, M1 \(which is now retired\) and M2 \(currently in use\), the Entitlement History related link displays both M1 and M2.

10. To view the history of the newly upgraded software model related to your entitlement and the previous software model, select the Upgrade History related list.

11. Select **Update**.

    The entitlement is created and added to the entitlement list view.


-   **[Create maintenance entitlements in Software Asset Management classic](Record-software-rights-non-microsoft.md)**  
Define license details, for all publishers other than Microsoft, to manage all your software license maintenance needs such as start and end dates of your contracts and software upgrades.
-   **[Create entitlements for Microsoft Software Assurance in Software Asset Management classic](create-entitlement-microsoft-sa.md)**  
Define license details for Microsoft Software Assurance \(SA\) to manage your contracts start and end dates, software upgrades, and related software entitlements.

**Parent Topic:**[Using Software Asset Management classic](../concept/using-sam-classic.md)

**Related topics**  


[Software entitlement fields](../reference/software-entitlement-fields.md)

[Software models and Software entitlements](../concept/software-models-and-entitlements.md)

[Software license metrics](../concept/c_SAMLicenseMetrics.md)

