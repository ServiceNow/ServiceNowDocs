---
title: Create maintenance entitlements in workspace
description: Define license details, for all publishers other than Microsoft in the Software Asset Workspace. Create maintenance entitlements to manage all your software license maintenance needs such as start and end dates of your contracts and software upgrades.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create entitlements in workspace, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create maintenance entitlements in workspace

Define license details, for all publishers other than Microsoft in the Software Asset Workspace. Create maintenance entitlements to manage all your software license maintenance needs such as start and end dates of your contracts and software upgrades.

## Before you begin

Role required: sam\_user or sam\_admin

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace**.

2.  Click **Create entitlement** to open the Create new entitlement dialog box.

    You can also navigate to the Create new entitlement dialog box from **Software asset** &gt; **Software Asset Workspace** &gt; **License operations**.

3.  Select **Standard form** and then click **Next**.

    The Create New Software Entitlement page opens and the entitlement is in build status.

4.  On the Create New Software Entitlement page, fill in the mandatory fields and select **Maintenance** in the **License type** field.

    For a detailed description of all the fields, refer to [Software entitlement fields](../reference/software-entitlement-fields.md).

    If the **Next Version** field is populated in the software model that the maintenance entitlement is associated with and the metric group selected in the maintenance entitlement is **Common**, then the maintenance entitlement is updated with the next version of the software model. Next version is applicable only for the **Common** metric group.

5.  Once you have entered the required details, click **Publish**.

    The maintenance entitlement is created and state of the entitlement is changed to **in use** from **build**. The maintenance entitlement is ready to be picked up for the reconciliation process.

    **Note:** If you purchase a perpetual entitlement and associate only some of the rights of that entitlement with a maintenance entitlement, your perpetual entitlement is automatically split into two entitlements. For example, you purchased a perpetual entitlement with 50 active rights \(E1\). You associate 20 of these rights with 20 rights of a maintenance entitlement. Your E1 perpetual entitlement is now automatically split into two entitlements: one perpetual entitlement \(E1\) with 20 active rights \(and 50 purchase rights\) associated with 20 rights of the maintenance entitlement \(M1\) and another perpetual entitlement \(E2\) with 30 active rights without any maintenance association and no purchased rights.

6.  You can perform additional configuration on your new maintenance entitlement record.

    For a detailed description, see [Software entitlement fields](../reference/software-entitlement-fields.md).

    You can't add user or device allocations for maintenance entitlements.

    1.  Enter information pertaining to finance such as the vendor from which the asset was purchased, the invoice number, in the **Financial** tab.

    2.  Enter information relating to contracts such as the lease contracts, the expiration date of the warranty in the **Contracts** tab.

    3.  Link related perpetual entitlements to your maintenance entitlement from the **Related Entitlements** related list.

        1.  Select the **Related Entitlements** related list and then click **New**.

            The Create New Related Entitlement form opens in a new tab.

        2.  On the form, fill in the fields.

            |Field|Description|
            |-----|-----------|
            |Active rights|Number of rights that you want to grant to the related perpetual entitlement.|
            |Software Entitlement|Software entitlement that you are linking the related perpetual entitlement to. This field populates automatically.|
            |Related Entitlement|Related perpetual entitlement that you want to link.|
            |Domain|Domain that the related perpetual entitlement applies to. The default value is **global**.|

        3.  Click **Save**.
        To remove the relationship between the perpetual and maintenance entitlement, remove the entitlement from the **Related Entitlements** related list in the maintenance entitlement.

        If the entitlement has split and you've deleted the maintenance entitlement, the perpetual entitlement is not removed.

    4.  View the downgrade rights for the software model associated with the maintenance entitlement in the **Downgrade Rights** related list.

    5.  To manage license keys, and specify which licenses keys are allocated to entitlements, click the **License Keys** related list

    6.  To track the cost of your software over its lifecycle, click the **Expense Lines** related list.

    7.  To view the history of all maintenance entitlements that you have purchased, click the**Entitlement History** related list.

        For example, if you purchased two maintenance entitlements, M1 \(which is now retired\) and M2 \(currently in use\), the Entitlement History related link displays both M1 and M2.

    8.  To view the history of the newly upgraded software model related to your entitlement and the previous software model, click the **Upgrade History** related list.

7.  Once you have completed filling in the additional configuration details, click **Save**.


**Parent Topic:**[Create entitlements in workspace](create-entitlements-workspace.md)

