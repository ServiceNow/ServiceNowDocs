---
title: Digital Product Release release notes
description: ServiceNow Digital Product Release is a release management solution that helps release managers, product managers, and program managers manage the release process. See the following sections for release notes by version.Digital Product Release version 2.6.2 includes restricted release access, an on-hold release state, planned and actual phase dates, configurable dashboards, and other enhancements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/digital-product-release-rn.html
release: australia
topic_type: topic
last_updated: "2026-10-05"
reading_time_minutes: 3
keywords: [Digital Product Release release notes, DPR release notes, Digital Product Release release notes]
breadcrumb: [IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Digital Product Release release notes

ServiceNow® Digital Product Release is a release management solution that helps release managers, product managers, and program managers manage the release process. See the following sections for release notes by version.

## About Digital Product Release

-   Plan, validate, and track product releases in one workspace, so product teams share a single view of release readiness.
-   Gate release progression with policies that evaluate data from the AI Platform and from connected planning and CI/CD tools.
-   Restrict release visibility to the teams that own a release, and inherit that access down to release phases, phase tasks, and linked records.
-   Hand a validated release to Change Management, so change approval focuses on deployment scheduling and service impact.

For more information, see .

## Activation and other requirements

**Note:** Digital Product Release is available from the ServiceNow Store. See the activation information that follows.

-   **Activation information**

    Install Digital Product Release by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    For more information, see .


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/it-service-management-rn-landing.md)

## Version 2.6.2

Digital Product Release version 2.6.2 includes restricted release access, an on-hold release state, planned and actual phase dates, configurable dashboards, and other enhancements.

### What's new

-   **Restricted access to releases**

    Limit who can see a release to its release team. Restricted access adds record-level control and applies to releases, release phases, release tasks, policy mappings, key dates, and release phase relationships.

    Configure a product team on the Product Settings page to apply restricted access on its releases. For more information, see .

    A release created for a restricted-access product inherits its setting, and the product team is set to its initial release team.

    In a multi-product release, individual releases inherit access control from the main release.

-   **On hold release state**

    Pause a release for a business reason without cancelling it or losing its place in the release life cycle. While a release is on hold, you can't complete the current phase and automatic phase progression does not run. Resume the release after the reason for the hold is resolved, or cancel it.

-   **Planned and actual phase dates in stage-based release**

    Track planned and actual start and end dates for stage-based release phases. You enter the planned dates; the actual dates are set automatically as the phase progresses.

-   **System properties for the default phase association**

    Control which phase is pre-selected when you associate a change or configuration item with a release. Configure **sn\_dpr.default\_phase\_for\_changes** for changes and **sn\_dpr.default\_phase\_for\_cis** for configuration items.


### What's changed

-   **Charts exclude cancelled phases from the release dashboards**

    Policies, phase tasks, and task approvals attached to a cancelled or restarted release phase are excluded from chart aggregates. They are also filtered out from the lists that opens on selecting a chart segment. This applies to the Digital Product Release landing page, Release Overview, Release Bundle Details, and the multi-product release dashboard.

-   **Digital Product Release home page widgets scoped to your releases**

    The **My releases** chart on the Digital Product Release Workspace home page shows only releases where you're the release owner or a release team member.

-   **Release actions on all release pages**

    From any release page, perform actions such as **Start release**, **Re-target release**, **Close release**, **Complete current phase**, and **Run policies**.

-   **Release template**

    The **Manage release template** button on the Release template form is renamed **Edit release template**.

-   **Release creation wizard**

    Additional Products fields are no longer required in the Create release flow.

-   ****

    In a multi-product release, the policy status of a product added after the release starts rolls up to the main release.

-   **Product enhancement creation**

    The **sn\_dpr\_workspace.enhancement\_work\_item\_types** system property controls which work item types auto-create product enhancements. Leave it empty to stop enhancement creation.


### What's deprecated or removed

-   **Auto create enhancement from primary epic system property**

    The `sn_dpr_workspace.auto_create_product_enhancement_for_primary_epic` property is removed. Use `sn_dpr_workspace.enhancement_work_item_types` instead.


