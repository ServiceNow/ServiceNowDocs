---
title: SBOM records and relationships in Third-party Risk Management
description: The records, related lists, and relationships created when you collect SBOM data in Third-party Risk Management, and how those records relate to engagements and third parties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-sbom-relationship.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 4
keywords: [SBOM, software bill of materials, BOM entity, BOM components, data model]
breadcrumb: [Third-party risk management data model, Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# SBOM records and relationships in Third-party Risk Management

The records, related lists, and relationships created when you collect SBOM data in Third-party Risk Management, and how those records relate to engagements and third parties.

## SBOM document related list \(engagement\)

The SBOM document related list appears on the engagement record and tracks each SBOM submission attempt for that engagement. Separate entries are created for successful and failed uploads.

Successful processing depends on whether the submitted file conforms to a supported SBOM schema and can be parsed by the SBOM API. Supported formats are JSON and XML. Files submitted in any other format return a parse error and a new entry is created in this list to record the failed attempt.

Each submission attempt creates a separate SBOM document record. Previously submitted documents are retained and not replaced or removed.

**Note:** Third-party assessment reviewers can view records in the SBOM document related list and the BOM components related list on the engagement and third-party records. Reviewers do not have access to the SBOM workspace.

|Field|Description|
|-----|-----------|
|Format|The declared file format of the SBOM submission, for example, JSON or XML.|
|Version|The version declared in the SBOM file.|
|Status|The processing status of the submission, for example, queued, processed successfully, or error.|
|Source assessment|The assessment instance that triggered the SBOM upload.|

## BOM components related list \(engagement\)

The BOM components related list on the engagement record shows all BOM component records generated from SBOM files collected for that engagement. Each component represents a declared library or dependency from the submitted SBOM.

If the SBOM Response and ITSM Vulnerability Response applications are available, vulnerability-related columns may appear at the individual component level. Vulnerability severity is not rolled up to the engagement or third-party level.

## Data model and record relationships

This table describes how SBOM records relate to each other and to TPRM records after a successful upload.

|Relationship|How it works|
|------------|------------|
|Engagement → SBOM document|An M2M table \(`sn_vdr_risk_asmt_m2m_engagement_sbom_doc`\) links each engagement to the SBOM documents collected for it.|
|Engagement SBOM document → Smart assessment instance|The M2M table also links to the SAE assessment instance \(`sn_smart_asmt_instance`\) that triggered the SBOM upload. This relationship is surfaced as the **Source assessment** field on the SBOM document record.|
|SBOM document → BOM entity|When the SBOM API parses a file, it creates a parent BOM entity record representing the submitted SBOM document as a whole.|
|BOM entity → BOM components|Each BOM entity has one or more child BOM component records representing individual libraries and dependencies declared in the SBOM.|
|BOM component → third party|BOM components can be associated with a third party through the product model relationship. The product model manufacturer field can reference a `core_company` record.|
|Engagement → BOM components|Components are surfaced on the engagement through the relationship chain: engagement → SBOM document → BOM entity → BOM components.|

**Note:** The SBOM workspace has no engagement concept. Engagement-level linkage occurs only when SBOMs are collected through the TPRM workflow. SBOM files uploaded directly into the SBOM workspace do not appear in engagement-level related lists.

## Work notes tracking

Work notes on the external assessment provide a running log of SBOM processing activity. Examples include:

-   Queued for processing — written when the submission is sent to the SBOM API.
-   Processed successfully — written when the SBOM API confirms successful parsing.
-   Error message — written when parsing fails, including the reason returned by the SBOM API.
-   Third-party declined — written when the engagement contact selects a **No** response option.

## SBOM questionnaire template

The SBOM questionnaire template is provided by ServiceNow and is configured as a TPRM external questionnaire with scoring disabled.

The template includes these questions:

1.  Can you provide an SBOM?
    -   Yes
    -   No, we do not generate SBOMs.
    -   No, we do not disclose SBOMs outside the company.
    -   No, other. \(Please explain.\)
2.  Upload your SBOM file. This question appears only when the response to question 1 is **Yes**.

You can modify the questionnaire template to meet internal requirements.

## Post-assessment automation

A subflow in Flow Designer handles post-assessment actions when an SBOM questionnaire is submitted.

The subflow performs these actions:

-   Sends the uploaded file to the SBOM API.
-   Tracks the `sn_bom_doc` record status.
-   On success, creates the engagement-to-SBOM relationship and updates assessment activity.
-   On error, records the error message and enables resubmission.
-   On third-party decline, records the response and closes the assessment.

**Parent Topic:**[Third-party risk management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-data-model.md)

**Related topics**  


[Exploring software bill of materials collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-exploring.md)

[Collecting software bill of materials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom.md)

[Request a software bill of materials from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-sbom-collect.md)

[Review a software bill of materials submission from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/sbom-review.md)

[Activate SBOM support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/sbom-activate.md)

