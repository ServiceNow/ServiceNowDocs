---
title: Configure Disputes intake via Virtual Agent in ServiceNow Otto for Financial Services Operations \(FSO\)
description: If you have the admin role, you can configure Disputes intake via Virtual Agent in ServiceNow Otto for Financial Services Operations \(FSO\). This provides a conversational experience for your customers to submit card disputes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/configuring-disputes-intake-via-virtual-agent.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Configure Disputes intake via Virtual Agent in ServiceNow Otto for Financial Services Operations \(FSO\)

If you have the admin role, you can configure Disputes intake via Virtual Agent in ServiceNow Otto for Financial Services Operations \(FSO\). This provides a conversational experience for your customers to submit card disputes.

## About this task

Disputes intake via Virtual Agent is an AI skill that uses a chat bot to collect card dispute information from customers. This streamlines the submission process and reduces workloads for live agents by using AI to infer answers and fill out dispute forms automatically. For more information, see [Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/disputes-intake-via-virtual-agent-fso.md).

## Before you begin

Verify that Financial Services Card Operations \(sn\_bom\_credit\_card\) and ServiceNow Otto for Financial Services Operations \(FSO\) plugin \(sn\_fso\_gen\_ai\) are installed.

-   For information about the ServiceNow Otto installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
-   For general information about configuring AI skills in FSO, see [Configure Financial Services Operations AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-fso-now-assist-skills.md).

Role required: admin

## About this task

Use the AI Admin Hub console to configure ServiceNow Otto for FSO. This console contains what you need to install the plugins and configure the generative AI skills. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  Select the **Customer** &gt; **FSO** workflow group.

3.  In the Disputes intake via Virtual Agent skill panel, select **Turn on**.

4.  In the Turn on skill window, define the roles permitted to use this skill.

    ACLs are implemented to identify the users permitted to access the skill. See [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md) for more information.

5.  Select **Turn on**.


## Result

A window displays confirming that the Disputes intake via Virtual Agent skill is active.

## What to do next

You can choose which service provider to use for this skill in ServiceNow Otto Admin. For more information, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md).

-   **[Customize the Virtual Agent topic in Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/customize-report-a-dispute-va-topic.md)**  
Review and modify the Virtual Agent topic in Disputes intake via Virtual Agent. Learn how the conversation workflow functions, and modify it for your own needs.

**Parent Topic:**[Set up Dispute Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/setting-up-disputes-management.md)

**Related topics**  


[Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/disputes-intake-via-virtual-agent-fso.md)

[Submit a dispute case with Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/submit-dispute-case-disputes-intake-via-virtual-agent.md)

[Form Data Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/learn-about-the-form-data-collector.md)

