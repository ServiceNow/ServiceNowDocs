---
title: Remediate stale CIs using the CMDB Staleness Agent
description: Use the CMDB Staleness Agent from the Data Foundations advisor dashboard to review and remediate flagged CIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-staleness-t.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 3
keywords: [stale CI, CMDB staleness, CI rediscovery, CI retirement]
breadcrumb: [Stale CI remediation, Use generative AI skills, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Remediate stale CIs using the CMDB Staleness Agent

Use the CMDB Staleness Agent from the Data Foundations advisor dashboard to review and remediate flagged CIs.

## Before you begin

Role required: cmdb\_inst\_admin

Role required: sn\_cmdb\_editor, plus now\_assist\_panel\_user, to use **Ask Otto**. A user with fewer roles can use a different action from the same panel; see the following steps.

## About this task

The staleness agentic workflow evaluates CIs against the staleness thresholds defined in the CI Class Manager and groups them by recommended action.

The system displays a linked list of all CIs in each group so you can review records before taking action.

The workflow uses activity signals, such as events, incidents, and changes, to determine whether a CI is still in use. This applies even if the CI has not been recently discovered. CIs with recent activity are excluded from retirement recommendations.

This action is separate from the Remediation actions panel reached from the KPI Details page. The Duplicate CIs card on the same dashboard has a separate **Ask Otto** action for the CMDB Duplicate CIs Agent, which is part of the Feature Preview Program. For more information, see [Feature Preview Program](https://www.servicenow.com/docs/r/platform-administration/feature-preview-program.html).

For more information on why CIs is set to stale, see [Stale CI remediation using the staleness agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-staleness-c.md).

## Procedure

1.  Open CMDB success advisor.

    The entry point for the staleness agentic workflow is through CMDB success advisor.

2.  Open CMDB success advisor and select **View insights** for Data Foundations.

    The Data Foundations advisor dashboard opens.

3.  On the dashboard, locate the **Stale CIs** card.

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

6.  Select the available action on the card.

    -   If you hold sn\_cmdb\_editor and the ServiceNow Otto panel user role, and the agent is available, select **Ask Otto** \[Omitted image "ask-otto-blue.png"\] on the card.
    -   If the required role or the agent isn't available, select **Review policies** instead.
    -   If you hold only the CMDB success advisor scope-user role, select **Learn more**.
    Selecting **Ask Otto** opens a new ServiceNow Otto panel conversation with the CMDB Staleness Agent. The other actions open the related record or article instead.

7.  Set up a retirement policy for CIs marked as stale.

    If applicable, use the Data Manager to define a policy for retiring CIs that the workflow has flagged. This step is required only if a retirement policy is not already configured for the affected CI class.


## Result

Stale CIs are rediscovered, retired, or flagged for configuration fixes based on the actions you applied. The CMDB data quality score in CMDB success advisor reflects the updated CI state.

Continue in the ServiceNow Otto panel conversation to review and apply the agent's recommended remediation. The CMDB data quality score in CMDB success advisor reflects the updated CI state after remediation.

