---
title: AI Risk and Compliance release notes
description: The ServiceNow AI Risk and Compliance application helps you to manage your AI capabilities ethically, mitigate AI risks, and maintain compliance. AI Risk and Compliance was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 5
keywords: [AI Risk and Compliance, AIRC release notes, AI governance, SB 53, Colorado AI Act, impact assessment auto-population, template versioning, multi-framework citations]
---

# AI Risk and Compliance release notes

The ServiceNow® AI Risk and Compliance application helps you to manage your AI capabilities ethically, mitigate AI risks, and maintain compliance. AI Risk and Compliance was enhanced and updated in the Australia release.

## AI Risk and Compliance highlights for the Australia release

-   Manage Smart Assessment templates with versioning support. Create, publish, and delete template versions to support consistent assessment governance.
-   View the related entity \(AI record, model, or dataset\) and control for each control attestation-based assessment directly in task and work queue lists, without opening the individual record.
-   Access authority documents, agency mappings, and citations for additional AI regulatory frameworks in the AI Risk and Compliance content pack.
-   Classify AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), enabling early risk identification and consistent AI governance decisions across the system life cycle.
-   Submit AI cases anonymously to report potential AI risks or concerns without disclosing your identity, helping improve early risk visibility and participation in AI governance.
-   Offboard AI assets with structured life-cycle tasks to support completion of governance and risk activities when systems are retired or replaced.

See [AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-and-compliance.md) for more information.

**Important:** AI Risk and Compliance is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the AI Risk and Compliance release

-   **[Risk‑based classification during intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/request-ai-system.md)**

    After upgrading to version 22.0.3, if you have the AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] role, you can now classify AI systems using a risk‑based approach at intake, enabling organizations to capture AI risk context early and align governance workflows with regulatory and internal risk requirements. This improvement to the AI use case request form supports more accurate AI oversight throughout the system life cycle.

-   **[Report an AI case anonymously](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/report-ai-case-anon.md)**

    After upgrading to version 22.0.3, if you have the AI Case Management \(sn\_ai\_case\_mgmt\) application installed and the AI case business user \[sn\_ai\_case\_mgmt.ai\_case\_business\_user\] role, you can navigate to the Employee Center to access the Anonymous Reporting Center and submit AI cases anonymously, enabling broader participation in AI governance while protecting the identity of reporters. No additional role is required to submit an anonymous report directly through the Anonymous Reporting Center. Broader participation helps organizations identify potential AI risks earlier by removing barriers to case submission.

-   **[Offboard AI models and datasets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-offboarding-ai-assets.md)**

    After upgrading to version 22.0.3, if you have the AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] role you can manage AI asset offboarding life cycle tasks. Managing these tasks supports completion of governance-related activities, such as risk and impact assessments, conformity reviews, issue closure, and audit documentation, when an AI asset is retired or removed from active use.


## UI changes

-   **[Operations tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/operations-tab.md)**

    On the Operations tab in the AI Risk and Compliance Workspace, the AI systems by state section includes an Offboard state to track AI systems in retirement or offboarding and the AI systems by department section now supports grouping by Risk classification from the Show by drop-down list to view the distribution of AI systems in each department.

-   **[AI use case request form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-intake.md)**

    A Use and Purpose section containing screening questions has been added to the AI use case request form to capture contextual information about how an AI system will be used and supports automated risk‑based classification during submission.

-   **[AI system record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-system-airc.md)**

    A Use and Purpose section has been added to the AI system record page, which you can access from the AI asset inventory list in the AI Risk and Compliance Workspace.

-   **AI record labels**

    The AI assets \(sn\_grc\_ai\_gov\_ai\_system\) table has been renamed to AI records \(sn\_grc\_ai\_gov\_ai\_system\). Two field labels on AI system, AI model, and dataset record pages in the AI Risk and Compliance Workspace have changed. The **Record type** field now displays **AI record** instead of the previous asset-specific labels. On AI system records, the **Asset type** field has been replaced by **Parent category**, which displays **AI system**.

-   **[Anonymous AI case reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-cases-inquiries.md)**

    A Visit Anonymous Reporting Center card is available in the Support resources section of the AI assets page in the Employee Center, enabling you to navigate to the Anonymous Reporting Center to submit an anonymous AI case.


## Changed in this release

-   **[Smart Assessment Engine template versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-assessment-templates.md)**

    After upgrading to version 22.3.5, if you have the AI risk and compliance admin \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\] role, you can use Smart Assessment templates that support versioning. A new version is created automatically when you edit and save a template. Publishing a new version retires the previously published version. Existing templates are set to Version 1.

-   **[Assessment scope context in task and work queue lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/tasks-ai-risk-compliance.md)**

    After upgrading to version 22.3.5, if you have the AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] role, assessment task list and work queue views display additional columns that show the governance scope \(related entity such as AI asset, model, or dataset\) of each control attestation-based assessment. These columns let you identify which AI asset, entity, and control an assessment belongs to without opening the individual record.

-   **[Impact assessment field auto-population](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-intake.md)**

    After upgrading to version 22.3.5, if you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] or AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] role, the screening question responses that capture the AI system's intended use and operational context from the Use and Purpose section of the AI use case request form are automatically populated in the corresponding Use and Purpose fields of a new impact assessment. This synchronization reduces manual entry and helps ensure that impact assessment responses are consistent with the information submitted at intake.

-   **[AI Risk and Compliance Content Pack regulatory frameworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/airc-content-pack.md)**

    After upgrading to version 22.3.0, if you have the AI Risk and Compliance Content application installed and the admin role, the AI Risk and Compliance content pack includes additional authority documents, agency mappings, and citations for the following regulatory frameworks: the Transparency in Frontier Artificial Intelligence Act \(SB 53\) and the Colorado Artificial Intelligence Act \(SB 205\). When at least one regulatory framework is activated, control objective records display citations from all activated authority documents in the **Citations** tab. This enables you to assess cross-framework regulatory coverage from a single control objective record without navigating each framework separately.


## Activation information

Install AI Risk and Compliance by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower-landing.md)**

    Use the ServiceNow®AI Control Tower application with AI Risk and Compliance to oversee and manage the AI asset inventory life cycle.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

