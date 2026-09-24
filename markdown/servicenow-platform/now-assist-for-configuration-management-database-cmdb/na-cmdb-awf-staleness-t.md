---
title: Remediate stale CIs using the staleness agentic workflow
description: Use the staleness agentic workflow to identify, evaluate, and remediate stale CIs through rediscovery or retirement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-staleness-t.html
release: brazil
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [stale CI, CMDB staleness, CI rediscovery, CI retirement]
breadcrumb: [Stale CI remediation, Use generative AI skills, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Remediate stale CIs using the staleness agentic workflow

Use the staleness agentic workflow to identify, evaluate, and remediate stale CIs through rediscovery or retirement.

## Before you begin

Role required: cmdb\_inst\_admin

## About this task

The staleness agentic workflow evaluates CIs against the staleness thresholds defined in the CI Class Manager and groups them by recommended action. The system displays a linked list of all CIs in each group so you can review records before taking action.

The workflow uses activity signals — such as events, incidents, and changes — to determine whether a CI is still in use, even if it has not been recently discovered. CIs with recent activity are excluded from retirement recommendations.

For more information on why CIs is set to stale, see [Stale CI remediation using the staleness agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-staleness-c.md).

## Procedure

1.  Open CMDB success advisor.

    The entry point for the staleness agentic workflow is through CMDB success advisor.

2.  In the Data Foundations dashboard, select the stale CIs chart segment or count.

    The KPI Details page opens. If remediation actions are available, the Remediation actions panel appears.

3.  In the Remediation actions panel, select the staleness action group to review.

    The system displays all CIs associated with the recommended action. Each CI is linked so you can open and review its record before proceeding.

4.  Select the CIs to include in the action.

    -   Apply the action to all CIs in the group.
    -   Select a subset of CIs from the group.
    -   Ignore the recommendation.
5.  Apply the recommended remediation action.

    Depending on the CI group, the available actions include the following:

    |Action|Description|
    |------|-----------|
    |**Rediscover**|Triggers on-demand or scheduled rediscovery for CIs that may be temporarily unreachable. Supported for all discovery sources, including Discovery, Service Graph Connectors, and Cloud Discovery.|
    |**Retire**|Marks confirmed stale CIs for retirement and routes them to the Data Manager. The system automatically marks non-discoverable CIs for retirement.|
    |**Fix configuration**|Applies targeted fixes to discovery schedules, credentials, or Service Graph Connector configuration to resolve the root cause of staleness.|

    The system applies the action, records the result, and generates an audit trail of actions.

6.  Set up a retirement policy for CIs marked as stale.

    If applicable, use the Data Manager to define a policy for retiring CIs that the workflow has flagged. This step is required only if a retirement policy is not already configured for the affected CI class.


## Result

Stale CIs are rediscovered, retired, or flagged for configuration fixes based on the actions you applied. The CMDB data quality score in CMDB success advisor reflects the updated CI state.

