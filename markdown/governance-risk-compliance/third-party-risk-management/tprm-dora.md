---
title: Using digital resilience third-party registers
description: Use the Digital Resilience Third-party Information Register application in the Vendor Management Workspace to create, update, and track assessments, branches, legal entities, and so on, and maintain registers of contractual arrangements with ICT third-party service providers.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 18
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Using digital resilience third-party registers

Use the Digital Resilience Third-party Information Register application in the Vendor Management Workspace to create, update, and track assessments, branches, legal entities, and so on, and maintain registers of contractual arrangements with ICT third-party service providers.

## Digital resilience third-party registers

Beginning with Release 19.1.x, the Digital Resilience Third-party Information Register application is supported for DORA compliance in the Vendor Management Workspace.

The Digital Resilience Third-party Information Register application is used to download the Digital resilience third-party registers. The application contains the Microsoft Excel template that includes all tabs for reporting purposes. It helps the financial entities to maintain a comprehensive register of their contractual arrangements with ICT Third-party service providers at the individual entity, sub-consolidated, and consolidated levels.

You can use Digital resilience third-party registers to create or edit the records in bulk or individually for assessments, branches, contracts, functions, legal entities, supply chains, third parties, or third-party engagements using the Microsoft Excel upload and download feature.

**Note:** The IRM Professional license users can access Digital resilience third-party registers in the Operational Resilience Workspace. The TPRM license users can access Digital resilience third-party registers in the TPRM Workspace.

The Digital resilience third-party registers application fulfills multiple functions for the entities:

-   Assists the entities in tracking their ICT third-party risks.
-   Empowers the competent authorities in European Union to oversee ICT and third-party risk management within financial entities.
-   Aids European Supervisory Authorities \(ESA\) in identifying Critical ICT third-party service providers \(CTPP\) for EU level supervision.

The following applications are used in the background for the Digital resilience third-party registers application:

-   Digital Resilience Third-party Information Register: This application is used to download the Digital resilience third-party registers application. It contains the Microsoft Excel template including all tabs for reporting purposes.
-   Digital Operational Resilience Management: This application is used for uploading and downloading of all individual DORA tables. It’s automatically installed when the Digital Resilience Third-party Information Register is activated.

For more information on configuring Digital resilience third-party registers and its possible use cases, see [Configuring Digital resilience third-party registers](../../grc-operational-res/concept/conf-dg-resi-party-regi.md) and [Use cases for updating the information registers](../../grc-operational-res/concept/use-cases-for-contra-arrangements.md).

## Digital Operational Resilience

Digital Operational Resilience refers to the ability of a financial entity to build, assure, and review its operational integrity and reliability. It ensures that the entity has the full range of ICT related capabilities that are needed to secure its network and information systems. These systems support the continuous provision of financial services and maintain their quality, even during disruptions. The continuity can be achieved directly or indirectly with the services provided by the ICT third-party service providers.

## Digital Operational Resilience Act

Digital Operational Resilience aligns with the Digital Operational Resilience Act \(DORA\). It’s a European Union \(EU\) regulation that came into effect on 16 January 2023 and it will be applicable from January 17, 2025. It enhances the ICT security of financial entities supervised by the European Supervisory Authorities \(ESA\)s and protects Europe's financial sector from major digital disruptions.

For more information on DORA and the Digital Resilience Third-party Information Register application, see [https://www.eba.europa.eu/activities/direct-supervision-and-oversight/digital-operational-resilience-act](https://www.eba.europa.eu/activities/direct-supervision-and-oversight/digital-operational-resilience-act) and [Exploring Digital resilience third-party registers](../../grc-operational-res/concept/exploring-digi-resi-third-party-registers.md).

## Creating records for Digital resilience third-party registers

Third-party risk \(TPR\) assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] and TPR managers \[sn\_vdr\_risk\_asmt.vendor\_manager\] can create and update these records by navigating to the Digital resilience third-party registers in the Vendor Management Workspace. You must create or update these records in a specific sequence. For more information on this sequence, see [Creating and reviewing the records](../../grc-operational-res/concept/order-for-creating-records.md).

