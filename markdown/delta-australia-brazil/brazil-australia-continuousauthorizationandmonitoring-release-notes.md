---
title: Combined Continuous Authorization and Monitoring release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Continuous Authorization and Monitoring from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-continuousauthorizationandmonitoring-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Continuous Authorization and Monitoring release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Continuous Authorization and Monitoring from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Continuous Authorization and Monitoring release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Continuous Authorization and Monitoring to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Continuous Authorization and Monitoring.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Support for exporting and importing the OSCAL Assessment Results \(AR\) model](https://www.servicenow.com/docs/access?context=oscal-cam-ws&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, Continuous Authorization and Monitoring supports import and export of OSCAL data for Assessment Results \(AR\) format.

-   **[Skip attestations configuration for controls within a package](https://www.servicenow.com/docs/access?context=skip-attestations&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, skip the attestation stage at the package level and move controls directly from Draft to Review without completing the attestation workflow.

-   **[Control tailoring request enhancements](https://www.servicenow.com/docs/access?context=request-control-tailoring&family=australia&ft:locale=en-US)**

After upgrading to version 22.3.3, control tailoring requests support changes to overlay controls. You can add new overlay controls or modify existing ones within a control tailoring request.

-   **[OSCAL export and import enhancements](https://www.servicenow.com/docs/access?context=oscal-cam-ws&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, OSCAL import and export support additional details for various records, including status, frequency, weighting, implementation statement, control tailoring requests, overlays, and activities.

-   **[Support for exporting and importing the OSCAL Assessment Plan \(AP\) model](https://www.servicenow.com/docs/access?context=oscal-cam-ws&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, Continuous Authorization and Monitoring supports import and export of OSCAL data for Assessment Plan \(AP\) format.

-   **[Request control tailoring](https://www.servicenow.com/docs/access?context=request-control-tailoring&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, make incremental changes to control sets while preserving the state of unchanged controls without having to reset the entire package life cycle. Supported modifications include adding new controls, marking controls as not applicable, changing control allocation \(baseline to inherited or hybrid\), and modifying inheritance configurations.

-   **[Inherit from multiple providers](https://www.servicenow.com/docs/access?context=inherit-from-multiple-providers&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, Controls can inherit individual control requirements from multiple Common Control Providers \(CCPs\) across different authorization packages. Previously, inheritance was limited to a single provider per control, which required creating duplicate inherited controls when requirements came from different sources.

-   **[Control grid view](https://www.servicenow.com/docs/access?context=view-controls-in-grid-view&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, edit implementation statements and attestation respondents directly in a hierarchical data grid through the Controls tab in an authorization package.

-   **[Control tests grid view in Engagements](https://www.servicenow.com/docs/access?context=view-control-tests-in-grid-view&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, toggle between traditional related list and hierarchical data grid on the Control tests tab. Changes to assessment procedure effectiveness automatically cascade to parent control test effectiveness.

Package detail forms now use a structured vertical layout instead of the previous horizontal tab arrangement.

-   **[CAM workflow configuration enhancements](https://www.servicenow.com/docs/access?context=cam-workflow-configurator&family=australia&ft:locale=en-US)**

After upgrading to version 22.0.2, configure control button visibility, UI page access, and related list actions across different workflow steps. Previously, related list actions \(such as add or remove buttons for information types or baseline control actions\) required manual scripting to support custom workflows.

The following new state model attributes have been introduced:

    -   Required Authorization Documents Page
    -   Required Overlay Page
    -   Required Information Type Actions
    -   Required Baseline Actions
    -   Required Overlay Actions
    -   Request Control Tailoring
    -   Generate OSCAL AP
    -   Generate OSCAL AR

</td></tr><tr><td>

Brazil

</td><td>

-   **[Document reuse and version control across records](https://www.servicenow.com/docs/access?context=c_cam_document_management_system&family=brazil&ft:locale=en-US)**

Link documents as shared resources across authorization packages, boundaries, and engagements. Set approval workflows to control who reviews and activates documents before they take effect.

-   **[Analyze documents with AI](https://www.servicenow.com/docs/access?context=t_use_smart_docs_with_documents&family=brazil&ft:locale=en-US)**

Summarize documents, generate frequently asked questions with answers, or ask specific questions about document content, all from the Documents side panel in an authorization package, boundary, or engagement.

-   **[Voice-based document analysis](https://www.servicenow.com/docs/access?context=t_use_smart_docs_with_documents&family=brazil&ft:locale=en-US)**

Generate spoken audio summaries of documents and conduct voice-based Q&amp;A using the Voice Assist panel, from the Documents side panel in an authorization package, boundary, or engagement.

-   **[Connect documents to external cloud storage](https://www.servicenow.com/docs/access?context=t_connect_documents_to_external_cloud&family=brazil&ft:locale=en-US)**

Link documents from Google Drive, OneDrive, or SharePoint and keep them synchronized with authorization packages, boundaries, and engagements. Pull updates from cloud storage or push approved versions back, without manual downloads and uploads.

-   **[AI-generated authorization package summary](https://www.servicenow.com/docs/access?context=t_generate_authorization_package_summary&family=brazil&ft:locale=en-US)**

Using generative AI, the Authorization package summarization skill generates a summary of authorization package records. Each summary consolidates system purpose, impact level, operational status, and open POA&amp;M counts to show the package's current state.

-   **[POAM user role](https://www.servicenow.com/docs/access?context=cam-roles-list&family=brazil&ft:locale=en-US)**

Users with the POAM User role can view and update their assigned Plan of Action and Milestones \(POA&amp;Ms\), including viewing and updating tasks, accepting or rejecting acceptance tasks, and completing milestone tasks.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Continuous Authorization and Monitoring features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Properties page enhancements](https://www.servicenow.com/docs/access?context=cam-system-properties&family=australia&ft:locale=en-US)**

The Properties page includes new configuration options:

    -   Use **Homepage Title** to customize the workspace homepage name.
    -   The **Days Before Next Authorization** property is now available on the UI page.

</td></tr><tr><td>

Brazil

</td><td>

-   **[OSCAL enhancements](https://www.servicenow.com/docs/access?context=oscal-cam-ws&family=brazil&ft:locale=en-US)**

The OSCAL enhancements include:

    -   Import system-generated authority documents \(SSP, POA&amp;M, SAR, SAP, ATO Letter, Executive Summary reports\) and user-attached files at Authorization Package and Authorization Boundary levels during OSCAL import.
    -   Control objective IDs include source values during OSCAL import and export.
    -   Policy fields are included during OSCAL import and export.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Continuous Authorization and Monitoring features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Continuous Authorization and Monitoring features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Continuous Authorization and Monitoring.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install Continuous Authorization and Monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Continuous Authorization and Monitoring is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Continuous Authorization and Monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


Continuous Authorization and Monitoring is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Continuous Authorization and Monitoring we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Continuous Authorization and Monitoring we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Continuous Authorization and Monitoring, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Continuous Authorization and Monitoring we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Continuous Authorization and Monitoring we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Import and export OSCAL data for Assessment Plan \(AP\) and Assessment Results \(AR\) formats to streamline compliance reporting.
-   Skip the attestation stage for all controls in a package and move controls directly to the Monitor step to accelerate package progression.
-   Populate additional control fields when importing and exporting OSCAL data for SSP, AP, and AR formats to capture richer compliance details.
-   Raise control tailoring requests to make incremental changes to control sets in authorized packages without resetting the entire package life cycle.

 See [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Applies a standardized approach to automate the NIST Risk Management Framework, a U.S. Federal mandate for information system security.
-   Defines clear accountability across System Owners, Authorizing Officials, Security Control Assessors, Information System Security Officers, and other roles
-   Provides continuous monitoring and centralized management of NIST RMF compliance, including control implementation and assessment, authorization boundaries and impact levels, and Plans of Action &amp; Milestones \(POA&amp;M\)

 See [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

