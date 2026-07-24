---
title: MID Server active issues
description: The ServiceNow instance has a dedicated table that publishes active issues with MID Servers and alerts administrators when a MID Server is in danger of exceeding its resources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/mid-server-active-issues.html
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resolving MID Server issues, MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server active issues

The ServiceNow® instance has a dedicated table that publishes active issues with MID Servers and alerts administrators when a MID Server is in danger of exceeding its resources.

The MID Server Issue \[ecc\_agent\_issue\] table displays a number of common issues that a MID Server can experience, as they occur. Error checking processes attempt to pinpoint the most likely cause of the issue. Informative error messages name the affected MID Server and explain the possible cause of the issue. The ecc\_agent\_issue table retains its records for 30 days.

To access records in this table, navigate to **MID Server** &gt; **Server Issues**.

Supported MID Server active issues:

-   Bad user credentials after [instance cloning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-post-clone-issue-resolution.md).
-   Unsupported [Java Runtime Environment \(JRE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md) on the MID Server host.
-   Approaching [resource thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-resource-threshold-alerts.md) for CPU usage and JVM memory.
-   Errors detected during [pre-upgrade testing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-pre-upgrade-check.md).
-   [User authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-connectivity-issues.md) and authorization failures.
-   Network [connectivity interruptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-connectivity-issues.md) and role configuration errors.

\[Omitted image "MIDServerIssueRecord.png"\] Alt text: Example MID Server Issue record

**Parent Topic:**[Resolving MID Server issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerTroubleshooting.md)