**Note:** TPR assessors and TPR managers can delete Third party, Third-party engagement, and Contract records. TPR administrators \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] can delete all record types by navigating to each individual record and selecting **Delete**.

The following example shows how records appear in the Digital resilience third-party registers in the Vendor Management Workspace.

![Example that shows how records are shown in the Digital resilience third-party registers.](../image/tprm-drtpr-le.png)

The following records can be manually created and updated.

-   **Legal entities**

    You can create a legal entity record, by navigating to the Digital resilience third-party registers in the Vendor Management Workspace. Here, you can view existing legal entities and enhance their digital resilience information to comply with DORA regulations. After installing the Digital Resilience Third-party Information Register application, a **Legal Entities** related list is added for existing companies that aren’t already defined as a third party, enabling you to add their details. The Legal Entity record includes essential fields for regulatory reporting, such as the Legal Entity Identifier \(LEI\), name, country of registration, and entity type. These fields are offered as choice lists within the system. The system acknowledges the entity hierarchy, with no additional details required for ultimate parents, while subsidiaries must specify their parent entity. The date of registration for each legal entity is also noted. Additionally, specific details like the last update, integration date, removal status, deletion date, currency used, and total asset value are documented for each entity, as required by regulators for entities engaging with external third parties for outsourced technical services. Regulators mandate these specific details for legal entities engaging with external third parties for outsourced technical services.

    **Note:** Existing third parties aren’t shown in the Legal entities list. Company records can only be defined as a Third party or Legal entity. For companies and legal entities, the Vendor option is set to **False**. \(The check box isn’t selected.\)

    For more information see, [Create a legal entity and enhance digital resilience data](../task/tprm-legal-entity.md), [Create New Company form](../reference/tprm-create-new-legal-entity-form.md), and [Create New Legal entity form](../reference/tprm-create-new-legal-entity.md).

-   **Branches**

    You can create a branch record by navigating to the Digital resilience third-party registers in the Vendor Management Workspace. This enables you to enhance the branch's digital resilience information to help ensure compliance with DORA regulations. A legal entity can operate multiple branches across different cities or countries, and all these branches can be documented. When a new branch is established, its information must be included for regulatory reporting. Some common details captured include the branch name and description, owner's details, business units and departments for reporting purposes, whether the branch is a head office or another type, the branch ID, and its originating country. The branch number is auto-generated, and once all details are complete, the information is ready to be captured in the information register.

    For more information see, [Create a branch and enhance digital resilience data](../task/tprm-drtp-reg-branch.md) and [Create New Branch form](../reference/tprm-create-new-branch-form.md).

-   **Function**

    You can create a function record, by navigating to the Digital resilience third-party registers in the Vendor Management Workspace. Here, you can add details such as the function identifier, license activity, function name, and criticality or importance assessment. Each function represents a specific service or group of services as defined by the Digital Operational Resilience Act \(DORA\). The functions record is used to capture detailed information about each function, including descriptive text. Once the function record is created, you can enhance its digital resilience information to help ensure compliance with DORA regulations, effectively documenting the third-party provided ICT service usage.

    For more information see, [Create a function and enhance digital resilience data](../task/tprm-drtp-reg-function.md) and [Create New Function form](../reference/tprm-create-new-function-form.md).

-   **Third parties**

    You can access and view existing third-party records by selecting the Third parties list within the Digital resilience third-party registers in the Vendor Management Workspace. After installing the Digital resilience third-party registers, a **Digital Resilience Information** related list is added on the third party's page, enabling you to set up the digital resilience information details.

    Here, you can view the legal entity ID of the third party, which can be captured by the Value Added Tax \(VAT\) number or Company Registration Number \(CRN\). You can specify the country of registration and its code, which the system uses to generate the ID. Additionally, you can indicate if the third party is an ultimate or a subsidiary, include the name of the ICT third party and the type of service they provide \(for example, Software as a Service\), and optionally note if an individual acts on behalf of the organization. You can also select the reporting currency and input the total annual expense for this engagement.

    For more information see, [Create a third party and enhance digital resilience data](../task/tprm-drtp-reg-third-party.md), [Create New Company form](../reference/tprm-create-third-party-company-form.md), and [Create New ICT third-party service provider form](../reference/tprm-create-ICT-thirdparty-serv-prov-form.md).

