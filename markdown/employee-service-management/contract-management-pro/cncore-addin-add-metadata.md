---
title: Configure metadata for fields, variables, and variables sets in a contract document
description: As a contract configurator, add and configure metadata for fields, variable, and variable sets to pre-fill the information in the contract document.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Add document content controls using Microsoft Word add-in for ServiceNow Contracts, Creating a contract template using Microsoft Word add-in for ServiceNow Contracts, Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure metadata for fields, variables, and variables sets in a contract document

As a contract configurator, add and configure metadata for fields, variable, and variable sets to pre-fill the information in the contract document.

## Before you begin

The Microsoft Word add-in for ServiceNow Contracts must have been configured. For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md).

A contract template must exist that is active and is in the Draft or Editing state. For more information, see [Create a contract template to contain content controls](cncore-create-ct-word-addin.md).

Role required: sn\_cm\_core.contract\_config and canvas\_user

## About this task

The metadata added for fields, variable, and variable sets act as placeholders for values that will be used in the contract document.

**Note:** In Contract Management Pro version 1.4.1, the Legal Contract Request form in Legal Counsel Center and Contract Workspace displays only mapped legal fields for variables in the contract fulfiller view. You therefore need to apply the **Field mapping** option when setting up Metadata mapping for legal contracts. For existing templates with Variable mapping, edit the template and update the configuration with **Field mapping**.

For more information on editing a contract template, see [Edit a contract template using Microsoft Word add-in for ServiceNow Contracts](cncore-edit-ct-addin.md).

-   The metadata of the type Field mapping gets its value from the table that the contract template is associated with.
-   The metadata of type Variables gets its value from the record producer.

## Procedure

1.  Open the document in which you want to mark the content controls in Microsoft Word.

2.  From the Microsoft Word ribbon, select the ServiceNow Contracts add-in.

3.  On the login screen, enter the credentials of the ServiceNow instance for which the Microsoft Word add-in is configured.

    For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md)

4.  On the add-in screen in the **Templates** tab, select the contract template to which you want to add the metadata.

    Only templates that have been created in the global application scope are visible.

5.  In the Microsoft Word document, place the cursor where you want to add the placeholder for metadata.

6.  In the **Metadata** tab, select **Create metadata mapping**.

7.  On the Create mapping form in the **Type** field, select either field mapping or variables.

<table id="choicetable_qfz_dkb_yyb"><thead><tr><th align="left" id="d188262e239">

Type of metadata

</th><th align="left" id="d188262e242">

Fields available

</th></tr></thead><tbody><tr><td id="d188262e248">

**Field mapping**

</td><td>

-   **Mapping field**- Fields of the table to which the contract template is associated.
-   **Field Name**- The field is automatically set to the value of the **Mapping Field**. You can also modify the value.


</td></tr><tr><td id="d188262e273">

**Variables**

</td><td>

**Note:** If a fulfiller updates the legal fields in a contract request and the template of the contract request uses variable mapping, the contract document will not be updated with the new values when you create a contract revision.

 -   **Record producer**- The record producer from which you want to add the variable. For example, if you want to add a variable from a contract request for a non-disclosure agreement, select the record producer for a non-disclosure agreement.
-   **Variable**- The variable of the record producer that you want to add.
-   **Variable set row**- The row value of the variable set. The field is displayed only when the selected value in **Variable** is a set of values.

For example, the Signatory variable is a set of variables for Title, Name, and email address. You can visualize this data set in rows and columns.

![Signatory variables](../image/lsd-addin-variableset-example.png)

If you wanted to map the variable to Beth Anglin, you would enter `Row2` as the value in the **Variable set row** field.

-   **Field Name**- This field is automatically populated depending on the values for **Variable** and **Variable set row**. You can also modify the value. The maximum character limit for the field name is 200.

**Note:**

Validation errors might occur for the following reasons:

    -   The field name is not unique.
    -   You have mapped metadata to a field that has already been mapped.


</td></tr></tbody>
</table>8.  Select **Create**.

    -   The metadata is added and displayed as a tile with the field name as the title.

        ![Metadata added using the add-in](../image/ccore-metadata-tile.png)

    -   The metadata is synced to the ServiceNow instance.
    **Note:**

    If you have included the sys\_id variable, you must adjust this script to display it correctly. For more information, see [Configure fields in contract template to display correct sys\_id value in contract documents](cncore-addin-adv-script.md).

9.  Add the metadata to other locations in the document or the header or footer of the Word document by selecting the tile and moving it to the desired location.

10. View the metadata by logging in to your ServiceNow instance and navigating to the **Template Mappings** related list of the contract template.


**Parent Topic:**[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

**Related topics**  


[Configuring signatories in Contract template using Microsoft Word add-in](../concept/cncore-config-sign-addin.md)

[Map clauses and clause variations using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-add-clauses.md)

[Map contract document tables using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-table.md)

