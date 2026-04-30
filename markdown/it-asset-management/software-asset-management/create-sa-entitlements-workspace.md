---
title: Create Microsoft Software Assurance entitlements in workspace
description: Define license details for Microsoft Software Assurance \(SA\) in the Software Asset Workspace to manage your contracts start and end dates, software upgrades, and related software entitlements.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create entitlements in workspace, Configuring Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create Microsoft Software Assurance entitlements in workspace

Define license details for Microsoft Software Assurance \(SA\) in the Software Asset Workspace to manage your contracts start and end dates, software upgrades, and related software entitlements.

## Before you begin

Role required: sam\_user or sam\_admin

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace**.

2.  Click **Create entitlement** to open the Create new entitlement dialog box.

    You can also navigate to the Create new entitlement dialog box from **Software asset** &gt; **Software Asset Workspace** &gt; **License operations**.

3.  Select **Standard form** and then click **Next**.

    The Create New Software Entitlement page opens and the entitlement is in build status.

4.  On the Create New Software Entitlement form, fill in the mandatory fields and select **SA** in the **License type** field.

    You must enter the number of rights to be granted for the SA entitlement in the **Active rights** field.

    For a detailed description of the fields related to all entitlements, see [Create entitlements in Software Asset Management classic](track-software-rights.md).

    **Note:** You can't add user or device allocations for SA entitlements.

5.  Click **Publish**.

    An entitlement appears in the Software Entitlement list.

    **Note:** If you purchase a perpetual entitlement and associate only some of the rights of that entitlement with a SA entitlement, your perpetual entitlement is automatically split into two entitlements. For example, you purchased a perpetual entitlement with 50 active rights \(E1\). You associate 20 of these rights with 20 rights of a SA entitlement. Your E1 perpetual entitlement is now automatically split into two entitlements: one perpetual entitlement \(E1\) with 20 active rights \(and 50 purchase rights\) associated with 20 rights of the SA entitlement \(M1\) and another perpetual entitlement \(E2\) with 30 active rights without any SA association and no purchased rights.

6.  To perform additional configuration, select your new software entitlement record from the Software Entitlements list.

    1.  To link related perpetual and SA entitlements, use the following steps:

        1.  Select the Related Entitlements related list and then click **New**.

            The Create New Related Entitlement form opens in a new tab.

        2.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Active rights|Number of rights that you want to grant to the related perpetual or SA entitlement.|
            |Software Entitlement|Software entitlement that you are linking the related perpetual or SA entitlement to. This field populates automatically.|
            |Related Entitlement|Related perpetual or SA entitlement that you want to link.|
            |Domain|Domain that the related perpetual or SA entitlement applies to. The default value is **global**.|

        3.  Click **Save**.
        To remove the relationship between the perpetual and SA entitlement, remove the entitlement from the Related Entitlements related list in the SA entitlement.

        If you delete either the perpetual or SA entitlement that is linked, the other entitlement isn't deleted.

        If the entitlement has split and you've deleted the SA entitlement, the perpetual entitlement is not removed.

    2.  To link your software to a newer version as part of your maintenance contract, click the Upgraded Entitlements related list.

        **Note:** This related list is only available if you selected **Step-up** as the entitlement license type.

        If the **Next Version** field is populated on the software model, entitlements with active SA are updated to the new version of the software model.

        After you've linked your related entitlements, if there aren't enough SA rights to cover the perpetual entitlement rights, an error message displays.

    3.  To view all previously related entitlements that are linked, click the Entitlement History related list.

        **Note:** Validation is run against the active rights of all related entitlements automatically. If there's an error with the calculation, a message with additional information on how to resolve the problem is displayed.

7.  Click **Update**.


**Parent Topic:**[Create entitlements in workspace](create-entitlements-workspace.md)

