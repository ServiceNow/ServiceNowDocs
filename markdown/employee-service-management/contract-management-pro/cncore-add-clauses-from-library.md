---
title: Add clauses during authoring or negotiation
description: As a contract fulfiller or reviewer, while authoring or negotiating a contract revision, add clauses from the clause library listed in the Microsoft Word add-in for ServiceNow Contracts.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Add clauses during authoring or negotiation

As a contract fulfiller or reviewer, while authoring or negotiating a contract revision, add clauses from the clause library listed in the Microsoft Word add-in for ServiceNow Contracts.

## Before you begin

Role required: sn\_cm\_core.contract\_fulfiller or sn\_cm\_core.contract\_reviewer

## About this task

When working on own-paper or third party paper based contract document, you can use the clause library to check the document for missing or non-compliant clauses. You can also add clause content from the clause library to the document.

The clause library is available under the following conditions:

-   The contract request is in Work in progress state. You are assigned to this request, or you are a group manager or collaborator.
-   The contract request is in Awaiting review state. You are assigned the internal review task as a contract reviewer.

## Procedure

1.  Open the Microsoft Word document that is under review or negotiation.

2.  From the Microsoft Word ribbon, select ServiceNow Contracts add-in.

3.  On the add-in login screen, enter the credentials of the ServiceNow instance from where you downloaded the manifest file.

    For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md)

4.  Select the **Clause library** tab.

5.  Search the clause by using the clause name.

    Active clauses for the contract type that is associated with the contract document is displayed.

6.  Select the clause in the library.

7.  Select the content in the document where you want to add the clause.

8.  Select **Use this clause** for a specific clause that is applicable.

    The clause is added to the document. When a valid metadata mapping exists within clause content, the metadata gets auto-populated. Otherwise, a content control tag name is added and the metadata has to be manually updated. For more information, see [Configure metadata for fields, variables, and variables sets in a contract document](cncore-addin-add-metadata.md).


**Parent Topic:**[Using Contract Management Pro](../concept/cncore-use-cmpro.md)

