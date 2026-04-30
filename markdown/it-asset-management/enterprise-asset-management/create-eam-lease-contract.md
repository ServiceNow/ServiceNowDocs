---
title: Create a contract for your leased enterprise assets
description: Create a contract to define the lease details of your enterprise assets.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create and manage contracts for enterprise assets, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Create a contract for your leased enterprise assets

Create a contract to define the lease details of your enterprise assets.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## About this task

The following steps describe how to create contracts for leased enterprise assets only. For information on how to create other types of contracts, see [Contract Management](https://www.servicenow.com/docs/access?context=c_ContractManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Procedure

1.  From the Enterprise Asset Workspace, open the Contract and lease management view.

2.  On the **Lease contracts** tab, select **New**.

3.  On the Create New Contract form, fill in the fields.

    See [Contract fields for Enterprise Asset Management](../reference/contract-fields-eam.md) for a detailed description of each field.

4.  Select **Save**.

    A new contract record is created for the lease contract.

5.  Build terms and conditions for the lease contract.

    Before you can build terms and conditions for a lease contract, you must create a terms and conditions record and add it to the contract. For detailed instructions on how to create a terms and conditions record, see [Create a terms and conditions record](https://www.servicenow.com/docs/access?context=t_CreateATermsAndConditionsRecord&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US). For detailed instructions on how to add a terms and conditions record to a contract, see [Add terms and conditions to a contract](https://www.servicenow.com/docs/access?context=t_AddTermsAndConditionsToAContract&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

    1.  On the lease contract record header, select the More Actions icon \(![More Actions icon.](../../hardware-asset-management/image/more-actions-icon.png)\).

    2.  When prompted, select **Build Terms and Conditions**.

    The terms and conditions are built for the lease contract and added to the **Contract History** tab of the lease contract record. On the **Contract History** tab, you can select the date in the **Contract Starts** field to view the complete terms and conditions for the lease contract.

6.  Add all enterprise assets that are covered by the lease contract.

    **Note:** If you created a multi-component asset from a multi-component model, only the parent asset can be added to the lease contract. The associated child assets cannot be added to the lease contract. See [Multi-component models and assets in Enterprise Asset Management](../concept/complex-models.md) for more information on multi-component assets.

    1.  On the **Assets Covered** tab of the lease contract record, select **Add**.

        The Add assets dialog box opens.

    2.  In the dialog box, select the check box for each enterprise asset that is covered by the lease contract.

        **Note:** The dialog box displays only the enterprise assets that are not already covered by another active lease contract.

    3.  Select **Add**.

        The dialog box closes and the **Assets Covered** tab automatically reloads with the list of all enterprise assets that you added.

7.  Create expense lines to track the cost of each enterprise asset that is covered by the lease contract.

    1.  On the **Expense Lines** tab of the lease contract record, select **New**.

    2.  On the Create New Expense Line form, fill in the fields.

        See [Expense line fields for Enterprise Asset Management](../reference/expense-line-fields-eam.md) for a detailed description of each field.

    3.  Select **Save**.

        A new expense line record is created for the selected enterprise asset.

    4.  Close the expense line record to return to the **Expense Lines** tab of the lease contract record.

    5.  Repeat steps a to d for each expense line that you want to create.

8.  Create child contracts that you want to associate with the lease contract.

    1.  On the **Child Contracts** tab of the lease contract record, select **New**.

    2.  In the **Contract model** field of the Create New Contract form, search for and select the type of contract that you want to create.

    3.  Configure the child contract by following the same steps that you used to configure the lease contract \(steps 3 to 7\).

    4.  Select **Submit For Review**.

        A review notification is sent to the user that you specified in the **Approver** field of the child contract record. After reviewing the child contract, the user can either approve or reject it.

    5.  Repeat steps a to d for every child contract that you want to create.

9.  Select **Submit For Review**.

    A review notification is sent to the user that you specified in the **Approver** field of the lease contract record. After reviewing the lease contract, the user can either approve or reject it.


**Parent Topic:**[Create and manage contracts for enterprise assets](../concept/create-manage-enterprise-asset-contracts.md)