-   **Engagements**

    You can access and view existing third-party engagement records by selecting the Third-party engagements list within the Digital resilience third-party registers in the Vendor Management Workspace. After you install the Digital resilience third-party registers, the **Digital Resilience Information** related list is added on the third-party engagements page, enabling you to set up the digital resilience information details.

    Here you can view the third party's name, its type, annual spend, engagement tier, and other relevant information. You can enhance the record's digital resilience information by creating ICT third-party service provider records. Add ICT third-party service provider details such as the name of the service provider, its identification code, type of ICT services, currency, and so on. This enhances the digital resilience information of its associated third-party engagement for compliance with DORA regulation.

    For more information see, [Create a third-party engagement and enhance digital resilience data](../task/tprm-drtp-reg-tp-engagement.md), [Create New Third-party engagement form](../reference/tprm-create-engmt-form.md), and [Add Digital resilience information to third-party engagements](../task/tprm-add-digi-resi-info.md).

-   **Contracts**

    You can create a contract record by navigating to the Digital resilience third-party registers in the Vendor Management Workspace. Here, you can add details such as the vendor name, start and end dates, state, substate, and other relevant information. Once the contract record is established, you can enhance its digital resilience information to help ensure compliance with the DORA regulations.

    The Digital resilience third-party registers provide details about who within your organization is using externally outsourced ICT services, which functions and branches are using them, and who the third-party providers and their engagements are. Contracts serve as the link between these aspects, binding legal entities, branches, and functions to third parties and their engagements.

    You can access these contracts through the Contracts list in the Digital resilience third-party registers. Alternatively, navigate to a specific legal entity's record, open the **Legal Entities** related list, and access all associated contract information. To view contracts for a legal entity, go to the legal entity's record, open the **Legal Entities** related list, and navigate to the different Contracts-related tabs. If the entity signing the contract differs from the one using it, that detail is included in the record, along with the service provider. Details captured in these records can include data storage and processing locations, data sensitivity and service provider reliance, contract and termination details, annual assessments, and contractual reference numbers.

    For more information see, [Create a contract and enhance digital resilience data](../task/tprm-drtp-reg-contract.md), [Create New Contract form](../reference/tprm-create-new-contract-form.md), and [Create New Contractual arrangement form](../reference/tprm-create-new-cont-arrange-form.md).

    **Note:** Provider‑level annual expense totals may be automatically aggregated during report generation when all contracts meet the required criteria. Aggregation applies only to exported reports and does not change contract records.

    For more information, see [Currency conversion and third-party total expense aggregation](tprm-dora-currency-aggregation.md).

-   **Supply chains**

    You can create a supply chain record by navigating to the Digital resilience third-party registers in the Vendor Management Workspace. Here you can capture details of the supply chain such as the type of the ICT services, Legal Entity Identifier \(LEI\) of the entity that provides the ICT services, and so on.

    For more information see, [Create a supply chain and enhance digital resilience data](../task/tprm-drtp-reg-supply-chain.md) and [Create New Contractual arrangement form](../reference/tprm-create-new-cont-arrange-form.md).

-   **Assessments**

    You can create an assessment of the ICT service record by navigating to the Digital resilience third-party registers in the Vendor Management Workspace. Here, you can add details such as the contractual arrangement reference number, identification code, and type of code for the ICT third-party service provider. Once the assessment is created, you can enhance its digital resilience information to help ensure compliance with the DORA regulation. It’s required to review your contracts and third parties annually.

    Add details such as the contractual arrangement reference number, identification code, and type of code for the ICT third-party service provider. You can then enhance its digital resilience information for compliance with DORA regulation.

    For more information see, [Create an assessment and enhance digital resilience data](../task/tprm-drtp-reg-assmt.md) and [Create New Contractual arrangement form](../reference/tprm-create-new-cont-arrange-form.md).


