---
title: Configure insurance customer profile summarization in Now Assist for FSO
description: Configure the Insurance Customer Profile Summarization skill in Now Assist for FSO to enable AI-powered summaries of insurance customer information in the Customer 360 page of Agentic Contact Center for Insurance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-insurance-customer-profile-summarization.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 2
breadcrumb: [Configure AI skills, Configure, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Configure insurance customer profile summarization in Now Assist for FSO

Configure the Insurance Customer Profile Summarization skill in Now Assist for FSO to enable AI-powered summaries of insurance customer information in the Customer 360 page of Agentic Contact Center for Insurance.

## Before you begin

Verify the Now Assist for Financial Services Operations \(FSO\) plugin \(`sn_fso_now_assist`\) and the Agentic Contact Center for Insurance plugin \(`com.sn_ins_csr`\) are installed.

-   For information about the plugin dependencies and plugin activation order, see [Application information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/supporting-information-for-now-assist-for-financial-services-operations-fso.md).
-   For information about the installation process, see .

**Note:** This skill is dependent on the Agentic Contact Center for Insurance application. Activate the **Insurance interaction context summary** skill after completing this task. For more information, see [Configure insurance customer interaction context summary skill in Now Assist for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-insurance-interaction-summary-skill.md).

Role required: admin

## About this task

The Insurance Customer Profile Summarization skill uses generative AI to deliver concise and comprehensive customer information in the Customer 360 page, eliminating searching across multiple data sources. It combines customer identity and an overview of owned and associated policies to provide a unified and actionable overview. The skill generates the **Profile** and **Status** sections in the **Customer summary** area of the Customer 360 page.

When the skill is not activated, the **Customer summary** section is not displayed.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Select the **Customer** &gt; **FSO** workflow group.

3.  In the **Insurance Customer Profile Summarization** feature card, select **Activate skill**.

4.  In the **Define access** step, define the user access for the skill using Access Control Lists \(ACLs\).

    The roles `sn_ins_csr.claims_agent` and `sn_ins_csr.servicing_agent` are defined by default.

5.  Select **Save and continue**.

6.  In the **Select display** step, enable these options:

    -   In-product desktop
    -   Now Assist context menu
    For each option, select the arrow icon \(&gt;\) to define the roles that can use the skill.

7.  Select **Save and continue**.

8.  In the **Review and activate** step, review your choices and select **Activate** to complete the configuration.


## Result

The skill is activated. The **Customer summary** section is displayed on the Customer 360 page for customers accessed by agents with the `sn_ins_csr.claims_agent` or `sn_ins_csr.servicing_agent` role.

## What to do next

You can choose which service provider to use for this skill in the Now Assist Admin console.

**Parent Topic:**[Configure Financial Services Operations Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-fso-now-assist-skills.md)

