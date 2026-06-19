---
title: Configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\)
description: If you have the admin role, you can configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\). This provides a conversational experience for your customers to submit card disputes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/configuring-disputes-intake-via-virtual-agent.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure AI skills, Configure, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\)

If you have the admin role, you can configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\). This provides a conversational experience for your customers to submit card disputes.

## Before you begin

Confirm that Financial Services Card Operations \(sn\_bom\_credit\_card\) is installed on your instance.

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for FSO. This console contains what you need to install the plugins and configure the generative AI skills. For additional information, see .

**Note:**

Now LLM Service is currently the only provider for this Now Assist application's skills.

## Procedure

1.  Install the Now Assist for Financial Services Operations \(FSO\) plugin \(sn\_fso\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Application information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/supporting-information-for-now-assist-for-financial-services-operations-fso.md).
    -   For information about the installation process, see .
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Select the **Customer** &gt; **FSO** workflow group.

4.  In the Disputes intake via Virtual Agent skill panel, select **Turn on**.

5.  In the Turn on skill window, define the roles permitted to use this skill.

    ACLs are implemented to identify the users permitted to access the skill. See  for more information.

6.  Select **Turn on**.


## Result

A window displays confirming that the Disputes intake via Virtual Agent skill is active.

## What to do next

You can choose which service provider to use for this skill in the Now Assist Admin console.

-   **[Customize the Virtual Agent topic in Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/customize-report-a-dispute-va-topic.md)**  
Review and modify the Virtual Agent topic in Disputes intake via Virtual Agent. Learn how the conversation workflow functions, and modify it for your own needs.

**Parent Topic:**[Configure Financial Services Operations Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-fso-now-assist-skills.md)

