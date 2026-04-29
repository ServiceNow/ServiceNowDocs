---
title: Create a new expense line
description: Typically, expense lines are automatically generated based on assets or users, but you can create a new expense line manually if needed.
locale: en-US
release: australia
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a contract rate card, Contracts, Contract Management use, Contract Management, Asset Management, IT Service Management]
---

# Create a new expense line

Typically, expense lines are automatically generated based on assets or users, but you can create a new expense line manually if needed.

## Before you begin

Role required: asset, contract\_manager\(core UI and Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## Procedure

1.  Open the list of contracts that are used across your deployment.

    -   If you are using the core UI, navigate to **Contract Management** &gt; **Contract** &gt; **All**.
    -   If you are using the Hardware Asset Workspace, open the Contract management view and then select the **All contracts** tab.
    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view and then select the **All contracts** tab.
2.  Select a contract.

3.  In the **Expense Lines** related list \(core UI\) or tab \(Hardware Asset Workspaceand Enterprise Asset Workspace\), click **New**.

4.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Number|The unique number identifying the expense line.|
    |Date|The date on which the expense line was created.|
    |Rate Card|The identification number of the rate card to which the expense line is associated.|
    |Rate type|The rate type that is considered during the expense line generation. This field is read-only.|
    |Source ID|The identification number of the item associated with the expense line. If this field is filled in, corresponding information is automatically added to the **Source** fields on this form.|
    |Amount|The monetary value of the item specified in the **Source ID** field. Enter a negative value to indicate a credit.|
    |Process date|The date the expense line is processed.|
    |Inherited|Check box that indicates whether the expense line is on another expense line.|
    |State|The current state of the expense line, either **Pending** or **Processed**.|
    |Summary type|The expense line category: **Grow Business**, **Run Business**, or **Transform Business**. Categorizing expense lines can be useful for reporting.|
    |Short description|A brief description of the expense line.|
    |Asset|The identification number of the asset associated with the expense line, if any.|
    |Fixed asset|Fixed asset that contains the asset in this expense line. A fixed asset is a container that holds one or more individual assets, including hardware or software assets. The system auto-populates this field with the appropriate fixed asset if the named **Asset** is contained within that fixed asset.|
    |Contract|The identification number \(not the contract number\) of the contract associated with the **Asset**, if any.|
    |User|The name of the user associated with the **Asset**, if any.|
    |Configuration Item|The name of the configuration item associated with the expense line, if any.|
    |Task|The identification number of the task associated with the expense line, if any.|
    |Cost center|The cost center financially responsible for the item identified in **Source ID**, if any.|

5.  Click **Submit** \(core UI\) or **Save** \(Hardware Asset Workspaceand Enterprise Asset Workspace\).


**Parent Topic:**[Create a contract rate card](t_ContractRateCardsAndExpenseLines.md)

**Related topics**  


[Contract Rate Card form](../reference/ContractRateCardForm.md)

[Generating expense lines based on assets or users](t_GenExpnsLinOnAssetsUsers.md)

[View contract expense lines](t_ViewingContractExpenseLines.md)

