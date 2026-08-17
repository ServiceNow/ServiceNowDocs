---
title: Using ServiceNow Otto skills in ServiceNow Otto for CMDB
description: Use ServiceNow Otto for CMDB skills to view a concise summary of key CI data, to help you to resolve deduplication tasks, and several other processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using-skills.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Using ServiceNow Otto skills in ServiceNow Otto for CMDB

Use ServiceNow Otto for CMDB skills to view a concise summary of key CI data, to help you to resolve deduplication tasks, and several other processes.

## Skill reuse in a domain-separated environment

By default, all skills exist in the global domain. When you use AI in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, AI only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

## ServiceNow Otto skills used by ServiceNow Otto for CMDB

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

**Note:** To enable a subset of users to access ServiceNow Otto for CMDB skills, create a role or a group for the users. For more information, see [Create a role or a group to access ServiceNow Otto skills](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2078019).

-   **CI summarization skill**

    View a concise summary of key CI data. You can select the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of. For more information, see [View CI information with the ServiceNow Otto CI summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-ci-summarizer.md).

-   **Summarize CMDB readiness skill**

    View an AI-generated summary of the CMDB success advisor for HAM or CMDB success advisor for Data Foundations dashboard data. The summary highlights the key findings on CMDB data accuracy, completeness, and health, and recommends remediation actions to address the findings. For more information, see [Summarize CMDB readiness with the ServiceNow Otto skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-summ-rdy.md).

-   **Manage duplicate CIs skill**

    Resolve deduplication tasks with support from the ServiceNow Otto Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template. For more information, see [Let ServiceNow Otto help you to manage duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-mng-dupe-cis-skill.md).

-   **Service Graph Connector diagnosis skill**

    To reduce debugging and resolution time and effort, the Service Graph Connector diagnosis skill generates summaries of errors and recommendations for resolving processing errors with SGC import sets. For more information, see [Fix SGC import set issues with the ServiceNow Otto SGC diagnosis skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)


