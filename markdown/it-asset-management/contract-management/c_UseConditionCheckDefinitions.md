---
title: Condition check definitions
description: Condition check definitions enable you to define logical conditions that indicate when to change a field value in a record.
locale: en-US
release: xanadu
product: Contract Management
classification: contract-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Contract Management, IT Asset Management]
---

# Condition check definitions

Condition check definitions enable you to define logical conditions that indicate when to change a field value in a record.

A scheduled job, called **Contract Compliance Checks** in **System Scheduler** &gt; **Scheduled Jobs**, evaluates these condition check definitions daily by running the condition checker. When this job is run, the ConditionChecks Script Include is triggered that runs the Condition Check Definitions. Use this condition checker to check start dates and end dates and to set expiration levels for contracts.

For example, a contract has a start date of March 1. When the condition checker runs on March 1, it verifies that the contract **Substate** is **Approved** and sets the contract **State** to **Active** based on the **Start Date** field.

The daily condition checker sets the appropriate expiration level for active contracts based on the contract **End Date**. The expiration level can be viewed in the Contracts list. Knowing the expiration level can help contract managers renew or extend a contract before it expires.

-   **[Define a condition check](../task/t_DefineAConditionCheck.md)**  
You can define a condition check to change values in a contract when the **Contract Compliance Checks** scheduled job runs each night.

**Parent Topic:**[Contract Management](c_ContractManagement.md)

**Related topics**  


[Use the Asset Contract Overview module](../task/t_UseTheContractMgmtOverviewModule.md)

[Components installed with Contract Management](../reference/r_ComponentsInstalledWContractMgmt.md)

[Contract Management use](c_UseContractManagement.md)

[Domain separation and Contract Management](domain-separation-contract-mgmt.md)

