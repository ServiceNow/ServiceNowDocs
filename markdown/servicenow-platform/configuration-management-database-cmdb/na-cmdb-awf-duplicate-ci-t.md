---
title: Remediate duplicate CIs using the CMDB Duplicate CIs Agent
description: Use the CMDB Duplicate CIs Agent from the Data Foundations advisor dashboard to review and remediate flagged duplicate CIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-duplicate-ci-t.html
release: brazil
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 1
keywords: [duplicate CI, CMDB Duplicate CIs Agent, CMDB deduplication]
breadcrumb: [Duplicate CI remediation, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Remediate duplicate CIs using the CMDB Duplicate CIs Agent

Use the CMDB Duplicate CIs Agent from the Data Foundations advisor dashboard to review and remediate flagged duplicate CIs.

## Before you begin

Role required: cmdb\_dedup\_admin, plus now\_assist\_panel\_user, to use **Ask Otto**. A user with fewer roles can use a different action from the same card; see the following steps.

## About this task

The CMDB Duplicate CIs Agent reviews CIs flagged as duplicates and proposes remediation actions for you to approve, reject, or skip. This action is separate from the Remediation actions panel reached from the KPI Details page.

The agent is part of the Feature Preview Program and is inactive by default. For background on the agent and its activation, see [Duplicate CI remediation using the CMDB Duplicate CIs Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-duplicate-ci-c.md).

## Procedure

1.  Open CMDB success advisor and select **View insights** for Data Foundations.

    The Data Foundations advisor dashboard opens.

2.  On the dashboard, locate the **Duplicate CIs** card.

3.  Select the available action on the card.

    -   If you hold cmdb\_dedup\_admin and the ServiceNow Otto panel user role, and the agent is active, select **Ask Otto** \[Omitted image "ask-otto-blue.png"\] on the card.
    -   If the required role or the agent isn't active, select **View de-duplication tasks** instead.
    -   If you hold only the CMDB success advisor scope-user role, select **Learn more**.
    Selecting **Ask Otto** opens a new ServiceNow Otto panel conversation with the CMDB Duplicate CIs Agent. The other actions open the related record or article instead.


## Result

Continue in the ServiceNow Otto panel conversation to review and apply the agent's recommended remediation. The CMDB data quality score in CMDB success advisor reflects the updated CI state after remediation.

