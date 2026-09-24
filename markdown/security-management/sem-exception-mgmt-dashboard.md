---
title: Exception management dashboard
description: The exception management dashboard gives vulnerability managers and exception administrators a live view of pending exception requests, approval workload, and service-level health across the Security Exposure Management bundle. Use the dashboard to track team capacity, spot bottlenecks, and prioritize follow-up.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-exception-mgmt-dashboard.html
release: brazil
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 2
keywords: [dashboard, exception management, approval workload, SLA]
breadcrumb: [Exception Management Overview, Use, Unified Security Exposure Management, Security Operations]
---

# Exception management dashboard

The exception management dashboard gives vulnerability managers and exception administrators a live view of pending exception requests, approval workload, and service-level health across the Security Exposure Management bundle. Use the dashboard to track team capacity, spot bottlenecks, and prioritize follow-up.

## Audience and access

The dashboard is intended for users who need a portfolio-level view of exception activity rather than a per-request approver view. Typical audiences include:

-   Vulnerability managers monitoring overall remediation health.
-   Exception administrators \(`sn_sec_exception.admin`\) responsible for approval-rule tuning.
-   Security operations leads tracking SLA performance and approver workload.

Access requires the `sn_sec_exception.admin` or `sn_sec_exception.read` role. Users with only an approver role see the Unified Approvals View instead.

## What the dashboard shows

The dashboard renders five widget groups:

-   **Pending workload**

    The current count of requests in **In Review** and **Requested** states, broken down by request type \(exception, false positive, extension, unassign\) and by approval rule. A trend line shows the seven-day change.

-   **SLA health**

    The proportion of pending requests within their approval-expiry window versus those approaching or past expiry. Color-coded thresholds \(green / amber / red\) reflect the configured warning windows on the approval rule.

-   **Approver workload**

    A per-approver and per-approval-group count of open assignments, sorted by oldest pending. Use this widget to detect overloaded approvers or stale assignments before they breach SLA.

-   **Outcome mix**

    The approve / reject / expire ratio over a rolling 30-day window, broken down by request type. A high reject rate against a single request type usually signals a configuration or training issue.

-   **Top contributors**

    The requesters and assignment groups with the most submitted requests in the period, which surfaces systemic remediation difficulties in specific teams or asset groups.


## Filtering and drill-down

The filter bar at the top of the dashboard lets you scope every widget by:

-   Time range \(today, last 7 days, last 30 days, custom\).
-   Finding source \(Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, Configuration Compliance\).
-   Risk rating \(Critical, High, Medium, Low, None\).
-   Assignment group.

Selecting a segment in any widget opens a filtered list of the underlying change approval records. From the filtered list you can drill into any single record to review the request \([Reviewing an Approval Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-review-approval-request.md)\) or take action.

## Navigating to the dashboard

From the Security Exposure Management Workspace, select **Administration** &gt; **Exception Management** &gt; **Dashboard**. The dashboard auto-refreshes every five minutes; use the refresh icon for an immediate update.

