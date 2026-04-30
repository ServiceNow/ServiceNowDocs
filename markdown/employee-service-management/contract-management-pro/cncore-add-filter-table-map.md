---
title: Add conditions for a contract table mapping
description: As a contract configurator, use condition builders to define criteria for a table mapping for a contract template so only the essential data from the mapped table is displayed in the contract document.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Creating a contract template using Microsoft Word add-in for ServiceNow Contracts, Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Add conditions for a contract table mapping

As a contract configurator, use condition builders to define criteria for a table mapping for a contract template so only the essential data from the mapped table is displayed in the contract document.

## Before you begin

-   Map tables in Microsoft Word document using the Microsoft Word add-in for ServiceNow Contracts. For more information, see [Map contract document tables using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-table.md).
-   Upload and parse the document with the content controls. For more information, see [Upload and parse a Microsoft Word document that includes content controls](cncore-upload-doc-addin.md).
-   Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Templates**.

2.  From the list, open the contract template for which you want to add table mapping conditions.

3.  Select the **Table Mappings** tab under **Related Links**.

4.  Select the table mapping.

5.  In the **Condition** field, define a condition for the table mapping.

    For more information, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

6.  Select **Update**.


**Parent Topic:**[Creating a contract template using Microsoft Word add-in for ServiceNow Contracts](../concept/cncore-setup-ct-add-in.md)

**Related topics**  


[Create a contract template to contain content controls](cncore-create-ct-word-addin.md)

[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

[Upload and parse a Microsoft Word document that includes content controls](cncore-upload-doc-addin.md)

[Complete clause mapping to build a clause library](cncore-clause-map-addin.md)

