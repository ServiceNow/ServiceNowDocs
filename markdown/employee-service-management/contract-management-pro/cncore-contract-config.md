---
title: Create a contract configuration
description: Define the contract repository where the contracts will be stored and map the data to be added to the contract or amendment document.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Create a contract configuration

Define the contract repository where the contracts will be stored and map the data to be added to the contract or amendment document.

## Before you begin

A contract template and a template rule that will pick the template when the user submits a contract or amendment request must exist. For more information, see [Configure templates for a contract and amendment request in Contract Management Pro](../concept/cncore-document-templates.md) and [Configure contract template rules](cncore-config-template-rules.md).

You can distinguish configurations for an amendment request from those for a new contract by using the **Request type** selection.

If you want the variables related to the contract request to be available in condition builder, add the contract request reference to your application table. For more information, see [Enable contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

For a request:

-   The fields mapped in the contract configuration determine which values will be updated in the contract document.
-   For a contract request, a new contract repository record is created. According to field and variables mapping, the values are populated into the contract document.
-   For an amendment request, a new contract repository record isn’t created. Instead, the existing record is updated by overriding values for fields and variables that have a defined mapping. If a mapping doesn’t exist for a specific field, its value remains unchanged. For example, to update the contract end date through an amendment, the mapping for the end date field must exist.

    If you want to copy fields with empty values and override existing values in the contract document, select the **Allow empty value flag** when configuring the mappings.![Set the flag Allow empty value for copying empty values](../image/cncore-amend-allow-empty-value.png)


Role required: sn\_cm\_core.contract\_config

## About this task

To add data to the contract documents, you have to map request table fields to repository fields.

**Note:**

Third party contracts already have a default contract configuration in the base system.

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Configuration**.

2.  Select **New**.

3.  On the Contract Configuration form, fill in the fields.

    For more information, see [Contract Configuration form](../reference/cncore-contract-config-form.md).

4.  Select **Save**.

5.  In the Contract Repository Mappings related list, select **New**.

    ![Contract configuration with repository mapping](../image/cmpro-contract-conf.png "Contract configuration")

6.  In the **Mapping type**, select the type of mapping you want to do.

    The fields on the form change depending on the selection.

<table id="choicetable_grz_dw5_yxb"><thead><tr><th align="left" id="d83300e214">

Mapping type

</th><th align="left" id="d83300e217">

Fields available

</th></tr></thead><tbody><tr><td id="d83300e223">

**Field mapping - Map fields from the request table to the fields in the contract repository table.**

</td><td>

-   **Request table**- Table to which you want to associate the contract configuration.
-   **Map from field**- Field of the request table that you want to map to the **Map to field**, a field in the contract repository.
-   **Active** - Option to indicate that contract repository mapping is active.
-   **Contract repository** - This field is automatically set to the configuration repository set in the **Contract repository** field.
-   **Allow empty value** - Option to enable copying of empty values to contract repository and override the existing value.

**Note:** This option is available only when the **Request type** is set to Amendment in the contract configuration and it isn’t selected by default.

</td></tr><tr><td id="d83300e271">

**Template mapping- Map the template mappings of a contract template to the fields in the contract repository.**

</td><td>

-   **Template** - This field is automatically set to the template for which you’re creating the repository mapping.
-   **Template mapping** - The field from the template that you want to map to the **Map to field** value, a field in the contract repository.
-   **Active** - Option to indicate that the contract repository mapping is active.
-   **Allow empty value** - Option to enable copying of empty values to contract repository and override the existing value.

**Note:** This option is available only when the **Request type** is set to Amendment in the contract configuration and it isn’t selected by default.

</td></tr><tr><td id="d83300e311">

**Template mapping- Map variables of record producer to the fields in the contract repository table.**

</td><td>

-   **Record producer**- The record producer from which you want to copy the variable. For example, If you want to copy a variable from a contract request for Non-disclosure Agreement, select record producer for a Non-disclosure Agreement.
-   **Variable**- The variable of the record producer that you want to map to a field in the contract repository.
-   **Active**- Option to indicate that the contract repository mapping is active.
-   **Map to field**- The field to which you want to map the variable from the record producer.
-   **Allow empty value** - Option to enable copying of empty values to contract repository and override the existing value.

**Note:** This option is available only when the **Request type** is set to Amendment in the contract configuration and it isn’t selected by default.

</td></tr></tbody>
</table>7.  Select **Submit** to save the repository mapping.

8.  Select **Update** to save the contract configuration.