For more information on the roles related to using Digital resilience third-party registers, see [Roles in Third-party Risk Management](../../grc-vendor-risk-implementation/reference/tprm-roles.md).

## Uploading and downloading records

In addition to creating individual records, TPR assessors and TPR managers can request the download of records using the Excel download/upload requests feature. For more information see, [Create a Microsoft Excel download request](../task/tprm-excel-upload-download-request.md), and [Create New Excel download/upload request form](../reference/tprm-excel-upload-download-req.md).

**Note:** You need the TPR administrator role to edit and delete Excel download/upload requests.

TPR administrators can create and update records in bulk using the Excel download/upload requests feature. For more information, see [Create records in bulk](../task/tprm-bulk-create.md) and [Update existing records in bulk](../task/tprm-bulk-update.md).

**Note:** Annual expense data is evaluated during Register of Information report generation when currency conversion or third-party total expense aggregation is enabled on the Excel download/upload request. Ensure that currencies and annual expense fields are accurate to avoid conversion failures or skipped aggregation

The following example shows where you can view and create Excel download/upload requests.

![Example that shows where you can view and create Excel download/upload requests.](../image/tprm-drtpr.png)

**Note:** If you have the Third-party assessment reviewer \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] role, you can export a list of each record type by navigating to the list of records you want in the Digital resilience third-party registers in the Vendor Management Workspace.

## Register of Information packages

After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party assessors \(sn\_vdr\_risk\_asmt.vendor\_assessor\) can generate regulator-ready Register of Information \(RoI\) packages using the Plain-CSV Report Package option on the download page. The resulting ZIP file includes metadata and report folders structured to regulator specifications, with filenames containing the Legal Entity Identifier \(LEI\), entity ID, and release version. This format ensures EU DORA compliance and supports automated validation workflows. Users can follow the guide provided in the Instructions section on the Download/Upload request page for step-by-step instructions and required permissions. For more information, see [Register of information regulatory packages](tprm-dora-roi.md) and [Generate a register of information package](../task/tprm-drtp-roi-packages.md).

During RoI package generation, users can optionally enable currency conversion and third-party total expense aggregation. When enabled, these options standardize annual expense values using historical exchange rates and consolidate eligible contract expenses at the provider or engagement level in the exported package.

Third-party risk managers \(sn\_vdr\_risk\_asmt.vendor\_manager\) can validate downloaded RoI packages using the same Plain-CSV Report Package option. The system performs validation across multiple tables, checking file format, structure, encoding, naming conventions, and field-level data. If validation warnings are detected, a report is automatically attached, including mappings to regulator fields such as Template Code, Row Code, and Column Code. These reports also include real-world field labels, rule expressions, and record identifiers. Validation errors can be cross-referenced using a downloadable Excel master template that mirrors the CSV structure, simplifying issue identification and resolution. This template can be generated using the Excel master template option on the download page. Additional enhancements include support for “Not applicable” values, enforcement of file size limits, and clearer error messages for malformed data. For more information, see [Validation framework for Register of Information](tprm-validation-roi.md) and [Validate Register of Information packages](../task/tprm-valid-dora.md).

**Note:**

Use the ITS on the Registers of Information, adopted and published in the Official Journal of the European Union \([Commission Implementing Regulation \(EU\) 2024/2956](https://eur-lex.europa.eu/eli/reg_impl/2024/2956/oj/eng)\), together with the EBA FAQs on RoI reporting \([EBA FAQs\)](https://www.eba.europa.eu/sites/default/files/2025-03/b90dc121-77cd-47cc-a8c7-ceebda33e381/20250319%20-%20DORA%20RoI%20reporting%20FAQ%20%28updated%29.pdf), to understand regulatory reporting requirements and column-level descriptions.

Refer to the sample files provided under the taxonomy architecture v2.0 to validate reporting structure. Download the taxonomy package and, under `instances/xBRL-CSV`, locate the DORA sample file `DUMMYLEI123456789012.CON_FR_DORA010100_DORA_2024-12-31_20241213174803429` to review the expected xBRL-CSV format.

