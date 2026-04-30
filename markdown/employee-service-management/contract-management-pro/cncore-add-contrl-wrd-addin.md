---
title: Add document content controls using Microsoft Word add-in for ServiceNow Contracts
description: Add content controls using the Microsoft Word add-in for ServiceNow Contracts. Content controls act as placeholders in contract templates.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Creating a contract template using Microsoft Word add-in for ServiceNow Contracts, Configure contract templates, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Add document content controls using Microsoft Word add-in for ServiceNow Contracts

Add content controls using the Microsoft Word add-in for ServiceNow Contracts. Content controls act as placeholders in contract templates.

The Microsoft Word add-in for ServiceNow Contracts enables you to add content controls for metadata, signatories, clauses, and table into the contract document from the following tabs.

-   Metadata: View and add metadata for fields, variable, and variable sets to pre-fill the information in the contract document.
-   Signatory: View and add signatories to add their signatures in the contract document.
-   Clauses: View and add clause and clause variations to a contract document.
-   Table: Determine the data that will be added from a data source table in your ServiceNow instance to a table in a contract document![The image shows the components of the Microsoft Word add-in for ServiceNow Contracts](../image/cmpro-word-addin-view.png)

You can also switch application scope and log out using the following options:

-   Switch scope icon: Use the switch scope icon \(![Switch scope icon](../image/cmpro-addin-scope.png)\) to set the correct scope to enable editing of the contract template. This icon is active when you select a contract template for editing and also have an admin role.
-   Logout icon: Use Logout icon \(![Logout icon](../image/cmpro-addin-logout.png)\) to log out from Microsoft Word add-in for ServiceNow Contracts.

    **Note:** If you are directed to platform page instead of Word Add-in page when you re-login, follow the steps mentioned in [this KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2025171) to resolve the issue.


-   **[Configure metadata for fields, variables, and variables sets in a contract document](cncore-addin-add-metadata.md)**  
As a contract configurator, add and configure metadata for fields, variable, and variable sets to pre-fill the information in the contract document.
-   **[Configuring signatories in Contract template using Microsoft Word add-in](../concept/cncore-config-sign-addin.md)**  
For signatories to add their signatures in the contract document, you can either create signature blocks or configure participants in a contract template with placeholders.
-   **[Map clauses and clause variations using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-add-clauses.md)**  
As a contract configurator, add clause and clause variations to a contract using the Microsoft Word add-in for ServiceNow Contracts.
-   **[Map contract tables using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-table.md)**  
Use the Microsoft Word add-in to map a contract table to a source table in your ServiceNow instance to determine the data that will be added in a contract document. When a contract document is generated from the template, the rows and columns are dynamically added in the mapped table of the contract document.

**Parent Topic:**[Creating a contract template using Microsoft Word add-in for ServiceNow Contracts](../concept/cncore-setup-ct-add-in.md)

**Related topics**  


[Create a contract template to contain content controls](cncore-create-ct-word-addin.md)

[Upload and parse a Microsoft Word document that includes content controls](cncore-upload-doc-addin.md)

[Complete clause mapping to build a clause library](cncore-clause-map-addin.md)

