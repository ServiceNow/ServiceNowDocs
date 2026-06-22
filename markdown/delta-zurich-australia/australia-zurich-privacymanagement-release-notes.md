---
title: Combined Privacy Management release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Privacy Management from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-privacymanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Privacy Management release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Privacy Management from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Privacy Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Privacy Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Privacy Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Data subjects](https://www.servicenow.com/docs/access?context=data-subjects&family=zurich&ft:locale=en-US)**

Select and define the multiple data subject types for each processing activity. You can capture the volume of data subjects that were processed, the specific data elements that were collected from the users, and the user locations. With this feature, you get a realistic, granular, and scalable representation of your processing activities.

-   **[Privacy management dashboard](https://www.servicenow.com/docs/access?context=privacy-manager-dashboard&family=zurich&ft:locale=en-US)**

Get an overview of your complete privacy risk and compliance posture from the Privacy Management dashboard so that you can quickly prioritize and remediate your processing activities. By looking at the Processing Activities, Risk &amp; Compliance, and Operations &amp; Case management sections, you can see the overall compliance score, trends, privacy criticality assessment scores, and risk heatmap. From the dashboard, you can also see information about the global legal framework to understand the regional obligations and the built-in risk metrics that automatically assess each processing activity.

-   **[New screening and PIA templates](https://www.servicenow.com/docs/access?context=privacy-mgmt-workflow&family=zurich&ft:locale=en-US)**

Use the new Privacy Impact Assessments \(PIAs\) and Screening Assessment templates that provide standardized questions, evaluation criteria, and workflows so that you can perform a processing activity criticality and privacy risk assessment. With these new templates, you can ensure consistency, reduce manual effort, and support compliance with regulatory and organizational requirements.


</td></tr><tr><td>

Australia

</td><td>

-   **[\[Placeholder link text to key configure-pdr-ext-form\]](https://www.servicenow.com/docs/access?context=configure-pdr-ext-form&family=australia&ft:locale=en-US)**
    -   Starting from version 22.3.x of Personal Data Rights, privacy administrators can navigate to **External form configuration** to tailor the public-facing PDR form for their organization. They can map jurisdictions to data subject types and request types, and specify whether an authorized agent can submit a request on behalf of a data subject for each jurisdiction.
    -   For each jurisdiction, administrators can add terms and conditions, disclaimers, and guidance text that requesters see when they submit a request from that jurisdiction.
    -   Administrators can also show or hide form fields based on the combination of jurisdiction, data subject type, and request type that a requester selects. The form collects only the information needed, therefore, requesters see only the fields that apply to their request.
-   **[\[Placeholder link text to key add-stakeholders-to-a-pa\]](https://www.servicenow.com/docs/access?context=add-stakeholders-to-a-pa&family=australia&ft:locale=en-US)**
    -   Starting from version 22.3.x of Privacy Management, privacy analysts can add any user, including users without privacy roles, as a key stakeholder on a processing activity. Such users are set to **No privilege to respond to assessments** by default, and therefore, can only view the record if they are granted the business user role.
    -   Key stakeholders with the appropriate business user role can select **Request edit access** to ask the privacy analyst for editing rights to a processing activity.
-   **[New privacy content in Privacy Management Content](https://www.servicenow.com/docs/access?context=update-privacy-content&family=australia&ft:locale=en-US)**
    -   Starting from version 22.3.x of Privacy Management Content, privacy managers can extend their regulatory library with new ready-to-use authority documents, Digital Personal Data Protection Act 2023 \(DPDPA\), Virginia Consumer Data Protection Act, and Colorado Privacy Act. When activating an authority document, they can select which citations to add to the library, and then select from the AI-generated control objectives already mapped to those citations.
    -   Privacy Management Content also ships an updated version of privacy risk statement that carries forward the AI-generated risk statements from the previous version and adds new ones. Reinstalling the already existing risk statements after the update may overwrite certain changes made to them.
-   **[Smart assessment versioning of privacy assessment templates](https://www.servicenow.com/docs/access?context=create-new-smart-asmt-version&family=australia&ft:locale=en-US)**

Starting from version 22.3.x of Privacy Management and Privacy Case Management, you can create a version of an existing privacy assessment template to revise the questionnaire, response options, or automations without disrupting assessments that are already in progress. New privacy assessments use the latest published version of the template.


-   **[Case summarization for privacy cases](https://www.servicenow.com/docs/access?context=privacy-case-summarization-skill&family=australia&ft:locale=en-US)**

Privacy analysts can now use the Now Assist case summarization feature to quickly understand a privacy case without manually reviewing every field or related list. Now Assist analyzes key case attributes, such as timelines, impacted areas, evidence, and actions, and generates a structured summary directly inside the privacy case. This feature solves a common problem: case data is often lengthy, scattered across multiple related lists, and difficult for analysts to digest efficiently. Analysts can also save and edit summaries as case data evolves, ensuring the record stays current.

-   **[Report a privacy case anonymously](https://www.servicenow.com/docs/access?context=report-privacy-case-anonymously&family=australia&ft:locale=en-US)**

Employees can now use the Anonymous Reporting Center to report privacy violations such as data breaches or exposure, unauthorized data use, privacy law violations \(GDPR, CCPA\), or other privacy-by-design lapses without revealing their identity or location.

Accessed through the Employee Center, the Anonymous Reporting Center portal automatically logs users out to enforce anonymity, creates case records without mapping to employee identity, and provides a unique report key for secure follow-up communication.

Reports are routed to the appropriate compliance team based on the nature of the concern. Throughout the investigation process:

    -   Investigators can request additional information through a comments system visible to the reporter
    -   Reporters can follow up on their case using their report key to check progress and respond to questions
    -   All interactions maintain reporter anonymity at every step; no identity or location data is ever captured or linked
This enhancement enables organizations to build trust, mitigate risks before escalation, and ensures regulatory compliance with whistleblower protection requirements.

-   **[Hierarchy and lineage enhancements](https://www.servicenow.com/docs/access?context=hierarchy-tab&family=australia&ft:locale=en-US)**

The Hierarchy and lineage enhancements enables privacy teams to identify which systems, vendors, and applications belong to a specific processing activity by marking relationships as “part of a processing activity.” This ability differentiates scoped components from global or shared connections. Users can toggle between a processing‑activity‑scoped view and a full lineage view, helping them understand data flows in the appropriate context.

-   **[Privacy content accelerator](https://www.servicenow.com/docs/access?context=privacy-content-accelerator&family=australia&ft:locale=en-US)**

The privacy regulatory content through Unified Content Management provides pre‑built authority documents, citations, control objectives, and risk statements aligned with major privacy frameworks, including GDPR, CCPA, LGPD, and the NIST Privacy Framework 1.0. These resources are available for download directly from the Privacy Workspace, enabling teams to readily access standardized regulatory content.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Privacy Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

-   **[Processing activity tab](https://www.servicenow.com/docs/access?context=processing-activity-tab&family=zurich&ft:locale=en-US)**

The revamped Processing Activity overview page provides a unified dashboard that displays key compliance and risk metrics, such as risk scores, compliance scores, and criticality scores. This update makes it easier for privacy managers and analysts to assess the status of each processing activity, track open issues, and prioritize actions.


-   **[Layout for processing activity record view](https://www.servicenow.com/docs/access?context=processing-activity-homepage&family=zurich&ft:locale=en-US)**

The vertical layout of a processing activity enables you to see the information in a top-down linear flow. With this layout, you can see the sequential representation of a data processing workflow.

-   **[Privacy management home page](https://www.servicenow.com/docs/access?context=privacy-mgmt-ws-privacy-compliance-manager&family=zurich&ft:locale=en-US)**

The enhanced Privacy Management home page now has dedicated tabs for Processing Activity, Risk and compliance, Operations, and Privacy Cases. This updated layout helps to improve readability by organizing your reports into clearly defined sections.


</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Privacy Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Privacy Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Privacy Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Privacy Management by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Privacy Management by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Privacy Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Privacy Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Privacy Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Privacy Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Privacy Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   A new external Personal data rights \(PDR\) request form enables customers, ex-employees, and third parties to submit PDR requests from a website with email verification.
-   Access Control by Legal Entity feature enables teams to access only processing activities relevant to their legal entity, maintaining privacy by design principle.
-   Now Assist for Privacy Management plugin uses Generative AI to streamline privacy workflows by summarizing assessments, condensing issues, and merging control objectives.
-   Reporting privacy incidents through email feature enables employees to report privacy incidents directly through email.
-   Impacted and related areas configuration allows privacy case managers to add custom business area types to privacy cases for better context.
-   Revamped Processing Activity overview page provides a unified dashboard showing key compliance and risk metrics for processing activities.

 See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Configure the Personal Data Rights \(PDR\) external-facing form to map jurisdictions to data subject types and request types, and control whether an authorized agent can submit a request on behalf of a data subject.
-   Enable key stakeholders to view and update processing activities that they own directly from **GRC tasks** in the Employee Center.
-   Activate new ready-to-use privacy content, including risk statements and authority documents, such as Digital Personal Data Protection Act 2023 \(DPDPA\), the Virginia Consumer Data Protection Act, and the Colorado Privacy Act.
-   Automatically generate an AI-recommended privacy case summary from varied compliance case data, reducing investigation time and enabling faster, more consistent decision-making.
-   Anonymously report compliance violations through a secure portal that maintains complete identity protection while enabling organizational trust and regulatory compliance.

 See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

