---
title: Complete clause mapping to build a clause library
description: As a contract configurator, complete clause mapping to build a clause library of clause variations containing the content marked in the Microsoft Word document using the Microsoft Word Add-in for ServiceNow Contracts.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Creating a contract template using Microsoft Word add-in for ServiceNow Contracts, Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Complete clause mapping to build a clause library

As a contract configurator, complete clause mapping to build a clause library of clause variations containing the content marked in the Microsoft Word document using the Microsoft Word Add-in for ServiceNow Contracts.

## Before you begin

-   Ensure that the application scope is set to **Global**. Otherwise, do the following:
    1.  Select the Application scope icon \(![Application scope icon](../../workplace-calendar-synchronization/image/application-scope-globe-icon.png)\) on the top-right corner.
    2.  In the drop- down, select the option consisting **Application scope**.
    3.  In the filter navigator, search and select **Global**.
-   Map clause and clause variations in the Microsoft Word document using the Microsoft Word Add-in for ServiceNow Contracts. For more information, see [Map clauses and clause variations using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-add-clauses.md)
-   Upload and parse the document with the content controls. For more information, see [Upload and parse a Microsoft Word document that includes content controls](cncore-upload-doc-addin.md).

Role required: sn\_cm\_core.contract\_config

## About this task

Clauses that are imported from the Microsoft Word document are used to build a clause library of clause variations.

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Templates**.

2.  From the list, open the contract template for which you want to complete the clause mapping.

3.  Navigate to the Imported clauses related list.

4.  Select **Complete Clause Mapping**.

    -   If the mapping is successful, the Clause Mappings related list displays the details of mapped clauses with their contract type.
    -   If the mapping is not successful, an error message appears. Possible causes could include:
        -   No contract type was selected.
        -   All clauses were not assigned a classification.
        -   Clauses classified as New clause were mapped to a clause instead of being empty.
        -   Clauses classified as Existing clause or No change don’t have a clause mapped to them.
5.  Select **Update** to save the contract template.

6.  View the clause variations associated with a clause by selecting the Display/hide hierarchical lists icon \(![Display/hide hierarchical lists](../image/lsd-icon-hirerachy-lists.png)\) for the clause.


**Parent Topic:**[Creating a contract template using Microsoft Word add-in for ServiceNow Contracts](../concept/cncore-setup-ct-add-in.md)

**Related topics**  


[Create a contract template to contain content controls](cncore-create-ct-word-addin.md)

[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

[Upload and parse a Microsoft Word document that includes content controls](cncore-upload-doc-addin.md)

[Add conditions for a contract table mapping](cncore-add-filter-table-map.md)

