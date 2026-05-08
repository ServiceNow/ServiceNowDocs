---
title: Map clauses and clause variations using the Microsoft Word add-in for ServiceNow Contracts
description: As a contract configurator, add clause and clause variations to a contract using the Microsoft Word add-in for ServiceNow Contracts.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Add content controls, Create templates in Microsoft Word, Configure contract templates, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Map clauses and clause variations using the Microsoft Word add-in for ServiceNow Contracts

As a contract configurator, add clause and clause variations to a contract using the Microsoft Word add-in for ServiceNow Contracts.

## About this task

The following video walks you through the process of mapping clause and clause variations using Microsoft Word add-in for ServiceNow Contracts.

The following video walks you through the process of mapping clause and clause variations using Microsoft Word add-in for ServiceNow Contracts. 

## Before you begin

The Microsoft Word add-in for ServiceNow Contracts must have been configured. For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md).

An active contract template in the Draft or Editing state must exist. For more information, see [Create a contract template to contain content controls](cncore-create-ct-word-addin.md).

Role required: sn\_cm\_core.contract\_config and canvas\_user

## Procedure

1.  Open the document in which you want to mark the content controls in Microsoft Word.

2.  From the Microsoft Word ribbon, select the ServiceNow Contracts add-in.

3.  In the login screen, enter the credentials of the ServiceNow instance from which you downloaded the manifest file.

    For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md)

4.  In the **Templates** tab, select the contract template for which you want to add or modify clauses.

5.  Navigate to the **Clauses** tab.

    A list of active clauses associated with the table selected in the contract template is displayed.

6.  On the Microsoft Word Home ribbon, select the Show/Hide formatting marks icon \(![Show/Hide formatting marks icon](../image/lsd-word-formatting-icon.png)\) to see the formatting symbols.

7.  In the Microsoft Word document, select the content to be tagged along with the paragraph ending symbol \(![Paragraph ending symbol](../image/lsd-word-formatting-icon.png)\).

8.  Map the content to the clauses by either using an existing clause variation, creating a clause, or creating clause variation.

    A clause cannot be mapped to more than one piece of content.

    ![Map clauses in ServiceNow Contracts add-in](../image/cmpro-waddin-use-clause.png "Clause mapping")

<table id="choicetable_j14_bd2_2yb"><thead><tr><th align="left" id="d144866e247">

Methods for content and clause mapping

</th><th align="left" id="d144866e250">

Steps

</th></tr></thead><tbody><tr><td id="d144866e256">

**Use the clause as it is and do not update any of the existing clauses or clause variation**

</td><td>

In the **Clauses** tab, select **Use this clause** for the clause that you want to use.**Note:** The imported clause is classified as No Change in the ServiceNow instance.

</td></tr><tr><td id="d144866e276">

**Create a clause and do not create any clause variation**

</td><td>

1.  In the **Clauses** tab, select the Create a new clause icon \(![Create new clause icon](../image/lsd-plus-symbol-addin.png)\).
2.  In the New clause form, fill in the fields.
    -   **Name** - Unique name for the clause.
    -   **Contract type** - This field is automatically set to the contract type associated with the contract template.

**Note:** If the contract type associated with the template is deactivated, the **Contract type** field will be empty. You will be able to select only active contract type in the field.

    -   **Description** - Information about the clause.
3.  Select **Create**.

**Note:**

    -   You can manually add more contract types.
    -   No clause variations are created.
    -   The imported clause is classified as Existing Clause in the ServiceNow instance.


</td></tr><tr><td id="d144866e349">

**Create a clause variation for an existing clause**

</td><td>

In the **Clauses** tab, select **Create Variation** for the clause that you want to use. The imported clause is classified as Existing Clause in the ServiceNow instance.

</td></tr></tbody>
</table>9.  Select the **View mapped clauses** toggle switch to see the mapped clauses.


## Result

-   The selected content is tagged with the clause.
-   The clause details are synced to the ServiceNow instance. You can access the clause details by logging to the ServiceNow instance and navigating to the **Imported Clauses** related list of the contract template.![Mapped clauses added from ServiceNow Contracts add-in are synced to your instance](../image/cmpro-waddin-view-mapped-cls.png)

## What to do next

[Complete mapping and upload Microsoft Word document that includes content controls](cncore-upload-doc-addin.md)

**Parent Topic:**[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

**Related topics**  


[Configure metadata for fields, variables, and variables sets in a contract document](cncore-addin-add-metadata.md)

[Configuring signatories in Contract template using Microsoft Word add-in](../concept/cncore-config-sign-addin.md)

[Map contract tables using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-table.md)

