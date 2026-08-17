---
title: Configure insurance customer profile summarization in ServiceNow Otto for FSO
description: Configure the Insurance Customer Profile Summarization skill in ServiceNow Otto for FSO to enable AI-powered summaries of insurance customer information in the Customer 360 page of Agentic Contact Center for Insurance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/configure-insurance-customer-profile-summarization.html
release: australia
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 2
breadcrumb: [Configuring Agentic Contact Center for Insurance, Agentic Contact Center for Insurance, Insurance applications, Financial Services Operations \(FSO\)]
---

# Configure insurance customer profile summarization in ServiceNow Otto for FSO

Configure the Insurance Customer Profile Summarization skill in ServiceNow Otto for FSO to enable AI-powered summaries of insurance customer information in the Customer 360 page of Agentic Contact Center for Insurance.

## Before you begin

Verify the ServiceNow Otto for Financial Services Operations \(FSO\) plugin \(`sn_fso_now_assist`\) and the Agentic Contact Center for Insurance plugin \(`com.sn_ins_csr`\) are installed.

-   For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
-   For general information about configuring AI skills in FSO, see [Configure Financial Services Operations AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-fso-now-assist-skills.md).

**Note:** This skill is dependent on the Agentic Contact Center for Insurance application. Activate the **Insurance interaction context summary** skill after completing this task. For more information, see [Configure insurance customer interaction context summary skill in ServiceNow Otto for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-insurance-interaction-summary-skill.md).

Role required: admin

## About this task

The Insurance Customer Profile Summarization skill uses generative AI to deliver concise and comprehensive customer information in the Customer 360 page, eliminating searching across multiple data sources. It combines customer identity and an overview of owned and associated policies to provide a unified and actionable overview. The skill generates the **Profile** and **Status** sections in the **Customer summary** area of the Customer 360 page.

When the skill is not activated, the **Customer summary** section is not displayed.

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  Select the **Customer** &gt; **FSO** workflow group.

3.  In the **Insurance Customer Profile Summarization** feature card, select **Activate skill**.

4.  In the **Define access** step, define the user access for the skill using Access Control Lists \(ACLs\).

    The roles `sn_ins_csr.claims_agent` and `sn_ins_csr.servicing_agent` are defined by default.

5.  Select **Save and continue**.

6.  In the **Select display** step, enable these options:

    -   In-product desktop
    -   ServiceNow Otto context menu
    For each option, select the arrow icon \(&gt;\) to define the roles that can use the skill.

7.  Select **Save and continue**.

8.  In the **Review and activate** step, review your choices and select **Activate** to complete the configuration.


## Result

The skill is activated. The **Customer summary** section is displayed on the Customer 360 page for customers accessed by agents with the `sn_ins_csr.claims_agent` or `sn_ins_csr.servicing_agent` role.

## What to do next

You can choose which service provider to use for this skill in ServiceNow Otto Admin. For more information, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md).

