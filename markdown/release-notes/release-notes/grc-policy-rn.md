---
title: Policy and Compliance Management release notes
description: The ServiceNow Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and benchmarks. Policy and Compliance Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Policy and Compliance Management release notes

The ServiceNow® Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and benchmarks. Policy and Compliance Management was enhanced and updated in the Australia release.

## Policy and Compliance Management highlights for the Australia release

-   Enable personal authentication for policy authoring in Microsoft SharePoint and Google Drive to register policy documents under the logged-in user's identity instead of a shared service account.
-   Access Policy and Compliance Management dashboards directly from the Compliance Workspace, without installing Platform Analytics application.
-   Manage control objective changes through a structured workflow without affecting the active published record.
-   Rationalize UCF and non-UCF control objectives together in a single rationalization process.
-   Email notification links redirect users to their appropriate workspace based on their assigned roles.

See [Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/r_PolicyComplianceMgmt.md) for more information.

**Important:** Policy and Compliance Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Personal authentication and document access permissions in policy authoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/personal-auth-and-document-access-policy-authoring.md)**

    After upgrading Policy and Compliance Management to 22.3.2, you can enable personal authentication for policy authoring in Microsoft SharePoint and Google Drive. When enabled, policy authoring uses a hybrid authentication model. Create, connect, and upload operations run under the logged-in user's personal credentials, while document access permission grants and content sync always run under the shared service account. This approach supports audit traceability at the individual user level for document operations and keeps access management and sync consistent regardless of who initiates them.


-   **[Dashboard access from Compliance Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/view-dashboards-in-compliance-workspace.md)**

    After upgrading to 22.3.2, you can access Policy and Compliance Management dashboards directly from the Compliance Workspace.

    The following dashboards are available:

    -   Compliance Overview
    -   Policy Acknowledgement
    -   Policy Exception Overview
    -   Policy Overview
    These dashboards are also accessible from the Platform Analytics application.


-   **[Assessment template versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/template-versioning.md)**

    After upgrading Policy and Compliance Management to 22.3.2, CRI tiering questionnaire, CRI profile assessment, and control assessment templates support versioning. Template managers can create and publish new versions of these templates over time. When a CRI tiering questionnaire, CRI profile assessment, or control assessment is initiated, the assessment is generated using the latest published version of the template.


-   **[Role-based workspace redirection for email notification links](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-tasks-pol-comp-ws.md)**

    After upgrading Policy and Compliance Management to 22.3.2, email notification links for Policy and Compliance Management records redirect users to their appropriate workspace based on their assigned roles. Users without a workspace role are redirected to the GRC Task Page, or to the classic UI if the common workspace is not installed. The following record types support workspace redirection: Controls, Evidence, Control risk indicators, Indicator task, Policy acknowledgments, and Policy exceptions.


-   **[Control objective workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/concept_cob_workflow.md)**

    After upgrading Policy and Compliance Management to 22.0.1, the new Control objective workflow feature introduces a structured lifecycle for managing control objective records. Enable this feature using the **Enable Control Objective Workflow** property under **Policy and Compliance** &gt; **All** &gt; **Properties** and is disabled by default.

    -   When disabled, only the State field is added to control objective records. Active records show Published, inactive records show Retired, and new records default to Draft.
    -   When enabled, control objectives move through: Draft, Review, Approved, Current version, and Retired. The following new fields are also introduced: State, Effective date, Revision type, and Record nature.
    -   Editing a published control objective creates a working draft, keeping the published record active until approved changes are published.
    -   Users must select a revision type: Major or Minor. A Major revision moves associated controls back to Draft. A Minor revision applies updates without moving controls back to Draft.
    -   The Owner and Owning Group fields control who can edit the control objective and perform workflow actions.
-   **[Rationalizing control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/take-actions-on-the-recommendations-for-similar-control-objectives.md)**

    After upgrading Policy and Compliance Management to 22.0.1, both Unified Compliance Framework \(UCF\) control objectives and non-UCF control objectives can be rationalized together.

    -   Recommendation cards show a Source field to indicate whether it originates from UCF or a non-UCF source.
    -   As UCF control objectives cannot be deactivated, the Identify Duplicates and Finalize sub-states guide the users to retain the UCF control objective. Any UCF recommendations that are not retained are automatically dismissed when the user requests review.
    -   Only one UCF control objective can be retained at a time. If you retain a different UCF control objective, the previously retained one is automatically dismissed.
    -   When rationalization is complete, the retained UCF control objective stays active, accepted non-UCF recommendations are deactivated, and any dismissed UCF control objectives remain active and unchanged.

## UI changes

-   **[SAE columns in Control Attestations list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/c_Attestations.md)**

    The Control Attestations list view now displays the Control and Entity columns, showing the control name and associated entity for each assessment instance. These columns are visible on the Compliance Workspace, Tasks page, Employee Center, and Risk Portal.


## Changed in this release

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Activation information

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Policy and Compliance Management supports the latest public release and the two preceding versions of the following web browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

