---
title: Contract Management Pro release notes
description: The ServiceNow Contract Management Pro is a contract lifecycle management solution that's easy to use and adopt. You can use it to set up contract document templates, clauses, clause variations, and to initiate contract requests. It also supports Now Assist driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.Contract Management Pro was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-13"
reading_time_minutes: 7
---

# Contract Management Pro release notes

The ServiceNow® Contract Management Pro is a contract lifecycle management solution that's easy to use and adopt. You can use it to set up contract document templates, clauses, clause variations, and to initiate contract requests. It also supports Now Assist driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.Contract Management Pro was enhanced and updated in the Yokohama release.

## Contract Management Pro highlights for the Yokohama release

-   Link parent contracts during drafting and negotiation phases to inherit parent contract terms.
-   Pause and resume an in-progress signature process when updates to the signatory list are required.
-   Perform wet signature in the electronic signature workflow. The enhanced electronic signature workflow capability provides flexibility to complete the signature process when the signatories want to do a wet signature instead of an electronic signature.
-   Upload the contract document directly from the Microsoft Word add-in for ServiceNow Contracts instead of selecting it from your system.
-   Use Logout icon \(![Logout icon](../image/cmpro-addin-logout.png)\) to log out from Microsoft Word add-in for ServiceNow Contracts.
-   Change the application scope to edit a contract template in the Microsoft Word add-in for ServiceNow Contracts. This option is only visible to the administrators.

