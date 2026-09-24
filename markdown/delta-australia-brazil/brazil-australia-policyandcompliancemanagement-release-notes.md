---
title: Combined Policy and Compliance Management release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Policy and Compliance Management from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-policyandcompliancemanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Policy and Compliance Management release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Policy and Compliance Management from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Policy and Compliance Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Policy and Compliance Management to Brazil

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

Between your current release family and Brazil, new features were introduced for Policy and Compliance Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Personal authentication and document access permissions in policy authoring](https://www.servicenow.com/docs/access?context=personal-auth-and-document-access-policy-authoring&family=australia&ft:locale=en-US)**

After upgrading Policy and Compliance Management to 22.3.2, you can enable personal authentication for policy authoring in Microsoft SharePoint and Google Drive. When enabled, policy authoring uses a hybrid authentication model. Create, connect, and upload operations run under the logged-in user's personal credentials, while document access permission grants and content sync always run under the shared service account. This approach supports audit traceability at the individual user level for document operations and keeps access management and sync consistent regardless of who initiates them.


 -   **[Dashboard access from Compliance Workspace](https://www.servicenow.com/docs/access?context=view-dashboards-in-compliance-workspace&family=australia&ft:locale=en-US)**

After upgrading to 22.3.2, you can access Policy and Compliance Management dashboards directly from the Compliance Workspace.The following dashboards are available:

    -   Compliance Overview
    -   Policy Acknowledgement
    -   Policy Exception Overview
    -   Policy Overview
These dashboards are also accessible from the Platform Analytics application.


 -   **[Assessment template versioning](https://www.servicenow.com/docs/access?context=template-versioning&family=australia&ft:locale=en-US)**

After upgrading Policy and Compliance Management to 22.3.2, CRI tiering questionnaire, CRI profile assessment, and control assessment templates support versioning. Template managers can create and publish new versions of these templates over time. When a CRI tiering questionnaire, CRI profile assessment, or control assessment is initiated, the assessment is generated using the latest published version of the template.


 -   **[Role-based workspace redirection for email notification links](https://www.servicenow.com/docs/access?context=grc-tasks-pol-comp-ws&family=australia&ft:locale=en-US)**

After upgrading Policy and Compliance Management to 22.3.2, email notification links for Policy and Compliance Management records redirect users to their appropriate workspace based on their assigned roles. Users without a workspace role are redirected to the GRC Task Page, or to the classic UI if the common workspace is not installed. The following record types support workspace redirection: Controls, Evidence, Control risk indicators, Indicator task, Policy acknowledgments, and Policy exceptions.


 -   **[Control objective workflow](https://www.servicenow.com/docs/access?context=concept_cob_workflow&family=australia&ft:locale=en-US)**

After upgrading Policy and Compliance Management to 22.0.1, the new Control objective workflow feature introduces a structured lifecycle for managing control objective records. Enable this feature using the **Enable Control Objective Workflow** property under **Policy and Compliance** &gt; **All** &gt; **Properties** and is disabled by default.

    -   When disabled, only the State field is added to control objective records. Active records show Published, inactive records show Retired, and new records default to Draft.
    -   When enabled, control objectives move through: Draft, Review, Approved, Current version, and Retired. The following new fields are also introduced: State, Effective date, Revision type, and Record nature.
    -   Editing a published control objective creates a working draft, keeping the published record active until approved changes are published.
    -   Users must select a revision type: Major or Minor. A Major revision moves associated controls back to Draft. A Minor revision applies updates without moving controls back to Draft.
    -   The Owner and Owning Group fields control who can edit the control objective and perform workflow actions.
-   **[Rationalizing control objectives](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&family=australia&ft:locale=en-US)**

After upgrading Policy and Compliance Management to 22.0.1, both Unified Compliance Framework \(UCF\) control objectives and non-UCF control objectives can be rationalized together.

    -   Recommendation cards show a Source field to indicate whether it originates from UCF or a non-UCF source.
    -   As UCF control objectives cannot be deactivated, the Identify Duplicates and Finalize sub-states guide the users to retain the UCF control objective. Any UCF recommendations that are not retained are automatically dismissed when the user requests review.
    -   Only one UCF control objective can be retained at a time. If you retain a different UCF control objective, the previously retained one is automatically dismissed.
    -   When rationalization is complete, the retained UCF control objective stays active, accepted non-UCF recommendations are deactivated, and any dismissed UCF control objectives remain active and unchanged.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Policy and Compliance Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[ServiceNow Otto® name announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.The Now Assist for IRM \(sn\_irm\_gen\_ai\) plugin, which provides generative AI capabilities for RCM, has been renamed to ServiceNow Otto for IRM.


 -   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 -   **[SAE columns in Control Attestations list view](https://www.servicenow.com/docs/access?context=c_Attestations&family=australia&ft:locale=en-US)**

The Control Attestations list view now displays the Control and Entity columns, showing the control name and associated entity for each assessment instance. These columns are visible on the Compliance Workspace, Tasks page, Employee Center, and Risk Portal.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Policy and Compliance Management features or functionality were removed.

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

Between your current release family and Brazil, some Policy and Compliance Management features or functionality were deprecated.

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

Review information on how to activate Policy and Compliance Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Policy and Compliance Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Policy and Compliance Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Policy and Compliance Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Browser requirements**

Policy and Compliance Management supports the latest public release and the two preceding versions of the following web browsers:

    -   Google Chrome
    -   Firefox and Firefox Extended Support Release \(ESR\)
    -   Microsoft Edge Chromium
    -   Safari 12.0 and later versions

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Policy and Compliance Management, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Policy and Compliance Management we have noted them here.

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

If there are specific highlight considerations for Policy and Compliance Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   ServiceNow Otto is the new name for the Now Assist experience, delivering agentic AI, multimodal interactions, and autonomous cross-system workflow orchestration.
-   Enable personal authentication for policy authoring in Microsoft SharePoint and Google Drive to register policy documents under the logged-in user's identity instead of a shared service account.
-   Access Policy and Compliance Management dashboards directly from the Compliance Workspace, without installing Platform Analytics application.
-   Manage control objective changes through a structured workflow without affecting the active published record.
-   Rationalize UCF and non-UCF control objectives together in a single rationalization process.
-   Email notification links redirect users to their appropriate workspace based on their assigned roles.

 See [Policy and Compliance Management](https://www.servicenow.com/docs/access?context=r_PolicyComplianceMgmt&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

