---
title: Submit Break-Fix Cases through Portal or Mobile
description: Report equipment failures using the Retail Operations portal or mobile app. Your requesting store and available equipment are automatically determined based on your user account and service organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/breakfix-submit-case.html
release: australia
topic_type: task
last_updated: "2026-07-09"
reading_time_minutes: 2
breadcrumb: [Manage Break-Fix cases, Retail]
---

# Submit Break-Fix Cases through Portal or Mobile

Report equipment failures using the Retail Operations portal or mobile app. Your requesting store and available equipment are automatically determined based on your user account and service organization.

## Before you begin

-   Equipment must be registered in install base with your store as buyer organization
-   Gather failure details: brief description, symptoms, business impact, troubleshooting attempted
-   **Role required:** Store Manager, Store Associate, Regional Manager, or Area Manager

## About this task

Both portal and mobile app support case submission. Your requesting store is automatically populated from your service organization. Equipment is filtered based on Install Base buyer organization relationship—only equipment registered to your store appears selectable. If an open case already exists for the same store and equipment, a duplicate warning appears before submission.

Upon submission, the case is created in the "New" state and routed to HQ support queue. In this state, only the Close action is available. Other actions \(Accept/Reject\) become available after HQ proposes a resolution.

## Procedure

1.  Log in to the Retail Operations portal or open the Retail Operations mobile app

2.  Navigate to **Browse Catalog &gt; Break-fix**

3.  Review the **Requesting store** field—your service organization is automatically populated

    **Note:** Store-level users cannot change this field. Regional and Area Managers can select a different managed store.

4.  In the **Affected device \(Install base\)** field, select the failed equipment from the filtered list

    **Note:** Only equipment registered to your store \(where your organization is the buyer organization\) appears. If equipment is missing, verify it exists in Install Base with your organization as buyer.

5.  In the **Priority** field, select a priority level \(default: 3 - Moderate\)

    **Note:** Mandatory. Options: 1 - Urgent, 2 - High, 3 - Moderate, 4 - Low.

6.  In the **Issue title** field, enter a brief summary of the equipment failure

    **Note:** Mandatory. Example: "POS Terminal 5 not booting"

7.  In the **Description** field, provide detailed failure information

    **Note:** Mandatory. Include: symptoms, when failure started, affected business operations, any troubleshooting already attempted.

8.  Attach supporting files using the **Attachment** field

    **Note:** Recommended for complex failures \(screenshots, error logs, photos\).

9.  Click \(portal\) or tap \(mobile\) **Submit**

    **Note:** If an open case exists for same store/equipment, a duplicate warning appears. Click/tap Yes to proceed with new case or No to cancel and review existing case.


## Result

Case created in "New" state and routed to HQ support queue. Success screen displays case number. Track case in your requested cases list. You can Close the case while in New state. After HQ proposes resolution, you can Accept or Reject it.

## What to do next

HQ Support Agents will triage your case. You will receive notification when they propose resolution. See [Respond to Resolutions \(Portal and Mobile\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-respond-resolution.md) for next steps.

**Related topics**  


[Break-Fix Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-overview.md)

[Respond to resolutions through Portal or Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-respond-resolution.md)

[Resolve Cases in Workspace through HQ Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-resolve-workspace.md)

[Components for Break-Fix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-reference.md)

