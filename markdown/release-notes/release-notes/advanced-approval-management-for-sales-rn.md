---
title: Advanced Approval Management release notes
description: The ServiceNow Advanced Approval Management application enables you to define workflows for approving Sales Customer Relationship Management entities, such as customer quotes. Advanced Approval Management is a new application in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Advanced Approval Management release notes

The ServiceNow® Advanced Approval Management application enables you to define workflows for approving Sales Customer Relationship Management entities, such as customer quotes. Advanced Approval Management is a new application in the Australia release.

## Advanced Approval Management highlights for the Australia release

-   Create approval workflows that specify appropriate approvers and define the approval steps within a workflow.
-   Automate the approval workflow by setting conditions that automatically trigger the approval process and route approvals to designated approvers.
-   Prevent approval delays by automatically reassigning pending approvals when the original approver does not act within a set timeframe.
-   Enable approval rule admins or approval rule writers to override an approval step when an approval is no longer required.
-   Enable approvers or approval request writers to add relevant approvers during an active approval cycle without modifying existing approval rules.
-   Keep requesters informed and approvers on track by using automated email notifications for approval status changes, escalations, overrides, and ad hoc approvals.

See [Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-advanced-approval-for-sales.md) for more information.

**Important:** Advanced Approval Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Advanced Approval Management features

-   **[Flexible approval configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-advanced-approval-management.md)**

    Build workflows that enable sequential approvals, parallel \(simultaneous\) approvals, or a combination of both.

    -   Define workflow approval steps and optional chains that progress through multiple approval levels based on rule evaluations.
    -   Set the approval order using combinations of levels, roles, and conditions.
    -   Define approval users and groups.
    -   Consolidate multiple email notifications on an approval request for an approver so that the approver receives a single email notification.
-   **[Intelligent routing rules and smart reapprovals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-approval-trigger-conditions.md)**

    Automatically trigger approvals by setting conditions based on items such as discount percentage, deal size, and margin thresholds. Configure thresholds and conditions so the approval workflow skips approved steps that have already been approved if the underlying conditions haven't changed.

-   **[Escalations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-approval-configuration.md)**

    Enable approval rule admins to escalate an approval request by reassigning a pending approval request to another approver automatically when the original approver does not act within a specified time.

-   **[Override an approval step](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/override-approval-step.md)**

    As an approval rule writer who also has the approval admin role, override or bypass a pending approval request step to unblock an approval request when the approval is no longer required.

-   **[Automated notifications of approval status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/setting-up-approval-notifications.md)**

    Inform sales agents and approvers of the status of approval items moving through the approval workflow by setting up notifications. Use predefined system notifications for reminders and escalations.

-   **[Flexible submission for approval requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/submitting-approval-requests.md)**

    Before submitting requests for approval, see the required approvals, approver names, approval reasons, and approval sequencing by creating and previewing approval requests. Requesters can recall approval requests for changes and resubmit them.

-   **[Ad-hoc approvers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-approver.md)**

    As a requester or an approver, add one or more approvers or approval groups to an approval request, outside of the predefined approvers for a given rule. Enables approval users to add approvers who have more expertise on certain aspects of the request, for example if there are legal or regulatory issues relevant to the request.

-   **[Real-time status tracking and approval history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/tracking-approval-status.md)**

    Monitor approval progress and access an audit trail with detailed status for each approval step including assigned approvers, actual approvers \(for completed steps\), approval comments, and assignment and completion timestamps.

-   **[Approval management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/approving-approval-requests.md)**
    -   Accept or reject approvals using multiple channels, such as email, push notifications, the CSM Configurable Workspace, or approval centers, such as My Approvals in the ServiceNow AI Platform®.
    -   Assign backup approvers with date-specific coverage periods for seamless continuity of the approval process.

## Activation information

Install Advanced Approval Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugin is new in Australia:

    Advanced Approval Management \(com.sn\_adv\_appr\_mgmt\): Create workflows for approving entities such as customer quotes submitted by sales agents.


## Related ServiceNow applications and features

-   **[Quote Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-management.md)**

    The Quote Management application enables sales teams to create, configure, and manage customer quotes so that they accurately reflect products, pricing, and discounts throughout the sales cycle. Sales agents can submit quotes for approval using workflows defined in the Advanced Approval Management application.


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

