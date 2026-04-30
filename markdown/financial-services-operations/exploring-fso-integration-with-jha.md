---
title: Exploring the Financial Services Operations Integration with Jack Henry jXchange
description: The Financial Services Operations Integration with Jack Henry jXchange application enables your agents to access the required system of record information so they can look up and verify your customer's financial and account information quickly. This integration also enables your organization to convert your end-to-end digital financial service processes.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Jack Henry jXchange, Integrate, Financial Services Operations \(FSO\)]
---

# Exploring the Financial Services Operations Integration with Jack Henry jXchange

The Financial Services Operations Integration with Jack Henry jXchange application enables your agents to access the required system of record information so they can look up and verify your customer's financial and account information quickly. This integration also enables your organization to convert your end-to-end digital financial service processes.

## Architectural overview

The following diagram is a high-level overview of the design of the Jack Henry jXchange integration and the role that each layer plays in Financial Services Operations \(FSO\). The table that follows the diagram describes the different layers.

![Diagram of a high-level overview of the design of the JHA integration and the role each layer plays in Financial Services Operations applications. For description of the layers, refer to the following table.](../image/jha-thirdparty-integ.png "Financial Services Operations Integration with Jack Henry jXchange")

<table id="table_nwm_zkl_15b"><thead><tr><th>

Layer

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Industry Workflow/FSO Layer

</td><td>

Layer that includes the Financial Services Operations application.

</td></tr><tr><td>

Integration Layer

</td><td>

Layer that helps to integrate with the Financial Services Operations application and stores information to the data model. This layer provides the following components:-   End-to-end integration of the FSO layer and spoke layer.
-   Subflows that consume the actions in the Jack Henry jXchange spoke. Each action has both individual subflows and combined subflows to call all the actions together. The combined subflows are as follows:
    -   Look up customer data adpr
    -   Look up customer info adpr
    -   Look up financial accounts for a customer adpr
    -   Look up financial transactions adpr
-   Subflow that can be called from the flow by passing the financial account and account type as an input to look up the customer's details and financial account details.

</td></tr><tr><td>

Spoke Layer

</td><td>

Layer that includes the Jack Henry jXchange spoke plugin. This layer provides the actions that use REST Web Services to interact with the Jack Henry jXchange APIs. The Jack Henry jXchange spoke actions are as follows:-   Look up Customers Information Stream
-   Look up Customer Information by ID
-   Look up Financial Accounts Stream
-   Look up Financial Account by Account Details
-   Look up Financial Transactions Stream

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations Integration with Jack Henry jXchange](fso-integration-with-jha-integthub-landing-page.md)

