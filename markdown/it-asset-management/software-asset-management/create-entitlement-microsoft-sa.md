---
title: Create entitlements for Microsoft Software Assurance in Software Asset Management classic
description: Define license details for Microsoft Software Assurance \(SA\) to manage your contracts start and end dates, software upgrades, and related software entitlements.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create entitlements in Software Asset Management classic, Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Create entitlements for Microsoft Software Assurance in Software Asset Management classic

Define license details for Microsoft Software Assurance \(SA\) to manage your contracts start and end dates, software upgrades, and related software entitlements.

## Before you begin

Role required: sam\_user or sam\_admin

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Licensing** &gt; **Software Entitlements**.

2.  Click **New**.

3.  On the Software Entitlement form, fill in the details about the software publisher rights that you've purchased and select **Maintenance** in the **License type** field.

    **Note:** Make sure that you enter the number of rights to be granted for the SA entitlement in the **Active rights** field. You can't add user or device allocations for SA entitlements.

    For a detailed description of the fields related to all entitlements, see [Create entitlements in Software Asset Management classic](track-software-rights.md).

4.  Right-click the form header and select **Save**.

    An entitlement appears in the Software Entitlement list.

    **Note:** If you purchase a perpetual entitlement and associate only some of the rights of that entitlement with a SA entitlement, your perpetual entitlement is automatically split into two entitlements. For example, you purchased a perpetual entitlement with 50 active rights \(E1\). You associate 20 of these rights with 20 rights of a SA entitlement. Your E1 perpetual entitlement is now automatically split into two entitlements: one perpetual entitlement \(E1\) with 20 active rights \(and 50 purchase rights\) associated with 20 rights of the SA entitlement \(M1\) and another perpetual entitlement \(E2\) with 30 active rights without any SA association and no purchased rights.

5.  To perform additional configuration, select your new software entitlement record from the Software Entitlements list.

    1.  To link related perpetual and SA entitlements, use the following steps:

        1.  On the Software Entitlement form, select the **Related Entitlements** tab.
        2.  In the **Related Entitlement** field of the Related Entitlements list, double-click **Insert a new row...**.
        3.  When prompted, search for and select the related perpetual or SA entitlement that you want to link and then click the Save \(![Save icon.](../image/save-icon.png)\) icon.
        4.  Double-click the corresponding **Active rights** field.
        5.  When prompted, enter the number of rights that you want to grant to the related perpetual or SA entitlement and then click the Save \(![Save icon.](../image/save-icon.png)\) icon.
        6.  Click **Save** on the Software Entitlement form header.
        To remove the relationship between the perpetual and SA entitlement, remove the entitlement from the Related Entitlements list.

        If you delete either the perpetual or SA entitlement that is linked, the other entitlement isn't deleted.

        If the entitlement has split and you've deleted the SA entitlement, the perpetual entitlement is not removed.

    2.  To link your software to a newer version as part of your maintenance contract, click the Upgraded Entitlements related list.

        **Note:** This related list is only available if you selected **Step-up** as the entitlement license type.

        If the **Next Version** field is populated on the software model, entitlements with active SA are updated to the new version of the software model.

        After you've linked your related entitlements, if there aren't enough SA rights to cover the perpetual entitlement rights, an error message displays.

    3.  To view all previously related entitlements that are linked, click the Entitlement History related list.

        **Note:** Validation is run against the active rights of all related entitlements automatically. If there's an error with the calculation, a message with additional information on how to resolve the problem is displayed.

6.  Click **Update**.


## Result

After you've created an entitlement, you can begin [viewing license usage](../concept/sam-license-workbench.md).

## Record software rights for Microsoft Software Assurance

You have purchased 100 rights of Microsoft SQL Server 2016.

![Software Entitlement form with a Perpetual License Type selected.](../image/sa-perpetual-entitlement.png)

You have also purchased SA for your Microsoft SQL Server 2016 licenses.

![Software Entitlement form with a Software Assurance License Type selected.](../image/sa-license-entitlement.png)

To accurately track your licenses, associate your perpetual and SA entitlements.

![Add the related SA software entitlement to the perpetual entitlement.](../image/sa-perpetual-related.gif)

While you are under active maintenance, Microsoft releases SQL Server 2016 datacenter. Step up from your current version to the new release by creating an entitlement for your upgraded software and link the related entitlements.

![Add the entitlement that is being upgraded to the new software entitlement you created.](../image/step-up-sql-server.png)

**Parent Topic:**[Create entitlements in Software Asset Management classic](track-software-rights.md)

