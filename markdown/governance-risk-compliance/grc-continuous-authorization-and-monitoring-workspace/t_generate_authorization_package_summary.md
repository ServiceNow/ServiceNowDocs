---
title: Generate an authorization package summary
description: Generate an AI-powered summary of an authorization package to view its status, key metrics, and operational information in a single consolidated view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t\_generate\_authorization\_package\_summary.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-08-06"
reading_time_minutes: 2
keywords: [generate, authorization package, summary, Now Assist, CAM]
breadcrumb: [Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Generate an authorization package summary

Generate an AI-powered summary of an authorization package to view its status, key metrics, and operational information in a single consolidated view.

## Before you begin

Role required: CAM GenAI user

Before you begin:

-   The ServiceNow Otto® GRC Shared Gen AI plugin must be installed and active on your instance.
-   The **Authorization package summarization** skill must be active \(it's enabled by default\).

## About this task

Use this procedure to generate an AI-powered summary of an authorization package at any point in its workflow lifecycle.

The authorization package summary includes the following fields from the authorization package record:

-   Package name
-   System purpose
-   Impact classification
-   Package version
-   Privacy-sensitive system flag
-   Authorization dates \(next authorization, ongoing authorization status, next engagement date\)
-   Boundary information \(boundary type, classification, and operational status\)
-   Number of change requests
-   Number of security incidents
-   Number of vulnerabilities
-   Plan of Action and Milestone \(POAM\) counts \(total open POAMs, high-priority POAMs\)
-   Authorization step status

Authorization package summarization provides the following benefits:

-   View critical package information at a glance without navigating multiple screens.
-   Support collaboration by sharing summaries to work notes for team review and discussion.

## Procedure

1.  Navigate to **CAM Workspace** and select the Lists icon from the sidebar.

2.  Navigate to **RMF** &gt; **Authorization pakages**.

3.  Select an authorization package record and navigate to the **Overview** tab.

    The package record can be in any workflow step \(Prepare, Categorize, Select, Implement, Assess, Authorize, or Monitor\).

4.  Select **Summarize** next to the Authorization Package summary section to generate the authorization package summary.

    The summary is generated and displayed on the authorization package overview. You can copy the summary text, regenerate it, provide feedback \(helpful or not helpful\), or share it to work notes. The summary card remains accessible whenever you view the package overview.

    The authorization package summary displays package name, system purpose, impact, version, privacy-sensitive status, authorization dates, boundary information, and POAM counts.

5.  Perform one of the following actions:

    -   Select **Copy** icon to copy the summary text to the clipboard.
    -   Select **Refresh** icon to refresh the summary with updated package information.
    -   Select **Share to work notes** to share the summary to work notes for team collaboration.

-   **[Reactivate Authorization package summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t_enable_authorization_package_summarization_skill.md)**  
Activate or deactivate the authorization package summarization skill from the AI Admin Panel to control whether users can generate summaries.

**Parent Topic:**[Continuous authorization and monitoring tasks in the CAM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-ws-continuous-auth-monitor.md)

