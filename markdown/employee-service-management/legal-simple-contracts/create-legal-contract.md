---
title: Create a legal contract intake workflow
description: Create a legal contract intake workflow by creating a record producer and configuring base system settings so that employees can request the legal department's guidance on legal contracts.
locale: en-US
release: zurich
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create a legal contract intake workflow

Create a legal contract intake workflow by creating a record producer and configuring base system settings so that employees can request the legal department's guidance on legal contracts.

## Before you begin

Role required: sn\_lg\_contracts.contracts\_config, admin

## About this task

The legal support for a contract request works based on a workflow, so you must provide specific information while setting up the intake process.

## Procedure

1.  Create a record producer for a new contract type.

    For more information, see [Create or modify a record producer for legal services through Classic environment](../../legal-request-management/task/create-record-producer-legal-request.md). On the form, you must provide the following specifications in the record producer for a new contract type:

    1.  In the **Table name** field, select the General Contract Support \[sn\_lg\_ops\_general\_contract\_support\] table.

        The contract workflow is associated with the General Contract Support table.

    2.  Set the **contract\_type** field to a contract type name such as `NDA`, `MSA`, or `SOW`, if you wish to set up the intake form to select specific contract type.

        For example, to set the contact type to NDA, enter the following code:

        ```
        current.contract_type = 1;
        ```

    3.  If the contract requires the signature of outside parties, in the Variable Sets related list, click **Edit** and add the **External signatory details** variable set.

2.  Add a new intake form in the Contracts practice area.

    For more information, see [Add an intake form to a practice area](../../legal-request-management/task/associate-categories-practice-area.md). Ensure to provide the following details in the respective fields.

    1.  From the **Type** drop-down list, select **Request**.

    2.  In the **Options** field, select **Assigned To field not mandatory**.

    3.  For third-party contract intake form, the **Generate Document from Template** option must not be enabled.

    4.  From the **Request record producer** field, select the record producer created in the Step 1 to associate with the intake form.

3.  Create legal contract templates.

    -   For more information, see [Legal contract templates](../concept/document-template-block.md).
    -   In the **Conditions**, you must select the new category added for the new contract.
4.  [Configure a rule for selecting a legal contract template](configure-legal-contract-template-rules.md) when a legal contract request is being created by a user.

5.  Configure the settings in the Standard Ticket Page for legal requests.

    **Note:** The following settings must be updated in the Legal Simple Contracts application scope.

    1.  Navigate to **Standard Ticket** &gt; **Standard Ticket Configuration**.

    2.  Select the **sn\_lg\_ops\_request** ticket configuration.

    3.  On the Ticket Configuration form, select **Documents** in the Tab Configuration related list.

    4.  On the Tab Configuration form, add the condition **\[Category\]\[is\]\[&lt;CategoryName&gt;\]** in the **Visible** field, where &lt;CategoryName&gt; is the category created for the new contract.

    5.  Click **Update**.

    6.  Repeat steps 5c-5e for the **Preview** tab configuration.

    For more information, see [Configure the standard ticket page](https://www.servicenow.com/docs/access?context=configure-st-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)


