---
title: Privacy Management release notes
description: The ServiceNow Privacy Management application enables you to manage your organization's privacy risks and compliance to protect your customers, employees, and suppliers. Privacy Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Privacy Management release notes

The ServiceNow® Privacy Management application enables you to manage your organization's privacy risks and compliance to protect your customers, employees, and suppliers. Privacy Management was enhanced and updated in the Australia release.

## Privacy Management highlights for the Australia release

-   Configure the Personal Data Rights \(PDR\) external-facing form to map jurisdictions to data subject types and request types, and control whether an authorized agent can submit a request on behalf of a data subject.
-   Enable key stakeholders to view and update processing activities that they own directly from **GRC tasks** in the Employee Center.
-   Activate new ready-to-use privacy content, including risk statements and authority documents, such as Digital Personal Data Protection Act 2023 \(DPDPA\), the Virginia Consumer Data Protection Act, and the Colorado Privacy Act.
-   Automatically generate an AI-recommended privacy case summary from varied compliance case data, reducing investigation time and enabling faster, more consistent decision-making.
-   Anonymously report compliance violations through a secure portal that maintains complete identity protection while enabling organizational trust and regulatory compliance.

See [Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-management.md) for more information.

**Important:** Privacy Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   ****
    -   Starting from version 22.3.x of Personal Data Rights, privacy administrators can navigate to **External form configuration** to tailor the public-facing PDR form for their organization. They can map jurisdictions to data subject types and request types, and specify whether an authorized agent can submit a request on behalf of a data subject for each jurisdiction.
    -   For each jurisdiction, administrators can add terms and conditions, disclaimers, and guidance text that requesters see when they submit a request from that jurisdiction.
    -   Administrators can also show or hide form fields based on the combination of jurisdiction, data subject type, and request type that a requester selects. The form collects only the information needed, therefore, requesters see only the fields that apply to their request.
-   ****
    -   Starting from version 22.3.x of Privacy Management, privacy analysts can add any user, including users without privacy roles, as a key stakeholder on a processing activity. Such users are set to **No privilege to respond to assessments** by default, and therefore, can only view the record if they are granted the business user role.
    -   Key stakeholders with the appropriate business user role can select **Request edit access** to ask the privacy analyst for editing rights to a processing activity.
-   **New privacy content in Privacy Management Content**
    -   Starting from version 22.3.x of Privacy Management Content, privacy managers can extend their regulatory library with new ready-to-use authority documents, Digital Personal Data Protection Act 2023 \(DPDPA\), Virginia Consumer Data Protection Act, and Colorado Privacy Act. When activating an authority document, they can select which citations to add to the library, and then select from the AI-generated control objectives already mapped to those citations.
    -   Privacy Management Content also ships an updated version of privacy risk statement that carries forward the AI-generated risk statements from the previous version and adds new ones. Reinstalling the already existing risk statements after the update may overwrite certain changes made to them.
-   **Smart assessment versioning of privacy assessment templates**

    Starting from version 22.3.x of Privacy Management and Privacy Case Management, you can create a version of an existing privacy assessment template to revise the questionnaire, response options, or automations without disrupting assessments that are already in progress. New privacy assessments use the latest published version of the template.


-   **[GRC case summarization skill for privacy cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-case-summarization-skill.md)**

    Privacy analysts can now use the Now Assist case summarization feature to quickly understand a privacy case without manually reviewing every field or related list. Now Assist analyzes key case attributes, such as timelines, impacted areas, evidence, and actions, and generates a structured summary directly inside the privacy case. This feature solves a common problem: case data is often lengthy, scattered across multiple related lists, and difficult for analysts to digest efficiently. Analysts can also save and edit summaries as case data evolves, ensuring the record stays current.

-   **[Report a privacy case anonymously](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/report-privacy-case-anonymously.md)**

    Employees can now use the Anonymous Reporting Center to report privacy violations such as data breaches or exposure, unauthorized data use, privacy law violations \(GDPR, CCPA\), or other privacy-by-design lapses without revealing their identity or location.

    Accessed through the Employee Center, the Anonymous Reporting Center portal automatically logs users out to enforce anonymity, creates case records without mapping to employee identity, and provides a unique report key for secure follow-up communication.

    Reports are routed to the appropriate compliance team based on the nature of the concern. Throughout the investigation process:

    -   Investigators can request additional information through a comments system visible to the reporter
    -   Reporters can follow up on their case using their report key to check progress and respond to questions
    -   All interactions maintain reporter anonymity at every step; no identity or location data is ever captured or linked
    This enhancement enables organizations to build trust, mitigate risks before escalation, and ensures regulatory compliance with whistleblower protection requirements.

-   **[Hierarchy and lineage enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/hierarchy-tab.md)**

    The Hierarchy and lineage enhancements enables privacy teams to identify which systems, vendors, and applications belong to a specific processing activity by marking relationships as “part of a processing activity.” This ability differentiates scoped components from global or shared connections. Users can toggle between a processing‑activity‑scoped view and a full lineage view, helping them understand data flows in the appropriate context.

-   **[Privacy content accelerator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-content-accelerator.md)**

    The privacy regulatory content through Unified Content Management provides pre‑built authority documents, citations, control objectives, and risk statements aligned with major privacy frameworks, including GDPR, CCPA, LGPD, and the NIST Privacy Framework 1.0. These resources are available for download directly from the Privacy Workspace, enabling teams to readily access standardized regulatory content.


## Changed in this release

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Activation information

Install Privacy Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

