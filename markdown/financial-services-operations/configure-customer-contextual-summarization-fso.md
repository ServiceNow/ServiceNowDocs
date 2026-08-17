---
title: Configure banking customer interaction context summary skill in ServiceNow Otto for FSO
description: Configure the customer interaction context summary skill in ServiceNow Otto for FSO to enable AI-powered summaries when initiating a banking customer interaction in Agentic Contact Center for Banking.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/configure-customer-contextual-summarization-fso.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Agentic Contact Center for Banking, Banking applications, Financial Services Operations \(FSO\)]
---

# Configure banking customer interaction context summary skill in ServiceNow Otto for FSO

Configure the customer interaction context summary skill in ServiceNow Otto for FSO to enable AI-powered summaries when initiating a banking customer interaction in Agentic Contact Center for Banking.

## Before you begin

Verify the ServiceNow Otto for Financial Services Operations \(FSO\) plugin \(sn\_fso\_gen\_ai\) is installed.

-   For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
-   For general information about configuring AI skills in FSO, see [Configure Financial Services Operations AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-fso-now-assist-skills.md).

**Note:** This skill is dependent on the customer profile summarization AI skill. For more information, see [Configure banking customer profile summarization in ServiceNow Otto for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-customer-profile-summarization-fso.md).

Role required: admin

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  Select the **Customer** &gt; **FSO** workflow group.

3.  In the **Customer interaction context summary** feature card, select **Activate skill**.

4.  In the **Define access** step, define the user access for the skill using Access Control Lists \(ACLs\).

    The roles sn\_fso\_csr.personal\_agent and sn\_fso\_csr.business\_agent are defined by default.

5.  Select **Save and continue**.

6.  In the **Select display** step, enable these options:

    -   In-product desktop
    -   ServiceNow Otto context menu
    For each option, select the arrow icon \(&gt;\) to define the roles that can use the skill.

7.  Select **Save and continue**.

8.  In the **Review and activate** step, review your choices and select **Activate** to complete the configuration.


## Result

The skill is activated.

## What to do next

Configure AI indexing for the sources that this AI skill uses to retrieve data and generate summaries. For more information, see [Configure AI indexing for Agentic Contact Center for Banking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-ai-indexing-fso-contact-center.md).

You can choose which service provider to use for this skill in ServiceNow Otto admin. For more information, see [Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md).

**Parent Topic:**[Configuring Agentic Contact Center for Banking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configuring-agentic-contact-center-for-banking.md)

