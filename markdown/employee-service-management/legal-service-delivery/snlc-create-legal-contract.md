---
title: Create a legal contract intake workflow
description: Create a legal contract intake workflow by creating a record producer and configuring base system settings so users can request the legal department's guidance on legal contracts.
locale: en-US
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create a legal contract intake workflow

Create a legal contract intake workflow by creating a record producer and configuring base system settings so users can request the legal department's guidance on legal contracts.

## Before you begin

Role required: sn\_lg\_cnt.contract\_config, admin

## About this task



-   The legal support for a contract request and amendment requestworks based on a workflow, so you must provide specific information while setting up the intake process.
-   Three record producers are available with the base system, Non-disclosure Agreement, Third-party Contract Review, and Amendment request. You can create a record producer by copying a base system \(OOB\) record producer to reuse its existing configuration settings.
-   To add supporting documents to an own-paper request, include the supporting documents widget in the record producer. For more information, see [Add supporting document widget in own-paper record producer](snlc-add-support-doc-wdgt.md).
-   To add external signatories to an third-party paper request, include the external signatories widget in the record producer. For more information, see [Add external signatories widget in third-party paper record producer](snlc-add-ext-signer-wdgt.md).

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Legal Catalog** &gt; **Record Producers**.

2.  Create a record producer or copy a base system record producer for a new contract type.

    -   To create a record producer, click **New**.

        For more information, see [Create or modify a record producer for legal services through Classic environment](../../legal-request-management/task/create-record-producer-legal-request.md).

    -   To copy a base system record producer, open the record producer and then select **Copy**.

        ![Copy a base system record producer](../../contract-mgmt-pro/image/cmpro-copy-record-producer.png "Copy record producer")

3.  On the record producer form, provide the following specifications for a new contract type.

    1.  In the **Table name** field, select the Legal Contract Request table \[sn\_lg\_ops\_contract\_request\].

        The contract workflow is associated with the Legal Contract Request table.

    2.  Create variables to add fields on the legal intake form.

        1.  In the Variables related list, select **New**.

            For more information on creating variables, see [Create a service catalog variable](https://www.servicenow.com/docs/access?context=t_CreateAVariableForACatalogItem&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

        2.  Map the variable to the corresponding column in the Legal Contract Request \[sn\_lg\_ops\_contract\_request\] table.
    3.  If the intake form requires user input for the type of contract, in the Variables related list, select **New**, and then add a variable of type Reference.

        Map the variable to the Contract type table \[sn\_cm\_core\_contract\_type\] in the **Type Specifications** tab.

    4.  If the contract requires the signature of outside parties, in the Variable Sets related list, select **Edit**, and then add the **External signatory details** variable set.

    5.  If you want to validate the state of contract type and restrict creation of a legal request for the inactive contract type on submission of the legal request, add the **Verify if Contract type is active** script from the base system non-disclosure agreement record producer to the new record producer.

        For more information on adding a catalog client script, see [Create a Service Catalog client script](https://www.servicenow.com/docs/access?context=t_CreateACatalogClientScript&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

        **Note:** If you don't add this script in the new record producer, the legal request with the corresponding record producer will be created in the Cancelled state and the contract request won't be created.

4.  Add an intake form in the Contracts practice area.

    For more information, see [Add an intake form to a practice area](../../legal-request-management/task/associate-categories-practice-area.md). Provide the following details in the respective fields.

    1.  From the **Type** drop-down list, select **Request**.

    2.  In the **Options** field, select **Assigned To field not mandatory**.

    3.  For the third-party contract intake form, the **Generate Document from Template** option must not be enabled.

    4.  For an Amendment intake form, the **Amendment request indicator** option must be enabled.

    5.  From the **Request record producer** field, select the record producer created in Step 1 to associate with the intake form.

5.  Modify business rule to enable data synchronization for custom intake forms.

    For more information, see [Configure a practice area table](../../legal-request-management/task/configure-pa-tables-for-reporting.md).

6.  For Non-disclosure agreement intake form that use own-papers, create a contract template.

    For more information, see [Create a contract template](../../contract-mgmt-pro/task/cncore-create-contract-template.md).

    In the **Conditions**, you must select the new category added for the new contract.

7.  For Non-disclosure agreement intake form that use own-papers, configure contract template rules when a legal contract request is being created by a legal user.

    For more information, see [Configure contract template rules](../../contract-mgmt-pro/task/cncore-config-template-rules.md).

8.  Configure the settings in the Standard Ticket Page for legal requests.

    **Note:** The following settings must be updated in the Contract Management Pro for Legal Service Delivery application scope.

    1.  Navigate to **Standard Ticket** &gt; **Standard Ticket Configuration**.

    2.  Select the **sn\_lg\_ops\_request** ticket configuration.

    3.  On the Ticket Configuration form, select **Documents** in the Tab Configuration related list.

    4.  On the Tab Configuration form, add the condition **\[Category\]\[is\]\[&lt;CategoryName&gt;\]** in the **Visible** field, where &lt;CategoryName&gt; is the category created for the new contract.

    5.  Select **Update**.

    6.  Repeat steps for the **Preview** tab configuration.

    For more information, see [Configure the standard ticket page](https://www.servicenow.com/docs/access?context=configure-st-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).


