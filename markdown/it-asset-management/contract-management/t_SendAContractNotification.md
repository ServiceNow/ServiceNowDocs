---
title: Verify contract administrator assignment for notification
description: An event runs automatically each night to send reminders to contract administrators about contract expiration dates so they can renew or renegotiate the contract. You can verify that the right contract administrator is assigned to the contract.
locale: en-US
release: australia
product: Contract Management
classification: contract-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contracts, Contract Management use, Contract Management, IT Asset Management]
---

# Verify contract administrator assignment for notification

An event runs automatically each night to send reminders to contract administrators about contract expiration dates so they can renew or renegotiate the contract. You can verify that the right contract administrator is assigned to the contract.

## Before you begin

Role required: admin, contract\_manager\(core UI and Hardware Asset Workspace only\), sn\_eam.enterprise\_admin \(Enterprise Asset Workspace only\), or sn\_eam.enterprise\_asset\_manager \(Enterprise Asset Workspace only\)

## About this task

When the contract.expiration event runs on the Contract \[ast.contract\] table each night, an email message is sent to the person identified as the contract administrator. This email is sent at the following times.

-   90 days ahead of the contract expiration date
-   60 days ahead of the contract expiration date
-   30 days ahead of the contract expiration date
-   On the contract expiration date

A user with the admin role can edit the contract.expiration condition check that processes contract notifications.

## Procedure

1.  Open the list of contracts that are used across your deployment.

    -   If you are using the core UI, navigate to **Contract** &gt; **Contracts** &gt; **All**.
    -   If you are using the Hardware Asset Workspace, open the Contract management view and then select the **All contracts** tab.
    -   If you are using the Enterprise Asset Workspace, open the Contract and lease management view and then select the **All contracts** tab.
2.  Select a contract.

3.  Check that the **Contract administrator** field contains the correct name.

    A single name can be specified.


**Parent Topic:**[Contracts](../concept/c_Contracts.md)

**Related topics**  


[Create a contract](t_CreateAContract.md)

[Adjust a contract](t_AdjustAContract.md)

[Send the contract for approval](t_SendTheContractForApproval.md)

[Terms and conditions](../concept/c_TermsAndConditions.md)

[Create a contract rate card](t_ContractRateCardsAndExpenseLines.md)

[Monitor a contract](t_MonitoringContracts.md)

[Condition check definitions](../concept/c_UseConditionCheckDefinitions.md)

[Email and SMS notifications](https://www.servicenow.com/docs/access?context=c_EmailNotifications&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

