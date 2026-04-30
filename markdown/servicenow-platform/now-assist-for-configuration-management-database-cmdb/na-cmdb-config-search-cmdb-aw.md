---
title: Configure the Search CMDB agentic workflow
description: Review and configure the settings of the Search CMDB agentic workflow.
locale: en-US
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2025-10-15"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the Search CMDB agentic workflow

Review and configure the settings of the Search CMDB agentic workflow.

## Before you begin

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Role required: admin

## Procedure

1.  Activate the Query Generation skills as described in [Query Generation skills](https://www.servicenow.com/docs/access?context=enable-query-generation&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

2.  Index the CI data.

    1.  Navigate to **Query Generation** &gt; **Indexed Sources**.

    2.  Open the two records and select **Index all tables** or **Index table**.


**Parent Topic:**[Configuring Now Assist for CMDB](../../configuration-management/concept/now-assist-cmdb-configuring.md)

**Related topics**  


[Use Now Assist to search the CMDB for CIs](na-cmdb-awf-search.md)

