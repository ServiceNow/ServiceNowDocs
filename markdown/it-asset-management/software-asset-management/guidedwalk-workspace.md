---
title: Create entitlements using the guided walk-through
description: Use the guided walk-through playbook for a step-by-step process of creating entitlements.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create entitlements using the guided walk-through

Use the guided walk-through playbook for a step-by-step process of creating entitlements.

## Before you begin

You can create perpetual entitlements with or without a publisher part number. You can also create SaaS entitlements to manage software subscriptions of your pure SaaS and hybrid applications.

The guided walk-through takes you through the entire process of creating an entitlement. Initially the entitlement is in the **build** status when you start creating it. Once you publish the entitlement, the status changes to **in use** and makes the entitlement eligible to be included in the reconciliation process.

The process of creating an entitlement is organized into lanes. The lanes appear in the left pane of the page. Each lane has a few tasks that you're asked to complete. After you complete a task, select **Mark Complete** to move to the next task. You can select **Save** at any time in the process to save your changes and return to the playbook later. You can also select **Cancel** to abort the entitlement setup at any point of time. While you're performing a particular task, a status of in progress appears for that task. As you mark a task complete, the status of that task changes to complete. Once you complete all the tasks in a lane, you move to the next lane.

Role required: sam\_user or sam\_admin

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace**.

    The Software asset overview page appears.

2.  Select **Create entitlement**.

    ![Guided walk-through for creating entitlements](../image/playbook-popup.png)

3.  Select **Guided step by step walk-through** and select **Next**.

    The Create New Software Entitlement page opens and the status of the entitlement is in **build**.

    ![Create an entitlement via the guided walk-through playbook](../image/create-new-entitlement-playbook.png)

4.  Select whether you're creating an entitlement for an on-premises product or for a SaaS product.

    -   If you select **on-premise**, enter the fields listed in the following On-premise entitlement table.
    -   If you select **SaaS**, enter the fields listed in the following SaaS entitlement table.
    **Note:** You're asked to select on-premise or SaaS only if the Software Asset Management - SaaS License Management Integrations \(sn\_sam\_saas\_int\) plugin is activated. If this plugin is not activated, then the product type is automatically selected as on-premise.

    |on-premise entitlement fields|Description|
    |-----------------------------|-----------|
    |Do you have a PPN|Select if you have a publisher part number \(PPN\) for setting up the entitlement.|
    |Publisher Part number|Enter the PPN if you have one or otherwise create a custom PPN by clicking the link in the informational message to take you to the Custom Part Numbers page.|

<table id="table_bwh_4nm_qpb"><thead><tr><th>

SaaS entitlement fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Has an integration profile being set-up

</td><td>

If you have an integration profile already set-up, select it. Otherwise, select the appropriate link to create a direct or a SSO integration profile. **Note:** Integration profile is needed to view software usage information and optimize stale licenses.

</td></tr><tr><td>

Are you using a direct or SSO integration profile for this SaaS product

</td><td>

Select the type of profile, direct or SSO, that you're using for this SaaS product.

</td></tr><tr><td>

Select an integration profile

</td><td>

Based on the type of profile you specified, select an integration profile.

</td></tr></tbody>
</table>5.  Select a software model for the entitlement.

    Once you complete all the tasks in the Product Details lane, you can move to the Entitlement Details lane.

6.  Select **Entitlement Details**.

    If you entered a PPN, then the metric group, agreement type, and license type are automatically populated. You can change the values if required.

7.  Enter a value in **Asset tag** to track the asset through its life cycle.

8.  Select a value in **License metric** for the license group that the software license is counted against when reconciliation is run.

    If you select Per Core or Per Core \(with CAL\), you must enter values in the following fields:

    1.  In **Rights per license pack**, enter rights associated with each pack that is purchased for Microsoft Per Core or Microsoft Per Core with CAL licenses.

    2.  In **Number of packs**, enter the number of packs for Microsoft Per Core or Microsoft Per Core with CAL licenses.

9.  Enter the number of rights purchased in **Purchased rights**.

    If you have specified a Microsoft Per Core or Microsoft Per Core with CAL license type, this field is automatically populated. This value is based on the values entered in the Rights per license pack field multiplied by the value in the Number of packs field.

10. Enter the cost of the software in **Unit cost**.

    Once you complete all the tasks in the Entitlement Details lane, you can move to the Additional Details lane.

11. Select **Additional Details**.

12. Enter the name of the company that this asset belongs to in **Company**.

13. Enter the location where the license is used.

    For example, you can specify a specific site, country, or region.

14. Enter the department of the person assigned to this software license in **Department**.

15. Enter the user or department with financial ownership of the asset in **Owned by**.

    The asset owner can be different than the manager.

16. Enter the financial details for the vendor in **Vendor**, **Invoice Number**, **Request Line**, **Purchased**, **Opened**, **GL account** and **Cost Center** fields.

17. Enter contract details in **Lease Contract**, **Warranty expiration**, **Support Group** and **Supported by** fields.

    After you complete all the tasks in the Additional Details lane, you can move to the Review lane.

18. Select **Review** to show all the details that you have entered in all the lanes.

19. You can choose to edit any field, otherwise select **Finish**.

20. Select **Publish** to publish this entitlement for use.

    The entitlement is created and state of the entitlement is changed to **in use** from **build**. The entitlement is ready to be used for the reconciliation process.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

