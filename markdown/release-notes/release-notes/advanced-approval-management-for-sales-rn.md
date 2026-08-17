---
title: Advanced Approval Management release notes
description: The ServiceNow Advanced Approval Management application enables you to define workflows for approving Sales Customer Relationship Management entities, such as customer quotes. Advanced Approval Management is a new application in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Advanced Approval Management release notes

The ServiceNow® Advanced Approval Management application enables you to define workflows for approving Sales Customer Relationship Management entities, such as customer quotes. Advanced Approval Management is a new application in the Australia release.

## Advanced Approval Management highlights for the Australia release

-   In the approval card for a step in the Requested or Escalated state, view the automatically-calculated elapsed time that has passed for taking action on a pending approval, to help identify requests needing immediate attention.
-   Enable requesters and approvers to insert ad-hoc approvers at valid positions within an existing approval chain.
-   Enable requesters to recall submitted quotes directly from the quote header for quick edits, without navigating to the Approvals tab to use the approval workflow interface.
-   Display approval rejection reasons near the associated approval step card to give approvers and requesters clear context on why a quote was rejected.
-   Enable approver delegates to approve or reject an approval request directly from the Approvals tab.

See [Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-advanced-approval-for-sales.md) for more information.

**Important:** Advanced Approval Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Advanced Approval Management to Australia

The default value for the **Rule order** field in a chain is now 10. If you have rule orders in chains configured with different order values, review and update them as needed to align with the new default.

Assign the approval\_request\_submitter role to requesters who submit approval requests only and don't have access to the full advanced approval workflow functionality and interface. Users with this role can't recall recall or update approval requests. For more information, see [Components installed with Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-advanced-approval-management-for-sales.md).

## Advanced Approval Management features

-   **Approval duration on approval cards**

    As an approver or requester, view the amount of time that has elapsed for an approval step in a Requested or Escalated state. The time amount is highlighted and displayed in

    -   Hours, if the duration is under 24 hours
    -   Days and hours, if the duration is under seven days
    -   Weeks and days, if the duration is over seven days
    The elapsed time starts when the approval request is submitted or when an escalation is triggered based on escalation rules.

-   **[Add ad-hoc approvers to approval chains](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-approver.md)**

    As a requester or approver, insert an ad-hoc approver at a specific position within an existing approval chain. The approval engine validates the position to prevent insertion before already requested or completed approvals. Ad-hoc approvers are clearly identified in the chain view and receive approval notifications with requester comments.

-   **[Recall an approval request from the quote header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/submitting-approval-requests.md)**

    Enable requesters to recall submitted approval requests directly from the quote header in the quote workflow, without navigating to the Approvals tab.

-   **[Rejection reason in Approvals tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/approving-approval-requests.md)**

    Inform approval requesters of rejected approval requests by displaying the rejection reason near the related step card in the Approvals tab of the entity. Displaying the rejection reason helps requesters understand the issue with the request, without contacting approvers for clarification.

-   **[Configure delegate approvers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-approval-delegation.md)**

    Configure the delegation rules allowing delegate approvers to approve or reject approval requests. Delegate approvers can approve or reject a request directly from the approval step card in the Approvals tab, on behalf of the original approver.

-   **[Flexible approval configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-advanced-approval-management.md)**

    Build workflows that enable sequential approvals, parallel \(simultaneous\) approvals, or a combination of both.

    -   Define workflow approval steps and optional chains that progress through multiple approval levels based on rule evaluations.
    -   Set the approval order using combinations of levels, roles, and conditions.
    -   Define approval users and groups.
    -   Consolidate multiple email notifications on an approval request for an approver so that the approver receives a single email notification.
    -   Provide approvers with the option to accept or reject approval requests directly from a consolidated email notification. Approvers can also reply to the email using commands for approving or rejecting individual requests or all requests. For more information on approval notifications, see [Notifications in Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/setting-up-approval-notifications.md)
-   **[Intelligent routing rules and smart reapprovals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-approval-trigger-conditions.md)**

    Automatically trigger approvals by setting conditions based on items such as discount percentage, deal size, and margin thresholds. Configure thresholds and conditions so the approval workflow skips approved steps that have already been approved if the underlying conditions haven't changed.

-   **[Escalations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-approval-configuration.md)**

    Enable approval rule admins to define escalation rules for reassigning pending requests to another approver automatically, when the original approver does not act within a specified time.

-   **[Override an approval step](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/override-approval-step.md)**

    As an approval rule writer who also has the approval admin role, override or bypass a pending approval request step to unblock an approval request when an approval is no longer required.

-   **[Automated notifications of approval status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/setting-up-approval-notifications.md)**

    Inform sales agents and approvers of the status of approval items moving through the approval workflow by setting up notifications. Use predefined system notifications for reminders and escalations.

-   **[Flexible submission for approval requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/submitting-approval-requests.md)**

    Before submitting requests for approval, see the required approvals, approver names, approval reasons, and approval sequencing by creating and previewing approval requests. Requesters can recall approval requests for changes and resubmit them.

-   **[Real-time status tracking and approval history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/tracking-approval-status.md)**

    Monitor approval progress and access approval history that provides detailed status for each approval step including assigned approvers, actual approvers \(for completed steps\), approval comments, and assignment and completion timestamps.

-   **[Approval management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/approving-approval-requests.md)**
    -   Accept or reject approvals using multiple channels, such as email, push notifications, the CSM Configurable Workspace, or approval centers, such as My Approvals in the ServiceNow AI Platform®.
    -   Assign backup approvers with date-specific coverage periods for seamless continuity of the approval process.

## Activation information

Install Advanced Approval Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugin is new in Australia:

    Advanced Approval Management \(com.sn\_adv\_appr\_mgmt\): Create workflows for approving entities such as customer quotes submitted by sales agents.


## Related ServiceNow applications and features

-   **[Quote Experience in CPQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quoting-experiences-overview.md)**

    The ServiceNow Quote Experience application enables sales teams to create, configure, and manage customer quotes so that they accurately reflect products, pricing, and discounts throughout the sales cycle. Sales agents can submit quotes for approval using workflows defined in the Advanced Approval Management application.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/sales-order-management-rn-landing.md)

