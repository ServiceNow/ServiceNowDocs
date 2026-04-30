---
title: Adjust a contract
description: After creating a contract, you can change the start date, end date, or payment amount for a contract.
locale: en-US
release: zurich
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Contracts, Contract Management use, Contract Management, IT Asset Management]
---

# Adjust a contract

After creating a contract, you can change the start date, end date, or payment amount for a contract.

## Before you begin

Role required: admin, contract\_manager\(core UI and Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## About this task

To adjust a contract, the **State** should be **Active**. If the end date of a contract changes, the end date of any associated assets changes to match the new end date.

## Procedure

1.  Open the list of contracts that are used across your deployment.

    -   If you are using the core UI, navigate to **Contract** &gt; **Contracts** &gt; **All**.
    -   If you are using the Hardware Asset Workspace, open the Contract management view and then select the **All contracts** tab.
    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view and then select the **All contracts** tab.
2.  Select a contract in the **Active** state.

3.  Click **Adjust**.

4.  In the Adjust the Contract dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Contract Start Date|Date on which the contract takes effect.|
    |Contract End Date|Date on which the contract expires.|
    |Contract Payment Amount|Total amount paid for the contract. If the contract has one or more rate cards, this field shows the total of all rate card base costs.|

5.  Click **Submit Adjustments**.


-   **[Renew a contract](t_RenewAContract.md)**  
After you have created a contract or the contract has expired, you can renew the contract.
-   **[Cancel a contract](t_CancelAContract.md)**  
You can cancel a contract when the **State** is **Active**.

**Parent Topic:**[Contracts](../concept/c_Contracts.md)

**Related topics**  


[Create a contract](t_CreateAContract.md)

[Verify contract administrator assignment for notification](t_SendAContractNotification.md)

[Send the contract for approval](t_SendTheContractForApproval.md)

[Terms and conditions](../concept/c_TermsAndConditions.md)

[Create a contract rate card](t_ContractRateCardsAndExpenseLines.md)

[Monitor a contract](t_MonitoringContracts.md)

