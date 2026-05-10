---
title: Policy and Compliance Management release notes
description: The ServiceNow Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and benchmarks. Policy and Compliance Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Policy and Compliance Management release notes

The ServiceNow® Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and benchmarks. Policy and Compliance Management was enhanced and updated in the Australia release.

## Policy and Compliance Management highlights for the Australia release

-   Manage control objective changes through a structured workflow without affecting the active published record.
-   Rationalize UCF and non-UCF control objectives together in a single rationalization process.

See [Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/r_PolicyComplianceMgmt.md) for more information.

**Important:** Policy and Compliance Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Control objective workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/concept_cob_workflow.md)**

    After upgrading Policy and Compliance Management to 22.0.1, the new Control objective workflow feature introduces a structured lifecycle for managing control objective records. This feature is controlled by the Enable Control Objective Workflow property under Policy and Compliance &gt; Properties and is disabled by default.

    Key highlights:

    -   When disabled, only the State field is added to control objective records. Active records show Published, inactive records show Retired, and new records default to Draft.
    -   When enabled, control objectives move through: Draft, Review, Approved, Current version, and Retired. The following new fields are also introduced: State, Effective date, Revision type, and Record nature.
    -   Editing a published control objective creates a working draft, keeping the published record active until approved changes are published.
    -   Users must select a revision type: Major or Minor. A Major revision moves associated controls back to Draft. A Minor revision applies updates without moving controls back to Draft.
    -   The Owner and Owning Group fields control who can edit the control objective and perform workflow actions.
-   **[Rationalizing control objectives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/take-actions-on-the-recommendations-for-similar-control-objectives.md)**

    After upgrading Policy and Compliance Management to 22.0.1, both Unified Compliance Framework \(UCF\) control objectives and non-UCF control objectives can be rationalized together. Key highlights include:

    -   Recommendation cards show a Source field to indicate whether it originates from UCF or a non-UCF source.
    -   As UCF control objectives cannot be deactivated, the Identify Duplicates and Finalize sub-states guide the users to retain the UCF control objective. Any UCF recommendations that are not retained are automatically dismissed when the user requests review.
    -   Only one UCF control objective can be retained at a time. If you retain a different UCF control objective, the previously retained one is automatically dismissed.
    -   When rationalization is complete, the retained UCF control objective stays active, accepted non-UCF recommendations are deactivated, and any dismissed UCF control objectives remain active and unchanged.

## Activation information

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Policy and Compliance Management supports the latest public release and the two preceding versions of the following web browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

