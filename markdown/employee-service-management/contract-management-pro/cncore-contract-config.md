---
title: Create a contract configuration
description: Define the contract repository where the contracts will be stored and map the data to be added to the contract document.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Create a contract configuration

Define the contract repository where the contracts will be stored and map the data to be added to the contract document.

## Before you begin

A contract template and a template rule that will pick the template when the user submits a contract request must exist. For more information, see [Configure contract templates for a contract request](../concept/cncore-document-templates.md) and [Configure contract template rules](cncore-config-template-rules.md).

If you want the variables related to contract request to be available in condition builder, add the contract request reference to your application table. For more information, see [Provide access to contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

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

6.  In the **Mapping type**, select the type of mapping you want to do.

    The fields on the form change depending on the selection.

<table id="choicetable_grz_dw5_yxb"><thead><tr><th align="left" id="d74403e193">

Mapping type

</th><th align="left" id="d74403e196">

Fields available

</th></tr></thead><tbody><tr><td id="d74403e202">

**Field mapping - Map fields from the request table to the fields in the contract repository table.**

</td><td>

-   **Request table**- Table to which you want to associate the contract configuration.
-   **Map from field**- Field of the request table that you want to map to the **Map to field**, a field in the contract repository.
-   **Active** - Option to indicate that contract repository mapping is active.
-   **Contract repository** - This field is automatically set to the configuration repository set in the **Contract repository** field.


</td></tr><tr><td id="d74403e247">

**Template mapping- Map the template mappings of a contract template to the fields in the contract repository.**

</td><td>

-   **Template** - This field is automatically set to the template for which you are creating the repository mapping.
-   **Template mapping** - The field from the template that you want to map to the **Map to field** value, a field in the contract repository.
-   **Active** - Option to indicate that the contract repository mapping is active.


</td></tr><tr><td id="d74403e280">

**Template mapping- Map fields of record producer to the fields in the contract repository table.**

</td><td>

-   **Record producer**- The record producer from which you want to copy the variable. For example, If you want to copy a variable from a contract request for Non-disclosure Agreement, select record producer for a Non-disclosure Agreement.
-   **Variable**- The variable of the record producer that you want to map to a field in the contract repository.
-   **Active**- Option to indicate that the contract repository mapping is active.
-   **Map to field**- The field to which you want to map the variable from the record producer.


</td></tr></tbody>
</table>7.  Select **Submit** to save the repository mapping.

8.  Select **Update** to save the contract configuration.


