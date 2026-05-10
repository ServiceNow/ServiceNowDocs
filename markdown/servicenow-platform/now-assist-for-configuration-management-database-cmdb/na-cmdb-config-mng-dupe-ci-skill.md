---
title: Configure the manage duplicate CIs skill
description: Enable and configure scheduled jobs that support the manage duplicate CIs skill.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the manage duplicate CIs skill

Enable and configure scheduled jobs that support the manage duplicate CIs skill.

## Before you begin

Role required: admin

## About this task

In this procedure, you enable scheduled jobs that support the manage duplicate CIs skill.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

## Procedure

1.  Enable the De-duplication: Populate Duplicate Task Data scheduled job.

    For instructions, see [Components installed for duplicate CI remediation](../../configuration-management/reference/components-installed-with-dup-ci.md).

2.  Enable the PopulateDuplicate Task Group Daily scheduled job to provide analysis of the root cause of remediation tasks.

    For instructions, see [Components installed with CMDB Workspace](../../configuration-management/reference/installed-with-cmdb-workspace.md).

3.  Enable the CMDB Health Dashboard - Correctness Score Calculation scheduled job.

    The job improves the accuracy of summary details on the CMDB Health Dashboard. For instructions, see [Enable and configure a CMDB Health Dashboard job](../../configuration-management/task/t_EnableCMDBHealthDashboardJob.md).


**Parent Topic:**[Configuring Now Assist for CMDB](../../configuration-management/concept/now-assist-cmdb-configuring.md)

**Related topics**  


[Use Now Assist to search the CMDB](na-cmdb-awf-search.md)

