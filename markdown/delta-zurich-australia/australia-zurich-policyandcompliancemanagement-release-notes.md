---
title: Combined Policy and Compliance Management release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Policy and Compliance Management from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-policyandcompliancemanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Policy and Compliance Management release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Policy and Compliance Management from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Policy and Compliance Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Policy and Compliance Management to Australia

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

Between your current release family and Australia, new features were introduced for Policy and Compliance Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[GRC Approval Configurator](https://www.servicenow.com/docs/access?context=grc-approval-configurator-for-policy-extension-and-exception&family=zurich&ft:locale=en-US)**

The GRC Approval Configurator can now be used to manage both policy exception and extension approvals. It allows verification, approval, and extension rules to be defined based on state, sub-state, and other filter conditions, with support for multiple user groups and multi-level approvals. This enhancement provides greater flexibility in assigning appropriate approvers at each level based on defined conditions, facilitating structured and collaborative reviews. For extension approvals, users can now configure multiple approvers, overcoming the previous limitation of a single default approver \(Compliance Manager\).


 -   **[Common Control Objective Creation](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&family=zurich&ft:locale=en-US)**

Use Generative AI to merge similar control objectives into a single, consolidated common control objective. The system automatically populates the name, description, and guidance fields from the accepted duplicates, eliminating the need to manually select a primary control objective.


 -   **[Entity based record access rules to secure new records](https://www.servicenow.com/docs/access?context=c_GRCControls&family=zurich&ft:locale=en-US)**

When entity based record access rules are enabled on the Entity Based Access Configuration Properties page, any newly created controls, control attestations, indicators, and indicator tasks associated with a configured entity will automatically inherit the entity-based access \(EBA\) value from that entity. Previously, users had to run bulk access updates to apply EBA restrictions whenever new objects were created.

Additionally, when a standard control is converted to a common control, the **Entity based access restriction** option is inactive by default. Users can manually enable the EBA option for common controls directly from the Access Settings section in the Details tab of the respective control.


</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Policy and Compliance Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


 -   **[Improved widget presentation and page layouts](https://www.servicenow.com/docs/access?context=compliance-manager-compliance-ws&family=zurich&ft:locale=en-US)**

As part of the Coral theme enhancements, rounded card containers with drop shadows have been introduced for widgets across Compliance pages, and the gray background has been removed from the Compliance home page to simplify the interface.


 -   **[Tasks panel in Compliance Home page](https://www.servicenow.com/docs/access?context=compliance-manager-compliance-ws&family=zurich&ft:locale=en-US)**

The Tasks section has been removed from the Compliance Workspace to improve page performance.


 -   **[Improvements to the rationalization process of control objectives](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&family=zurich&ft:locale=en-US)**

Several enhancements have been made to the rationalization process:

    -   Redesigned the rationalization UI with a reordered layout and highlighted primary actions.
    -   Validations added for deactivated and deleted control objectives. Introduced the “Restart Analyze” option to support reevaluation of recommendations.
    -   Introduced support for Azure OpenAI, Amazon Bedrock, and Google Gemini for recommendations of control objectives.
    -   Updated the Consolidate state UI to show the recommendation panel with retained and accepted control objectives and their associated items.

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

Between your current release family and Australia, some Policy and Compliance Management features or functionality were removed.

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

Between your current release family and Australia, some Policy and Compliance Management features or functionality were deprecated.

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

Review information on how to activate Policy and Compliance Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Policy and Compliance Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Policy and Compliance Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Browser requirements**

Policy and Compliance Management supports the latest public release and the two preceding versions of the following web browsers:

    -   Google Chrome
    -   Firefox and Firefox Extended Support Release \(ESR\)
    -   Microsoft Edge Chromium
    -   Safari 12.0 and later versions

</td></tr><tr><td>

Australia

</td><td>

-   **Browser requirements**

Policy and Compliance Management supports the latest public release and the two preceding versions of the following web browsers:

    -   Google Chrome
    -   Firefox and Firefox Extended Support Release \(ESR\)
    -   Microsoft Edge Chromium
    -   Safari 12.0 and later versions

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Policy and Compliance Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

If there are specific localization considerations for Policy and Compliance Management we have noted them here.

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

If there are specific highlight considerations for Policy and Compliance Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Association of citations to controls feature enables users to associate controls with citations directly to avoid duplicated controls and ensure accurate compliance reporting.
-   Multiple enhancements to control objectives rationalization process, including improvements including automatic rationalization process creation, simplified two-step workflow for recommendations, skipped approvals for owner-reviewers, comment capabilities, and improved UI.
-   Now Assist for IRM includes skills and AI agent to identify affected control objectives when citation descriptions change and to provide suggested updates for review and approval.
-   Enhancements to control objectives and controls, including control objective requirements for granular statements, automatic control requirement generation, and attestation at control requirement level.
-   Enhancements to policy exception and extension requests, including approver pop-ups with key details, no indicator tasks for exempt controls, Send Information button for requesters, and expanded linking requirements for issue-based policy exceptions.

 See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   ServiceNow Otto is the new name for the Now Assist experience, delivering agentic AI, multimodal interactions, and autonomous cross-system workflow orchestration.
-   Enable personal authentication for policy authoring in Microsoft SharePoint and Google Drive to register policy documents under the logged-in user's identity instead of a shared service account.
-   Access Policy and Compliance Management dashboards directly from the Compliance Workspace, without installing Platform Analytics application.
-   Manage control objective changes through a structured workflow without affecting the active published record.
-   Rationalize UCF and non-UCF control objectives together in a single rationalization process.
-   Email notification links redirect users to their appropriate workspace based on their assigned roles.

 See [Policy and Compliance Management](https://www.servicenow.com/docs/access?context=r_PolicyComplianceMgmt&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

