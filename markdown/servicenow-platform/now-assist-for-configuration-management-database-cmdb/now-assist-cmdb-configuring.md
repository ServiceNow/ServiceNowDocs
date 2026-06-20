---
title: Configuring Now Assist for CMDB
description: Configure Now Assist for CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.html
release: yokohama
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring Now Assist for CMDB

Configure Now Assist for CMDB.

## Skill activation

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see .

## Skill reuse in a domain-separated environment

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see . \(Note that global domain is not the same as global scope. For more information, see .\)

## Procedures

Follow these procedures to set up and configure Now Assist for Configuration Management Database \(CMDB\).

-   **[Configure Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configure.md)**  
Configure the Now Assist for CMDB application so users can benefit from Agentic workflows, agents, and skills.
-   **[Configure the Search CMDB agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-search-cmdb-aw.md)**  
Review and configure the settings of the Search CMDB agentic workflow.
-   **[Configure the CI summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-config-ci-summary.md)**  
Review and configure the settings of the Now Assist for Configuration Management Database \(CMDB\) CI summarization skill to restrict the availability of the skill to certain users or conditions.
-   **[Configure the manage duplicate CIs skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-config-mng-dupe-ci-skill.md)**  
Enable and configure scheduled jobs that support the manage duplicate CIs skill.
-   **[Configure the Service Graph Connector diagnosis skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown)**  
Review and configure the settings of the Service Graph Connector diagnosis skill.

**Parent Topic:**[Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md)

