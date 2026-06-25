---
title: Monitor a contract
description: You can monitor contracts by viewing contract history and creating contract reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/contract-management/t\_MonitoringContracts.html
release: australia
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Contracts, Contract Management use, Contract Management, Asset Management, IT Service Management]
---

# Monitor a contract

You can monitor contracts by viewing contract history and creating contract reports.

## Before you begin

Role required: asset, contract\_manager\(core UI and Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## About this task

If changes are made to a contract start date, end date, or terms and conditions, a copy of the contract is automatically saved and placed in contract history. This is useful for tracking changes to a contract and keeping an audit trail. Configure the **Contract History** related list or tab to include columns for creation and update so you can easily see who edited the contract.

## Procedure

1.  Open the list of contracts that are used across your deployment.

    -   If you are using the core UI, navigate to **Contract** &gt; **Contracts** &gt; **All**.
    -   If you are using the Hardware Asset Workspace, open the Contract management view and then select the **All contracts** tab.
    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view and then select the **All contracts** tab.
2.  Select a contract.

3.  View the **Contract History** related list \(core UI\) or tab \(Hardware Asset Workspaceand Enterprise Asset Workspace\) and perform one of the following actions.

    -   If earlier versions of the contract exist, click a date in the **Contract Starts** column to view a version.
    -   If an earlier version of the contract does not exist, change the contract's **Start date** or **End date**. Right-click in the header bar and select **Save**. In the **Contract History** related list, click a date in the **Contract Starts** column to view the earlier version.

-   **[Run a contract report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/contract-management/t_CreatingContractReports.md)**  
A variety of contract reports are available to help track and manage contracts.

**Parent Topic:**[Contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/contract-management/c_Contracts.md)

**Related topics**  


[Create a contract]()

[Adjust a contract]()

[Verify contract administrator assignment for notification]()

[Send the contract for approval]()

[Terms and conditions]()

[Create a contract rate card]()

