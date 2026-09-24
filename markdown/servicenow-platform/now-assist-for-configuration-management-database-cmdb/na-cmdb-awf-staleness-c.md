---
title: Stale CI remediation using the staleness agentic workflow
description: The staleness agentic workflow identifies, evaluates, and remediates stale configuration items \(CIs\) in the CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-staleness-c.html
release: brazil
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [stale CI, CMDB staleness, CI rediscovery, CI retirement]
breadcrumb: [Use generative AI skills, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Stale CI remediation using the staleness agentic workflow

The staleness agentic workflow identifies, evaluates, and remediates stale configuration items \(CIs\) in the CMDB.

A CI is set to stale when its record in the CMDB is no longer updated to reflect the actual state of the IT asset it represents. This staleness can occur when a physical device is removed from the network, taken offline, or is set to inaccessible to discovery tools. Stale CIs reduce trust in the CMDB and can cause incorrect assignments in incident management, change management, and compliance processes.

Staleness thresholds are defined in the CI Class Manager. Default thresholds are 60 or 90 days without an update or rediscovery. When a CI exceeds its threshold, the system can trigger remediation actions such as rediscovery or retirement through the Data Manager. The primary interface for managing staleness is CMDB success advisor.

## Replacement CI Staleness Agent \(Tom Brotherton\)

The Replacement CI Staleness Agent is a lightweight, semi-interactive version of Data Manager. It targets users who are not power users of the CMDB and aren't managing the CI life-cycle independently. The agent provides straightforward configurations per CI class to manage the flow from fresh CI to stale, attestation, retirement, archival, and deletion.

Key configuration options include:

-   The number of days before a fresh CI is considered stale
-   Automated attestation when AI confidence is high, or manual attestation task creation when confidence is low
-   The number of days a positive attestation excludes a CI from the next staleness check
-   The time period after retirement before a CI is archived
-   The time period after archival before a CI is deleted

## Causes of staleness

Stale CMDB data undermines every downstream process — incident management, change management, compliance audits, and vulnerability tracking all suffer when your CMDB data is unreliable.

-   No Consistent Definition: There is no standard for what "stale" means. In addition, many CI classes are non-discoverable by nature, so they quickly appear stale.
-   Discovery Failures: Network issues, expired credentials, and configuration errors prevent discovery methods from keeping CIs current.
-   Silent Decommissions: Assets removed from the network without updating their CMDB records or life-cycle status is set to stale.
-   Unmanaged Imports: Manually entered or imported CIs that aren't linked to automated discovery or life-cycle status become stale over time.

## Remediation actions

The staleness agentic workflow provides end-to-end automation to define, rediscover and retire CIs.

-   Unified staleness definition: Establish a single, consistent definition of what makes a CI "stale" across your entire CMDB. Aligned with Data Health Dashboard and CMDB success advisor, one definition drives all health scores.
-   Smart rediscovery: Automatically re-scan stale CIs to determine whether they are still active. Supports on-demand or scheduled rediscovery for temporarily unreachable assets, fixes configuration settings to resolve root causes, and determines staleness using activity signals such as changes and incidents.
-   Discovery and SGC health fixes: Beyond cleanup, the system identifies why CIs went stale. Get targeted recommendations to fix discovery or SGC schedules, credential issues, and configuration gaps to help prevent future staleness.
-   Guided life-cycle actions: For confirmed stale CIs, the system displays the recommended life-cycle action.

For each recommended action, the system displays all related CIs with a link to each CI record so you can review the list before applying the action. You can apply the action to all CIs in the group, select a subset, or ignore the recommendation.

CIs determined to be non-discoverable are marked for retirement and handled by the Data Manager. For manually entered or non-discovered CIs, the system uses activity signals — such as events, incidents, or other actions performed on the CI — to determine whether the CI is still in use before recommending retirement.

## Supported discovery sources

The staleness workflow supports all discovery sources, including Discovery, Service Graph Connectors, and Cloud Discovery. For cloud resources, the workflow supports automated rediscovery and reconfiguration following changes made to connect a CI to a datacenter and discovery source.