See [Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-cmpro-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

**Important:** Contract Management Pro is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Link parent contract requests](https://www.servicenow.com/docs/access?context=cmpro-link-parent-cmr&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Establish a hierarchical relationship between the parent and child contract requests by using the **Link** option in the **Related contract requests** tab during drafting and negotiation phases.

    Establish a hierarchical relationship between the parent and child contract requests and automatically inherit the configured fields from the parent request by using the **Link and inherit fields** option in the **Related contract requests** tab during drafting and negotiation phases.

    The linked parent contract request appears in the **Related contract requests** tab and displays the parent-child hierarchy. The contract repository records that are associated with the parent and child contract requests are automatically linked after the contracts are signed.

    Use the **Remove linked contract** option in the **Related contract requests** tab to remove the linked parent contract request when you have linked a wrong contract request or the linking is no longer required.

-   **[Perpetual contracts](https://www.servicenow.com/docs/access?context=cncore-work-ss-cntr-request-fulfiller&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Select the **Perpetual** check box in the Details tab of a contract request to classify it as a perpetual contract. When this check box is selected, the contract end date must be blank.

    The **Perpetual** check box is available in contract requests that are initiated from Sales Customer Relationship Management and Source-to-Pay Operations.

-   **[Signature workflow for a contract request](https://www.servicenow.com/docs/access?context=cncore-signature-workflow&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    During the electronic signature process, one or more signatories can now choose to use a wet signature. In this scenario, the contract fulfiller uploads the partially signed document and sends the uploaded document to the remaining signatories to complete the signature process.


-   **[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](https://www.servicenow.com/docs/access?context=cncore-add-contrl-wrd-addin&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Logout and application scope change functionality in Microsoft Word add-in for ServiceNow contracts.


## Changed in this release

-   **[Select contract type while initiating a third-party contract](https://www.servicenow.com/docs/access?context=cncore-initiate-non-ss-cnt&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    In the Initiate contract window, the **Type** field appears when you select the **Third party paper** option. You can specify whether the contract request is for a single contract or multiple contracts.

    If you select **Single contract**, a **Contract type** field appears where you can define the type of contract document. This field isn’t available when you select **Multiple contracts**.

-   **[Classify contract requests as a single or multiple contracts type based on selected documents](https://www.servicenow.com/docs/access?context=snlc-submit-request-tpc&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    When you're creating a third-party contract review request from Employee Portal, you can now select a single contract document to classify it as a single contract type. By selecting multiple contract documents, you can classify them as a multiple contracts type. The **Type** field in the contract request reflects this selection by displaying either **Single contract** or **Multiple contracts**.

-   **[Use scripts to define additional conditions for a clause variation](https://www.servicenow.com/docs/access?context=cncore-add-clauses-doc-tmplt&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    You can now define the clause conditions on the fields and variables of a table that isn’t directly linked to the contract template table. The **Advanced script** check box in the Clause Variation form enables you to add custom logic to determine when a clause variation is used in a contract.

-   **[Configure tables in a contract template to append or add fields from related tables](https://www.servicenow.com/docs/access?context=cncore-append-data-table&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    You can now use scripts to insert additional data from the related table fields into the dynamic tables of a contract. The **Advanced script** check box in the Column Mapping form enables you to configure dynamic tables in a contract template to display additional data from related table fields by appending it to existing columns or adding it as new columns.

-   **[Contract Management Pro configurations are available on the Contract Request table](https://www.servicenow.com/docs/access?context=cncore-create-ct-word-addin&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    You can now set up the following Contract Management Pro configurations directly on the Contract Request \[sn\_cm\_core\_contract\_request\] table to centralize the configuration on a single table and improve consistency and reusability across business units:

    -   Contract templates
    -   Template rules
    -   Internal signatory rules
    -   Clause and clause variation setup
    -   Contract configuration
    -   External storage and e-signature integrations
    -   Mappings for Now Assist contract metadata extraction and Now Assist contract analysis
    The Contract Request table is automatically selected for a new configuration. You can manually select a different table, if necessary.

    **Note:** To avoid configuration issues, ensure that you select the same table across all related configurations.

-   **[Configure dynamic tables for contract template](https://www.servicenow.com/docs/access?context=cncore-addin-table&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    You can now set up the contract template on the Contract Request \[sn\_cm\_core\_contract\_request\] table. When you select the Contract Request table, the **Table** tab in the Microsoft Word add-in displays an additional field, called the **Parent request table** field, that you can use to select the source parent request table.

    Additionally, the **Table** field has been renamed to **Lookup table** where you can select the table from the data that is populated into the contract document.

    If the template isn’t based on the Contract Request table, only the **Lookup table** field is shown.

-   **[Signature blocks enabled by default for new contract templates](https://www.servicenow.com/docs/access?context=cncore-create-ct-word-addin&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    When you’re creating a contract template, the **Signature blocks** check box in the Word Template New Record form is selected by default. If you want to configure the participant-based signatories for the contract template, you can clear the check box.

-   **[Copy fields from parent request to contract request](https://www.servicenow.com/docs/access?context=cncore-copy-fld-frm-parent&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    You can now configure the ContractManagementExt extension point to automatically copy the required fields from the originating business unit record to the contract request when it’s initiated.

-   **[Modify signatories](https://www.servicenow.com/docs/access?context=cncore-pause-signature&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Enable contract fulfillers to pause an ongoing signature process, make necessary changes to the list or order of signatories, and then resume the process without restarting the entire workflow by using the **Modify Signatories** and **Resume signature** options. This feature is supported only for the Docusign electronic signature provider.

-   **[Signature workflow for a contract request](https://www.servicenow.com/docs/access?context=cncore-signature-workflow&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    The wet signature process has been enhanced for better control and clarity. Wet signature requests are sent one signatory at a time, starting with the first signatory in order. When the signatory signs and returns the document, the fulfiller manages the remaining signatures.

-   **[Resend signature request](https://www.servicenow.com/docs/access?context=cncore-resend-sign-req&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Enable contract fulfillers to manually trigger a signature request when needed, instead of relying on automated reminders by using the **Resend signature request** option.

-   **[Configuring signatories in Contract template using Microsoft Word add-in](https://www.servicenow.com/docs/access?context=cncore-config-sign-addin&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Signature placeholders in contract templates are now mapped to the e-signature tool tags \(such as Docusign\), instead of signer fields to help accommodate changes in the signatories. The values in the signature blocks are filled in by the signatories during the signing process.

-   **[Upload and parse a Microsoft Word document that includes content controls](https://www.servicenow.com/docs/access?context=cncore-upload-doc-addin&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Upload the contract document directly from the Microsoft Word Add-in instead of selecting it from your system.


## Activation information

Contract Management Pro is a ServiceNow AI Platform feature that is available with activation of the Contract Management Pro \(sn\_cm\_pro\). For details, see [Install Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-install-cmpro&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-cmpro-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use Contract Management Pro to set up contract document templates, clauses, clause variations, and to initiate contract requests. It also supports Now Assist -driven contract analysis and metadata extraction, e-signatures, wet signatures, and external storage systems.

-   **[Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    The ServiceNow® Now Assist in the Contract Management application analyzes a contract for missing and non-standard clauses. It also enables you to review and add the information to the mapped fields in the contract repository, eliminating the need to manually update the contract repository.


-   **[Now Assist in Contract Management release notes](cmpro-na-rn.md)**  
The ServiceNow® Now Assist in Contract Management uses generative AI capabilities to analyze a contract for missing or non-standard clauses and conversational search to query documents using natural language. It also includes agentic AI capabilities that automatically extract metadata and obligationsfrom signed contracts and calculate reminder dates for contract renewals or terminations. Now Assist in Contract Management was enhanced and updated in the Yokohama release.

**Parent Topic:**[Employee Service Management release notes](../employee-service-management/employee-service-management-rn-landing.md)

