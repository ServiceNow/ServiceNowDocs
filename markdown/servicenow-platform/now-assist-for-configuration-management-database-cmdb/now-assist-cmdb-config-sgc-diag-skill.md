---
title: Configure the Service Graph Connector diagnosis skill
description: Review and configure the settings of the Service Graph Connector diagnosis skill.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the Service Graph Connector diagnosis skill

Review and configure the settings of the Service Graph Connector diagnosis skill.

## Before you begin

Role required: admin

## About this task

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-pickers.md).\)

## Procedure

1.  In the Select display section, review where the skill appears and then select **Save and continue**.

2.  In the Review and activate section, review your selections and then select **Activate**.

3.  On the Successfully activated pop-up, select **Return to Service Graph Connector**.

4.  In the Active skills section of the Service Graph Connector page, see the **Status** column to verify that the skill is active.

    ![Active skills section displaying that theService Graph Connector diagnosis skill is active.](../image/now-assist-sgc-active.png "Active skills section")


**Parent Topic:**[Configuring Now Assist for CMDB](../concept/now-assist-cmdb-configuring.md)

