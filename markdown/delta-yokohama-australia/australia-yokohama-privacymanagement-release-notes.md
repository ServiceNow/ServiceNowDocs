---
title: Combined Privacy Management release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Privacy Management from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-privacymanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Privacy Management release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Privacy Management from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Privacy Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Privacy Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

-   **[\[Placeholder link text to key bundle-grc.configure-criticality-factors\]](https://www.servicenow.com/docs/access?context=configure-criticality-factors&family=yokohama&ft:locale=en-US)**

Leverage criticality factors to evaluate the initial risks associated with processing activities. Integrate these factors into privacy assessments and automatically generate a criticality score upon assessment approval. These factors are also added to processing activities, enabling you to make updates at any time. Integrating these factors in a privacy assessment eliminates the need for a separate criticality assessment. This consolidation reduces the workload for the privacy teams.

-   **[Smart assessments](https://www.servicenow.com/docs/access?context=smart-assessments-in-privacy-management&family=yokohama&ft:locale=en-US)**

Use the new and improved assessment experience that enables:

    -   capturing the data elements, the information object attributes, hierarchies
    -   building the assessment questionnaire
This new experience enables responders to update all the necessary details within the assessments, eliminating the need to update the processing activity separately.

-   **[Configure categories](https://www.servicenow.com/docs/access?context=configure-information-object-categories&family=yokohama&ft:locale=en-US)**

Implement Information object categories to tag and classify information objects effectively. For example, attributes like iris scans and fingerprints are often referred to as biometric data, or email addresses and phone numbers can be tagged as contact information. Information object categories enable you to categorize these information objects under these broader classifications. This approach is useful in the following ways:

    -   Enhances compliance with regulations such as GDPR, CCPA, and so on by accurately capturing and tracking required data categories.
    -   Improves clarity for business users, ensuring they can easily identify and work with terms they’re familiar with while adhering to regulatory standards.
    -   Streamlines data governance by creating a structured framework that supports both regulatory needs and business operations.
-   **[Smart assessment for privacy case management action tasks](https://www.servicenow.com/docs/access?context=accept-a-case-task&family=yokohama&ft:locale=en-US)**

Use the new assessment experience of Smart Assessment Engine for privacy case action tasks. Only when an action task moves from the **Draft** to the **Assigned** state, the assessment can be sent. To use the smart assessment, a new property called enable\_smart\_assessments \(sn\_grc\_case\_mgmt.enable\_smart\_assessments\) is introduced with the default value as **true**.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Data subjects](https://www.servicenow.com/docs/access?context=data-subjects&family=zurich&ft:locale=en-US)**

Select and define the multiple data subject types for each processing activity. You can capture the volume of data subjects that were processed, the specific data elements that were collected from the users, and the user locations. With this feature, you get a realistic, granular, and scalable representation of your processing activities.

-   **[Privacy management dashboard](https://www.servicenow.com/docs/access?context=privacy-manager-dashboard&family=zurich&ft:locale=en-US)**

Get an overview of your complete privacy risk and compliance posture from the Privacy Management dashboard so that you can quickly prioritize and remediate your processing activities. By looking at the Processing Activities, Risk &amp; Compliance, and Operations &amp; Case management sections, you can see the overall compliance score, trends, privacy criticality assessment scores, and risk heatmap. From the dashboard, you can also see information about the global legal framework to understand the regional obligations and the built-in risk metrics that automatically assess each processing activity.

-   **[New screening and PIA templates](https://www.servicenow.com/docs/access?context=privacy-mgmt-workflow&family=zurich&ft:locale=en-US)**

Use the new Privacy Impact Assessments \(PIAs\) and Screening Assessment templates that provide standardized questions, evaluation criteria, and workflows so that you can perform a processing activity criticality and privacy risk assessment. With these new templates, you can ensure consistency, reduce manual effort, and support compliance with regulatory and organizational requirements.


 -   **[PDR external-facing form](https://www.servicenow.com/docs/access?context=pdr-external-facing&family=zurich&ft:locale=en-US)**

A new external-facing form for personal data rights \(PDR\) requests is now available, enabling customers, ex-employees, and third party individuals to initiate PDR requests directly from a company's website, without needing Employee Center access. The form allows users to submit various requests, including Right to Know, Right to Delete, Right to Correct, and Right to Opt-Out, with the flexibility to add additional request types as required. An email-based verification process ensures security before processing the PDR request. The PDR form is customizable and can be easily embedded on external sites.


 -   **[Access control by legal entity](https://www.servicenow.com/docs/access?context=access-control-by-legal-entity&family=zurich&ft:locale=en-US)**

The Access control by legal entity feature allows teams to access processing activities relevant only to their legal entity. This ensures teams view only their own records, maintaining adherence to the privacy by design principle. By limiting access according to legal entities, this feature reduces operational risks and enables organizations to manage privacy requests and regulatory compliance effectively.


 -   **[ServiceNow Otto for Privacy Management](https://www.servicenow.com/docs/access?context=now-assist-for-privacy-management&family=zurich&ft:locale=en-US)**

Now Assist for Privacy Management leverages GenAI to support privacy workflows by summarizing risk assessments, condensing issue details, and identifying redundant control objectives and merging them into a common control objective. Now Assist for Privacy Management is delivered as a separate plugin, requiring administrators to activate specific skills and assign the new sn\_prm\_gen\_ai.user role to access these features.


 -   **[Report a privacy case through email](https://www.servicenow.com/docs/access?context=add-issues-email&family=zurich&ft:locale=en-US)**

Employees can now report privacy incidents directly through email, eliminating the need for complex forms or portals. This enhancement simplifies the reporting process, enabling faster case handling and efficient tracking of privacy issues.


 -   **[Impacted and related areas configuration](https://www.servicenow.com/docs/access?context=configure-record-type-area&family=zurich&ft:locale=en-US)**

The Record Type Configuration feature allows privacy case managers or analysts to add additional relevant business area types in impacted and related areas. When creating or updating a privacy case, users can select from pre-defined options to add these areas, ensuring that each case accurately reflects its business context.


</td></tr><tr><td>

Australia

</td><td>

-   **[Case summarization for privacy cases](https://www.servicenow.com/docs/access?context=privacy-case-summarization-skill&family=australia&ft:locale=en-US)**

Privacy analysts can now use the Now Assist case summarization feature to quickly understand a privacy case without manually reviewing every field or related list. Now Assist analyzes key case attributes, such as timelines, impacted areas, evidence, and actions, and generates a structured summary directly inside the privacy case. This feature solves a common problem: case data is often lengthy, scattered across multiple related lists, and difficult for analysts to digest efficiently. Analysts can also save and edit summaries as case data evolves, ensuring the record stays current.

-   **[Report a privacy case anonymously](https://www.servicenow.com/docs/access?context=report-privacy-case-anonymously&family=australia&ft:locale=en-US)**

Employees can now use the Anonymous Reporting Center to report privacy violations such as data breaches or exposure, unauthorized data use, privacy law violations \(GDPR, CCPA\), or other privacy-by-design lapses without revealing their identity or location.Accessed through the Employee Center, the Anonymous Reporting Center portal automatically logs users out to enforce anonymity, creates case records without mapping to employee identity, and provides a unique report key for secure follow-up communication.Reports are routed to the appropriate compliance team based on the nature of the concern. Throughout the investigation process:

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

Yokohama

</td><td>

-   **[Tagging of information object tags](https://www.servicenow.com/docs/access?context=tag-io-with-pi&family=yokohama&ft:locale=en-US)**

Use the **Data classification** field to tag information objects instead of using the tag icon.

-   **[Initiating privacy assessment](https://www.servicenow.com/docs/access?context=send-privacy-asmt-from-pa&family=yokohama&ft:locale=en-US)**

When you initiate a privacy assessment from either an entity or a processing activity, you’re no longer redirected to the **Create new privacy assessment form**, instead, a new pop-up window appears where you can specify all the assessment details.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Some generative AI skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Privacy Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

-   **Activation information**

Install Privacy Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Privacy Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Privacy Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Privacy Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

-   Integrate criticality factors into assessments and processing activities thereby simplifying the assessment process, and reducing the workload for privacy teams.
-   Use the Smart Assessment Engine to capture details regarding information objects and hierarchies, updating all details within the assessments and eliminating the need to separately update processing activities.
-   Implement information Object \(IO\) categories such as biometric data, to align with regulatory classifications and bridge the gap between requirements and user understanding.
-   Empower privacy case analysts to perform assessments on privacy cases using the Smart Assessment Engine

 See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

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

-   ServiceNow Otto is the new name for the Now Assist experience, delivering agentic AI, multimodal interactions, and autonomous cross-system workflow orchestration.
-   Configure the Personal Data Rights \(PDR\) external-facing form to map jurisdictions to data subject types and request types, and control whether an authorized agent can submit a request on behalf of a data subject.
-   Enable key stakeholders to view and update processing activities that they own directly from **GRC tasks** in the Employee Center.
-   Activate new ready-to-use privacy content, including risk statements and authority documents, such as Digital Personal Data Protection Act 2023 \(DPDPA\), the Virginia Consumer Data Protection Act, and the Colorado Privacy Act.
-   Automatically generate an AI-recommended privacy case summary from varied compliance case data, reducing investigation time and enabling faster, more consistent decision-making.
-   Anonymously report compliance violations through a secure portal that maintains complete identity protection while enabling organizational trust and regulatory compliance.

 See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

