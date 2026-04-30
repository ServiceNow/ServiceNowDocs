---
title: Create a software maintenance contract example
description: One common use case for the Contract Management application is creating a contract to track maintenance payments for enterprise software. You can use this example to learn how to create a software maintenance contract.
locale: en-US
release: xanadu
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a contract, Contracts, Contract Management use, Contract Management, IT Asset Management]
---

# Create a software maintenance contract example

One common use case for the Contract Management application is creating a contract to track maintenance payments for enterprise software. You can use this example to learn how to create a software maintenance contract.

## Before you begin

Role required: contract\_manager or admin

## About this task

The goal of this example is to create a contract that shows the total amount of maintenance that must be paid for the software application, independent of different license purchases made over time. The Software Asset Management plugin must be activated to use this example.

## Procedure

1.  Create an [application model](../../product-catalog/concept/c_Models.md), adding a **Name** and specifying **Software License** in **Model categories**.

2.  Create a [software model](../../product-catalog/concept/c_Models.md), adding a **Name** and **Model Number**, and selecting the application model created in step 1.

3.  Create a new software entitlement by selecting the software model created in step 2.

4.  Navigate to **Contract** &gt; **Contracts** &gt; **Maintenance**.

5.  Click **New** and enter the following information.

<table id="choicetable_iy4_czk_35"><tbody><tr><td id="d32347e158">

**Agreement Type**

</td><td>

Select **Enterprise**.

</td></tr><tr><td id="d32347e170">

**Application Model**

</td><td>

Select the application model created in step 1.

</td></tr></tbody>
</table>6.  Right-click the form header and click **Save**.

    A number of related lists and sections appear.

7.  In the **Asset Covered** related list, click **New** and enter the following information.

<table id="choicetable_yqm_mzk_35"><tbody><tr><td id="d32347e207">

**Asset**

</td><td>

Select the software license created in step 3.

</td></tr><tr><td id="d32347e216">

**Date added**

</td><td>

Enter the value.

</td></tr></tbody>
</table>8.  Click **Submit**.

9.  Continue completing the form with the following information.

<table id="choicetable_smt_zzk_35"><tbody><tr><td id="d32347e243">

**Payment schedule**

</td><td>

Select **Annually**.

</td></tr><tr><td id="d32347e255">

**Payment amount**

</td><td>

Enter the value.

</td></tr></tbody>
</table>10. Complete the other fields as appropriate.

11. Click **Update**.

12. [Submit the contract for review](t_ObtainContractApproval.md).


**Parent Topic:**[Create a contract](t_CreateAContract.md)

**Related topics**  


[Add an asset to a contract](t_AddAnAssetToAContract.md)

[Add a user to a contract](t_AddAUserToAContract.md)

[Add a configuration item to a contract](t_AddAConfigurationItemToAContract.md)

[Add a document to a contract](t_AddADocumentToAContract.md)

[Software Asset Management](../../software-asset-management2/concept/c_SAMOverview.md)

