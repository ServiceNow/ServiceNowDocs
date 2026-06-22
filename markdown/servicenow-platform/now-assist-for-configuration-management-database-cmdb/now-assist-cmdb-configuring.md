---
title: Configuring Now Assist for CMDB
description: Configure Now Assist for CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-12-01"
reading_time_minutes: 2
breadcrumb: [Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring Now Assist for CMDB

Configure Now Assist for CMDB.

## Roles

[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).

## Skill activation

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

## Skill reuse in a domain-separated environment

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/next-experience-pickers.md).\)

## Procedures

Follow these procedures to set up and configure Now Assist for Configuration Management Database \(CMDB\).

-   **[Configure Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configure.md)**  
Configure the Now Assist for CMDB application so users can benefit from Agentic workflows, agents, and skills.
-   **[Configure the Search CMDB agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-search-cmdb-aw.md)**  
Review and configure the settings of the Search CMDB agentic workflow.
-   **[Configure the CI form contextual help skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-form-sense-config.md)**  
Configure the CI form contextual help skill.
-   **[Configure the CI summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-config-ci-summary.md)**  
Review and configure the settings of the Now Assist for Configuration Management Database \(CMDB\) CI summarization skill to restrict the availability of the skill to certain users or conditions.
-   **[Configure the manage duplicate CIs skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-mng-dupe-ci-skill.md)**  
Enable and configure scheduled jobs that support the manage duplicate CIs skill.
-   **[Configure the Service Graph Connector diagnosis skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown)**  
Review and configure the settings of the Service Graph Connector diagnosis skill.

**Parent Topic:**[Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md)

