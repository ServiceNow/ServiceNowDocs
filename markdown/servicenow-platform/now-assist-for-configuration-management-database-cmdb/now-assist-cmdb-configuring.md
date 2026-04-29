---
title: Configuring Now Assist for CMDB
description: Configure Now Assist for CMDB.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configuring Now Assist for CMDB

Configure Now Assist for CMDB.

## Roles

Agentic workflows and their AI agents use [role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Skill reuse in a domain-separated environment

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).\)

## Procedures

Follow these procedures to set up and configure Now Assist for Configuration Management Database \(CMDB\).

-   **[Configure Now Assist for CMDB 3.0](../task/now-assist-cmdb-configure-3.0.md)**  
Configure the Now Assist for CMDB application so users can benefit from Agentic workflows, agents, and skills.
-   **[Configure Now Assist for CMDB before v3.0](../task/now-assist-cmdb-configure.md)**  
Configure the Now Assist for CMDB application so users can benefit from Agentic workflows, agents, and skills.
-   **[Configure the Search CMDB agentic workflow](../../now-assist-cmdb/task/na-cmdb-config-search-cmdb-aw.md)**  
Review and configure the settings of the Search CMDB agentic workflow.
-   **[Configure the CI summarization skill](../task/now-assist-cmdb-config-ci-summary.md)**  
Review and configure the settings of the Now Assist for Configuration Management Database \(CMDB\) CI summarization skill to restrict the availability of the skill to certain users or conditions.
-   **[Configure the CI form contextual help skill](../../now-assist-cmdb/task/na-cmdb-skill-form-sense-config.md)**  
Configure the CI form contextual help skill.
-   **[Configure the manage duplicate CIs skill](../../now-assist-cmdb/task/na-cmdb-config-mng-dupe-ci-skill.md)**  
Enable and configure scheduled jobs that support the manage duplicate CIs skill.
-   **[Configure the Service Graph Connector diagnosis skill](../task/now-assist-cmdb-config-sgc-diagnose.md)**  
Review and configure the settings of the Service Graph Connector diagnosis skill.

**Parent Topic:**[Now Assist for Configuration Management Database \(CMDB\)](now-assist-landing-cmdb.md)

