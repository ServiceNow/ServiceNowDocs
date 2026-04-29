---
title: Using Now Assist skills in Now Assist for CMDB
description: Use Now Assist for CMDB skills to view a concise summary of key CI data, to help you to resolve de-duplication tasks, and several other processes.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Using Now Assist skills in Now Assist for CMDB

Use Now Assist for CMDB skills to view a concise summary of key CI data, to help you to resolve de-duplication tasks, and several other processes.

## Skill reuse in a domain-separated environment

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).\)

## Now Assist skills used by Now Assist for CMDB

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** To enable a subset of users to access Now Assist for CMDB skills, create a role or a group for the users. For more information, see [Create a role or a group to access Now Assist skills](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2078019).

-   **CI summarization skill**

    View a concise summary of key CI data. You can select the CI on a CI form, in a workspace page, or on any list view. The summary can include discovery data, ownership, and key related items such as open incidents, alerts, problems, upcoming change requests, and security vulnerabilities. Additionally, the summary lists the service instances that the CI is part of. For more information, see [View CI information with the Now Assist CI summarization skill](../../now-assist-cmdb/task/na-cmdb-agent-ci-summarizer.md).

-   **Manage duplicate CIs skill**

    Resolve de-duplication tasks with support from the Now Assist Manage duplicate CIs skill. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template. For more information, see [Let Now Assist help you to manage duplicate CIs](../task/now-assist-cmdb-mng-dupe-cis-skill.md).

-   **Service Graph Connector diagnosis skill**

    To reduce debugging and resolution time and effort, the Service Graph Connector diagnosis skill generates summaries of errors and recommendations for resolving processing errors with SGC import sets. For more information, see [Fix SGC import set issues with the Now Assist SGC diagnosis skill](../task/now-assist-cmdb-sgc-diagnose.md)


