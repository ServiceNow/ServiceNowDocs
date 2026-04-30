---
title: Renew a contract
description: After you have created a contract or the contract has expired, you can renew the contract.
locale: en-US
release: yokohama
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Adjust a contract, Contracts, Contract Management use, Contract Management, Asset Management, IT Service Management]
---

# Renew a contract

After you have created a contract or the contract has expired, you can renew the contract.

## Before you begin

Role required: admin, contract\_manager\(core UI or Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## About this task

-   When a contract is renewed, a new contract isn't created. Instead, the same contract is updated with renewal information.
-   The changes to the start date and end date of a contract is captured in the Contract History tab.
-   Contract information and history is retained when a contract is renewed. If the end date of the contract changes, the end date of any associated assets changes to match. You can renew a contract that meets the following conditions.
    -   **State** is **Active** or **Expired**
    -   **Substate** is **None** or **Rejected**
-   If the system property **sn\_contract\_enable\_renewal\_flow** is enabled, the contract renewal workflow is available for maintenance &amp; warranty contracts. For more information, see [Contract renewal workflow](../concept/cont-renew-wf.md).

## Procedure

1.  Open the list of contracts that are used across your deployment.

    -   If you are using the core UI, navigate to **Contract** &gt; **Contracts** &gt; **All**.
    -   If you are using the Hardware Asset Workspace, open the Contract management view and then select the **All contracts** tab.

        Alternatively, select the **Overview** tab of the Contract management view. In the Contract overview section, locate the Expiring contract widget to view the list of contracts that are expiring.

    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view and then select the **All contracts** tab.

        Alternatively, select the **Overview** tab of the Contract and lease management view. In the Contract overview section, locate the Expiring contract widget to view the list of contracts that are expiring.

2.  Select a contract in the **Active** or **Expired** state.

3.  Click **Renew**.

4.  On the Renew the Contract form \(core UI\) or dialog box \(Hardware Asset Workspaceand Enterprise Asset Workspace\), fill in the fields.

    |Field|Descriptions|
    |-----|------------|
    |Approver|User who approves or rejects the contract.|
    |Options|Length of time for the renewal, in years.|
    |Renewal start date|Date on which the renewed contract takes effect.|
    |Renewal end date|Date on which the renewed contract expires.|
    |Cost adjustment type|Type of cost adjustment applied to the renewed contract: **None**, **Fixed**, **Manual**, or **CPI**.|
    |Cost adjustment percentage|Percentage increase or decrease in price of the renewed contract. To indicate a decrease in price, enter a negative percentage. A **Cost adjustment amount** or **Cost adjustment percentage** can be specified, but not both.|
    |Cost adjustment amount|Numerical increase or decrease in price of the renewed contract. To indicate a decrease in price, enter a negative number. A **Cost adjustment amount** or **Cost adjustment percentage** can be specified, but not both.|

5.  Perform one of the following steps.

    -   To save all entered data and change the substate to **Under Review**, click **Submit for Review**. The contract is sent to the specified **Approver**.
    -   To save all entered data and change the substate to **Awaiting Review**, click **Save**. The **Renew** button is available to submit the renewed contract for review later.
6.  Change any information on the **Contract** form, as necessary.

7.  Click **Update**.


## What to do next

If you selected the **Save** option, ensure that you click **Renew** when you are ready to submit the contract renewal for approval.

**Parent Topic:**[Adjust a contract](t_AdjustAContract.md)

