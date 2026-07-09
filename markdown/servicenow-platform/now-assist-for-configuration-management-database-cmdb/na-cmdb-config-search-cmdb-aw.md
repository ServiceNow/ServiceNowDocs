---
title: Configure the Search CMDB agentic workflow
description: Review and configure the settings of the Search CMDB agentic workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-search-cmdb-aw.html
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

[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/define-sec-controls-aw.md).

Role required: admin

## Procedure

1.  Activate the Query Generation skills as described in [Query Generation skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/enable-query-generation.md).

2.  Index the CI data.

    1.  Navigate to **Query Generation** &gt; **Indexed Sources**.

    2.  Open the two records and select **Index all tables** or **Index table**.


**Parent Topic:**[Configuring Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

**Related topics**  


[Use Now Assist to search the CMDB for CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-search.md)

