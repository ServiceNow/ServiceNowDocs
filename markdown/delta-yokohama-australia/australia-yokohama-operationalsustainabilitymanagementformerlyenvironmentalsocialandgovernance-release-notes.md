---
title: Combined Operational Sustainability Management \(formerly Environmental, Social, and Governance\) release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-operationalsustainabilitymanagementformerlyenvironmentalsocialandgovernance-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Operational Sustainability Management \(formerly Environmental, Social, and Governance\) release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Operational Sustainability Management \(formerly Environmental, Social, and Governance\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Operational Sustainability Management \(formerly Environmental, Social, and Governance\) to Australia

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

Between your current release family and Australia, new features were introduced for Operational Sustainability Management \(formerly Environmental, Social, and Governance\).

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

-   **[Edit a calculated metric definition formula](https://www.servicenow.com/docs/access?context=edit-a-calculated-metric-definition-formula&family=australia&ft:locale=en-US)**

After upgrading GRC: Metrics to version 22.3.1, you can edit a calculated metric definition formula after it has been executed. When you save an edited formula, select a date from which the updated formula applies. Each saved edit creates a new formula version.

-   **[Microsoft Word based audit report templates using Document designer](https://www.servicenow.com/docs/access?context=document-designer-template&family=australia&ft:locale=en-US)**

After upgrading Document Designer to version 22.3.2, the Microsoft 365 reporting and Document Designer add-ins are consolidated into a single Document Designer plugin. A Create Claim button is added to the manifest. The repeater limit per document increases from 2 to 5, and the repetition limit per repeater increases from 200 to 500.

-   **[AI reporting assistant](https://www.servicenow.com/docs/access?context=ai-reporting-assistant&family=australia&ft:locale=en-US)**

After upgrading AI for Document Designer to version 22.3.3, you can use the AI reporting assistant in Document designer to generate report content from ServiceNow data using prompts directly within Microsoft Word. The assistant inserts the output into your document as stories, tables, charts, or data points.

-   **[Components installed with Environmental, Social, and Governance Management \(formerly ESG Management\)](https://www.servicenow.com/docs/access?context=components-installed-with-esg&family=australia&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.3.1, Operational Sustainability Management roles are mapped to Risk Library and Compliance Library feature roles to enforce functional domain separation. Users assigned these roles can access only risk and compliance records tagged to the functional domains they are authorized for.

-   **[Document intelligence for utility invoices](https://www.servicenow.com/docs/access?context=ai-driven-document-intelligence-for-utility-invoices&family=australia&ft:locale=en-US)**

After upgrading Now Assist for Operational Sustainability Management to version 22.0.1, unit values from invoices and updates metric data are extracted automatically, reducing manual data entry and improving data accuracy.

-   **[Integrating Environmental, Social, and Governance Management with Socialsuite](https://www.servicenow.com/docs/access?context=integrate-operational-sustainability-with-SocialSuite&family=australia&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.0.1, streamline sustainability reporting and compliance processes by conducting CSRD-compliant double materiality assessments in Socialsuite and automatically syncing the results with Operational Sustainability Management. This integration supports impact and financial materiality assessments following Global Reporting Initiative \(GRI\) and European Sustainability Reporting Standards \(ESRS\) standards.

-   **[Create a threshold for a metric](https://www.servicenow.com/docs/access?context=create-a-threshold-for-a-metric&family=australia&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.0.1, you can configure thresholds with multiple levels and ranges for granular monitoring. When thresholds are breached, automated actions trigger immediately.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Operational Sustainability Management \(formerly Environmental, Social, and Governance\) features.

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

-   **[Components installed](https://www.servicenow.com/docs/access?context=components-installed-with-grc&family=australia&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.3.1, role inheritance is updated to restrict access only to the resources required for each role. These changes apply to new installations only.

    -   The connection\_admin role is removed from sn\_esg.integration\_admin inheritance.
    -   The workspace\_user role is removed from Formula Builder configuration table access and from sn\_esg.reader and sn\_esg.data\_owner inheritance.
    -   The sn\_align\_core.ap\_read\_only role in sn\_esg.reader is replaced with sn\_ppm.reader.
    -   Read access to the sn\_esg\_gen\_ai\_emission\_calculation\_guidelines table is restricted to sn\_esg\_gen\_ai.cmd\_agent\_user.
    -   Metric reader access to Sustainable IT tables is restricted to required configuration tables only.
-   **[Configure templates](https://www.servicenow.com/docs/access?context=configure-template-for-document-designer&family=australia&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.3.2, the Business domain field in the Template configuration and Data relationship tables now references the GRC business domain \(sn\_grc\_business\_domain\). Previously, these fields referenced the M365 business domain.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Operational Sustainability Management \(formerly Environmental, Social, and Governance\) features or functionality were removed.

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

Between your current release family and Australia, some Operational Sustainability Management \(formerly Environmental, Social, and Governance\) features or functionality were deprecated.

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

Review information on how to activate Operational Sustainability Management \(formerly Environmental, Social, and Governance\).

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

Install Operational Sustainability Management by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) we have noted them here.

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

If any specific browser requirements were introduced or changed for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) we have noted them here.

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

Review details on accessibility information for Operational Sustainability Management \(formerly Environmental, Social, and Governance\), such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) we have noted them here.

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

If there are specific highlight considerations for Operational Sustainability Management \(formerly Environmental, Social, and Governance\) we have noted them here.

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

-   Edit calculated metric definition formulas after execution and apply updated formulas from a specific date, preserving historical data integrity with formula versioning.
-   The Microsoft 365 reporting add-in and the Document designer add-in are consolidated into a single Document designer plugin for streamlined sustainability reporting.
-   Use the AI reporting assistant in Document designer to generate report content from ServiceNow data using prompts directly within Microsoft Word.
-   Map Operational Sustainability Management roles to Risk Library and Compliance Library feature roles to control access to risk and compliance data based on functional domains.
-   Perform CSRD-compliant double materiality assessments in Socialsuite and automatically sync the results with the Operational Sustainability Management application.

 See [Environmental, Social, and Governance Management \(formerly Environmental, Social, and Governance\)](https://www.servicenow.com/docs/access?context=esg-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

