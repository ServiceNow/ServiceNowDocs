---
title: Combined Advanced Approval Management release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Advanced Approval Management from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-advancedapprovalmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Advanced Approval Management release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Advanced Approval Management from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Advanced Approval Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Advanced Approval Management to Australia

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

The default value for the **Rule order** field in a chain is now 10. If you have rule orders in chains configured with different order values, review and update them as needed to align with the new default.

 Assign the approval\_request\_submitter role to requesters who submit approval requests only and don't have access to the full advanced approval workflow functionality and interface. Users with this role can't recall recall or update approval requests. For more information, see [Components installed with Advanced Approval Management for Sales](https://www.servicenow.com/docs/access?context=components-installed-advanced-approval-management-for-sales&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Advanced Approval Management.

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

-   **Approval duration on approval cards**

As an approver or requester, view the amount of time that has elapsed for an approval step in a Requested or Escalated state. The time amount is highlighted and displayed in

    -   Hours, if the duration is under 24 hours
    -   Days and hours, if the duration is under seven days
    -   Weeks and days, if the duration is over seven days
The elapsed time starts when the approval request is submitted or when an escalation is triggered based on escalation rules.

-   **[Add ad-hoc approvers to approval chains](https://www.servicenow.com/docs/access?context=add-approver&family=australia&ft:locale=en-US)**

As a requester or approver, insert an ad-hoc approver at a specific position within an existing approval chain. The approval engine validates the position to prevent insertion before already requested or completed approvals. Ad-hoc approvers are clearly identified in the chain view and receive approval notifications with requester comments.

-   **[Recall an approval request from the quote header](https://www.servicenow.com/docs/access?context=submitting-approval-requests&family=australia&ft:locale=en-US)**

Enable requesters to recall submitted approval requests directly from the quote header in the quote workflow, without navigating to the Approvals tab.

-   **[Rejection reason in Approvals tab](https://www.servicenow.com/docs/access?context=approving-approval-requests&family=australia&ft:locale=en-US)**

Inform approval requesters of rejected approval requests by displaying the rejection reason near the related step card in the Approvals tab of the entity. Displaying the rejection reason helps requesters understand the issue with the request, without contacting approvers for clarification.

-   **[Configure delegate approvers](https://www.servicenow.com/docs/access?context=configure-approval-delegation&family=australia&ft:locale=en-US)**

Configure the delegation rules allowing delegate approvers to approve or reject approval requests. Delegate approvers can approve or reject a request directly from the approval step card in the Approvals tab, on behalf of the original approver.

-   **[Flexible approval configurations](https://www.servicenow.com/docs/access?context=configuring-advanced-approval-management&family=australia&ft:locale=en-US)**

Build workflows that enable sequential approvals, parallel \(simultaneous\) approvals, or a combination of both.

    -   Define workflow approval steps and optional chains that progress through multiple approval levels based on rule evaluations.
    -   Set the approval order using combinations of levels, roles, and conditions.
    -   Define approval users and groups.
    -   Consolidate multiple email notifications on an approval request for an approver so that the approver receives a single email notification.
    -   Provide approvers with the option to accept or reject approval requests directly from a consolidated email notification. Approvers can also reply to the email using commands for approving or rejecting individual requests or all requests. For more information on approval notifications, see [Notifications in Advanced Approval Management for Sales](https://www.servicenow.com/docs/access?context=setting-up-approval-notifications&family=australia&ft:locale=en-US)
-   **[Intelligent routing rules and smart reapprovals](https://www.servicenow.com/docs/access?context=set-approval-trigger-conditions&family=australia&ft:locale=en-US)**

Automatically trigger approvals by setting conditions based on items such as discount percentage, deal size, and margin thresholds. Configure thresholds and conditions so the approval workflow skips approved steps that have already been approved if the underlying conditions haven't changed.

-   **[Escalations](https://www.servicenow.com/docs/access?context=create-approval-configuration&family=australia&ft:locale=en-US)**

Enable approval rule admins to define escalation rules for reassigning pending requests to another approver automatically, when the original approver does not act within a specified time.

-   **[Override an approval step](https://www.servicenow.com/docs/access?context=override-approval-step&family=australia&ft:locale=en-US)**

As an approval rule writer who also has the approval admin role, override or bypass a pending approval request step to unblock an approval request when an approval is no longer required.

-   **[Automated notifications of approval status](https://www.servicenow.com/docs/access?context=setting-up-approval-notifications&family=australia&ft:locale=en-US)**

Inform sales agents and approvers of the status of approval items moving through the approval workflow by setting up notifications. Use predefined system notifications for reminders and escalations.

-   **[Flexible submission for approval requests](https://www.servicenow.com/docs/access?context=submitting-approval-requests&family=australia&ft:locale=en-US)**

Before submitting requests for approval, see the required approvals, approver names, approval reasons, and approval sequencing by creating and previewing approval requests. Requesters can recall approval requests for changes and resubmit them.

-   **[Real-time status tracking and approval history](https://www.servicenow.com/docs/access?context=tracking-approval-status&family=australia&ft:locale=en-US)**

Monitor approval progress and access approval history that provides detailed status for each approval step including assigned approvers, actual approvers \(for completed steps\), approval comments, and assignment and completion timestamps.

-   **[Approval management](https://www.servicenow.com/docs/access?context=approving-approval-requests&family=australia&ft:locale=en-US)**
    -   Accept or reject approvals using multiple channels, such as email, push notifications, the CSM Configurable Workspace, or approval centers, such as My Approvals in the ServiceNow AI Platform®.
    -   Assign backup approvers with date-specific coverage periods for seamless continuity of the approval process.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Advanced Approval Management features.

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
</table>## Removed

Between your current release family and Australia, some Advanced Approval Management features or functionality were removed.

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

Between your current release family and Australia, some Advanced Approval Management features or functionality were deprecated.

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

Review information on how to activate Advanced Approval Management.

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

Install Advanced Approval Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Advanced Approval Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Advanced Approval Management we have noted them here.

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

Review details on accessibility information for Advanced Approval Management, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Advanced Approval Management we have noted them here.

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

If there are specific highlight considerations for Advanced Approval Management we have noted them here.

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

-   In the approval card for a step in the Requested or Escalated state, view the automatically-calculated elapsed time that has passed for taking action on a pending approval, to help identify requests needing immediate attention.
-   Enable requesters and approvers to insert ad-hoc approvers at valid positions within an existing approval chain.
-   Enable requesters to recall submitted quotes directly from the quote header for quick edits, without navigating to the Approvals tab to use the approval workflow interface.
-   Display approval rejection reasons near the associated approval step card to give approvers and requesters clear context on why a quote was rejected.
-   Enable approver delegates to approve or reject an approval request directly from the Approvals tab.

 See [Advanced Approval Management for Sales](https://www.servicenow.com/docs/access?context=explore-advanced-approval-for-sales&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

