---
title: Combined Compliance Case Management release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Compliance Case Management from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-compliancecasemanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Compliance Case Management release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Compliance Case Management from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Compliance Case Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Compliance Case Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Between your current release family and Australia, new features were introduced for Compliance Case Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Regulatory Agency Library](https://www.servicenow.com/docs/access?context=regulatory-agency-library-rcm&family=xanadu&ft:locale=en-US)**

Establish a centralized library of agencies for identifying the relevant regulatory authorities that are responsible for overseeing particular industries or sectors within each jurisdiction. The centralized library consolidates all the regulatory communications via emails and implements the notification rules for the data privacy or security breaches for the reported compliance cases.

-   **[Auto-calculate future dates](https://www.servicenow.com/docs/access?context=auto-calculate-future-dates&family=xanadu&ft:locale=en-US)**

Set up future auto-calculations to track your compliance cases or requests.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Smart assessments in Compliance Case Management](https://www.servicenow.com/docs/access?context=smart-assessment-in-ccm&family=yokohama&ft:locale=en-US)**

Utilize the Smart Assessment Engine to assess if your employees are compliant with the necessary regulations. The compliance case administrator configures the questionnaire, and when an action task moves from the **Draft** to the **Assigned** state, the assessment is sent. After the assessment, the compliance case manager examines the nature of the non-compliance and its impact on the organization. Based on the findings, appropriate remediation measures are identified and implemented to resolution. To use the smart assessment, a new property called enable\_smart\_assessments \(sn\_grc\_case\_mgmt.enable\_smart\_assessments\) is introduced with the default value as **true**.

-   **[Unified Task-driven UI experience](https://www.servicenow.com/docs/access?context=perform-smart-assessment-on-action-task&family=yokohama&ft:locale=en-US)**

As a business user, use the **Tasks** page on the Employee Center for a consolidated view of all your tasks, enabling you to access and complete them efficiently. This page provides an easy way to manage all your assessments in one place, enabling you to view and perform tasks seamlessly.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[Report a compliance case anonymously](https://www.servicenow.com/docs/access?context=report-compliance-case-anonymously&family=australia&ft:locale=en-US)Report compliance cases anonymously**

Employees can now use the Anonymous Reporting Center to report compliance violations such as fraud and embezzlement, workplace misconduct \(harassment, discrimination\), bribery and corruption, and other concerns without revealing their identity or location.

Accessed through the Employee Center, the Anonymous Reporting Center portal automatically logs users out to enforce anonymity, creates case records without mapping to employee identity, and provides a unique report key and report number for secure follow-up communication.

CAPTCHA‑based verification is used to authenticate submissions, and the system generates a report statement summarizing the case after submission. Employees can save a copy of their report for future reference. For security and confidentiality, the submitted information is not displayed again. Reports are routed to the appropriate compliance team based on the nature of the concern.

Throughout the investigation process:

    -   Investigators can request additional information through a comments system visible to the reporter
    -   Reporters can follow up on their case using their report key to check progress and respond to questions
    -   All interactions maintain reporter anonymity at every step; no identity or location data is ever captured or linked
This enhancement enables organizations to build trust, mitigate risks before escalation, and ensures regulatory compliance with whistleblower protection requirements.

-   **[Case summarization for compliance cases](https://www.servicenow.com/docs/access?context=compliance-case-summarization-skill&family=australia&ft:locale=en-US)AI-driven compliance case summarization**

After upgrading Now Assist for Integrated Risk Management \(IRM\) application to version 22.x, Compliance analysts can use the case summarization feature to quickly understand a compliance case without manually reviewing every field, attachment, or related list. Now Assist analyzes key case attributes—such as timelines, impacted areas, evidence, and actions—and generates a structured summary directly inside the compliance case.

This solves a common problem: case data is often lengthy, scattered across multiple related lists, and difficult for analysts to digest efficiently. Analysts can also save and edit summaries as case data evolves, ensuring the record stays current.

By consolidating all relevant information into a single, coherent narrative, Now Assist reduces investigation time, improves consistency across reviewers, and supports faster decision-making.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Compliance Case Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

A new graphical chart enables your compliance case managers to monitor and access their compliance cases by the subtype classification.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Roles updated for smart assessment](https://www.servicenow.com/docs/access?context=roles-compliance-case-management&family=yokohama&ft:locale=en-US)**

The following roles in Compliance Case Management have been updated with respect to smart assessments.

    -   sn\_comp\_case.compliance\_case\_admin
    -   sn\_comp\_case.compliance\_case\_analyst
    -   sn\_comp\_case.compliance\_case\_business\_user
    -   sn\_comp\_case.compliance\_case\_manager
-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US)**

The Compliance Management configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

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

Between your current release family and Australia, some Compliance Case Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Between your current release family and Australia, some Compliance Case Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Review information on how to activate Compliance Case Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install the Regulatory Agency Library by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Compliance Case Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

Install Compliance Case Management by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Compliance Case Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If any specific browser requirements were introduced or changed for Compliance Case Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Review details on accessibility information for Compliance Case Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US) for details.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Compliance Case Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If there are specific highlight considerations for Compliance Case Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Establish a centralized library of agencies for identifying the relevant regulatory authorities that are responsible for overseeing particular industries or sectors within each jurisdiction. The centralized library consolidates all regulatory communications via emails and implements the notification rules for data privacy or security breaches for the reported compliance cases.
-   Auto-calculate the notification dates for the reported compliance cases.
-   Monitor and access your compliance cases by the subtype classification through a new graphical chart.
-   Enable your compliance analysts to access a homepage so that your compliance analysts can manage reported compliance cases or requests.

 See [Compliance Case Management](https://www.servicenow.com/docs/access?context=compliance-case-management&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Empower compliance professionals to perform assessments on compliance cases using the Smart Assessment Engine.
-   Utilize the unified **Tasks** page on Employee Center to complete your assessments.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

 See [Compliance Case Management](https://www.servicenow.com/docs/access?context=compliance-case-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   Automatically generate an AI-recommended compliance case summary from varied compliance case data, reducing investigation time and enabling faster, more consistent decision-making.
-   Anonymously report compliance violations through a secure portal that maintains complete identity protection while enabling organizational trust and regulatory compliance.

 See [\[Placeholder link text to key compliance-case-management\]](https://www.servicenow.com/docs/access?context=compliance-case-management&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

