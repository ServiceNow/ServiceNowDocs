---
title: Classify and map imported clauses
description: Classify and map imported clauses to use the content from the clauses in a contract template.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create contract template by manually adding content controls, Configure contract templates, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Classify and map imported clauses

Classify and map imported clauses to use the content from the clauses in a contract template.

## Before you begin

A Microsoft Word document must have been uploaded and parsed to provide clauses for the contract template. For more information, see [Create a contract template](cncore-create-contract-template.md).

Role required: sn\_cm\_core.contract\_config

## About this task

The imported clauses contain content that have been extracted from the Microsoft Word document that are marked by the content controls. Classifying and mapping the imported clauses builds a clause library of clause variations containing the content available in the imported clauses.

For more information on clause variations, see [Create a clause variation](cncore-add-clauses-doc-tmplt.md).

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Templates**.

2.  Open a contract template.

3.  Navigate to the Imported clauses related list.

4.  Either update an existing clause variation with the content available in the imported clause or create a new clause or clause variation with that content.

<table id="choicetable_j14_bd2_2yb"><thead><tr><th align="left" id="d357635e116">

Usage of the imported clause data

</th><th align="left" id="d357635e119">

Steps

</th></tr></thead><tbody><tr><td id="d357635e125">

**Do not update any of the existing clause or clause variation**

</td><td>

1.  In the **Classification** field, select the drop down arrow.
2.  Select **No change** from the list.
3.  In the **Mapping clause** field, select an active clause from the clause library.


</td></tr><tr><td id="d357635e155">

**Create a new clause and its clause variation**

</td><td>

1.  In the **Classification** field, select the drop down arrow.
2.  Select **New Clause** from the list.
3.  In the **Mapping clause** field, do not take any action.


</td></tr><tr><td id="d357635e185">

**Create a new clause variation**

</td><td>

1.  In the **Classification** field, select the drop down arrow.
2.  Select **Existing Clause** from the list.
3.  In the **Mapping clause** field, select an active clause from the clause library.


</td></tr></tbody>
</table>5.  Select **Complete Clause Mapping**.

    ![Classify and map imported clauses](../image/cmpro-complete-mapping.png "Contract document template")

    -   If the mapping is successful, the Clause Mappings related list displays the details of mapped clauses with their contract type.
    -   If the mapping is not successful, an error message appears. Possible causes could include:
        -   No contract type was selected.
        -   All the clauses were not assigned a classification.
        -   Clauses with the classification of New clause were mapped to a clause instead of being empty.
        -   Clauses with the classifications of Existing clause or No change don’t have a clause mapped to them.
6.  View the clause variations associated with a clause by selecting the Display/hide hierarchical lists icon \(![Display/hide hierarchical lists](../image/lsd-icon-hirerachy-lists.png) for a clause.


**Parent Topic:**[Create contract template by manually adding content controls](../concept/cncore-setup-ct-manual.md)

**Related topics**  


[Add content controls in a Microsoft Word document](cncore-word-doc-tmplt-contls.md)

[Create a contract template](cncore-create-contract-template.md)

[Create and configure participants](cncore-add-participants.md)

[Update contract template mappings](cncore-template-mapping.md)

