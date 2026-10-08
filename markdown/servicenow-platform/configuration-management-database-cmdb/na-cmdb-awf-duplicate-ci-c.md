---
title: Duplicate CI remediation using the CMDB Duplicate CIs Agent
description: The CMDB Duplicate CIs Agent identifies and helps remediate duplicate configuration items \(CIs\) in the CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-duplicate-ci-c.html
release: brazil
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 1
keywords: [duplicate CI, CMDB Duplicate CIs Agent, CMDB deduplication, Feature Preview Program]
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Duplicate CI remediation using the CMDB Duplicate CIs Agent

The CMDB Duplicate CIs Agent identifies and helps remediate duplicate configuration items \(CIs\) in the CMDB.

For background on duplicate CIs and the remediation process, see [Detecting duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/id-detect-dup-ci.md) and [Duplicate CIs remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/de-duplication-tasks.md).

On the Data Foundations advisor dashboard, the Duplicate CIs card displays its own **Ask Otto** action. This action is separate from the Remediation actions panel reached from the KPI Details page.

Selecting **Ask Otto** opens a ServiceNow Otto panel conversation with the CMDB Duplicate CIs Agent. Each selection starts a new conversation.

The **Ask Otto** action appears only when the ServiceNow Otto panel is enabled on the instance and the agent is active. The agent requires a deduplication administrator role in addition to the panel user role. If you hold only the CMDB success advisor scope-user role, the panel shows **Learn more** instead.

When the **Ask Otto** action isn't available for any reason, the panel falls back to **View de-duplication tasks**. For step-by-step instructions, see [Remediate duplicate CIs using the CMDB Duplicate CIs Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/na-cmdb-awf-duplicate-ci-t.md).

## Activation

The CMDB Duplicate CIs Agent is part of the Feature Preview Program and is inactive by default. Until an admin activates the agent, the **Ask Otto** action doesn't appear on the Duplicate CIs card. An admin can activate the agent from the Feature Preview Program. For steps to activate the agent, see [Activate the CMDB Duplicate CIs Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/configuration-management-database-cmdb/activate-na-cmdb-awf-duplicate-ci.md).

