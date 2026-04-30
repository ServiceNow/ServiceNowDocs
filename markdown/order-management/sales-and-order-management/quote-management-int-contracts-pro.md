---
title: Quote Management integration with Contract Management Pro
description: The Quote Management integration with Contract Management Pro is known as Contract Management for Sales and Order Management \(com.sn\_som\_clm\).
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Quote Management, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Quote Management integration with Contract Management Pro

The Quote Management integration with Contract Management Pro is known as Contract Management for Sales and Order Management \(com.sn\_som\_clm\).

Quote Management integrates with Contract Management Pro to help sales agents create legal sales contracts from a quote. A legal sales contract confirms the sales deal and agreements between your company and customer.

The following roles are required to initiate, view, and manage contract execution:

-   Contract fulfiller: This role is assigned with the **Sales agent** role and it enables sales agents to create contracts and execute the contract workflow.
-   Contract configurator: This role is assigned with **Sales Ops specialist** role and it enables sales ops specialists to configure data required for contract initiation and its related tasks.

A contract generation process consists of the following steps:

-   A sales ops specialist creates a contract type and document template, defines signatory rules, and completes configurations for the contract generation process. To learn more, see [Configuring Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-config-cmpro&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).
-   A sales agent then initiates the contract creation process through the Initiate contract UI action by filling the required details, such as Type of paper, Contract type, Signature type, and Start and End dates.

    -   **Inititate Contract** UI action is visible only when a quote is in Completed state.
    -   After you submit the contract creation form, it creates a contract request record.
    -   The new contract request triggers the workflow to generate the legal sales contract.
    To learn more, see [Initiate a contract request](../task/quote-management-create-contract.md).

-   When the contract workflow is complete, the state of the contract request is changed to Closed complete.

## What to do next

To learn more, see [Integrate with Contract Management Pro](../task/quote-management-integrate-contract-management.md).

