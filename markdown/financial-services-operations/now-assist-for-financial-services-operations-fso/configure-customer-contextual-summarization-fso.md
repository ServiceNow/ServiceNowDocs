---
title: Configure customer interaction context summary skill in Now Assist for FSO
description: Configure the customer interaction context summary skill in Now Assist for FSO to enable AI-powered summaries when initiating a customer interaction.
locale: en-US
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Configure customer interaction context summary skill in Now Assist for FSO

Configure the customer interaction context summary skill in Now Assist for FSO to enable AI-powered summaries when initiating a customer interaction.

## Before you begin

Verify the Now Assist for Financial Services Operations \(FSO\) plugin \(sn\_fso\_gen\_ai\) is installed.

-   For information about the plugin dependencies and plugin activation order, see [Application information](../../fso-common/concept/supporting-information-for-now-assist-for-financial-services-operations-fso.md#section_ng1_bdj_mbc).
-   For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

**Note:** This skill is dependent on the customer profile summarization AI skill. For more information, see [Configure customer profile summarization in Now Assist for FSO](configure-customer-profile-summarization-fso.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Select the **Customer** &gt; **FSO** workflow group.

3.  In the **Customer interaction context summary** feature card, select **Activate skill**.

4.  In the **Define access** step, define the user access for the skill using Access Control Lists \(ACLs\).

    The roles sn\_fso\_csr.personal\_agent and sn\_fso\_csr.business\_agent are defined by default.

5.  Select **Save and continue**.

6.  In the **Select display** step, enable these options:

    -   In-product desktop
    -   Now Assist context menu
    For each option, select the arrow icon \(&gt;\) to define the roles that can use the skill.

7.  Select **Save and continue**.

8.  In the **Review and activate** step, review your choices and select **Activate** to complete the configuration.


## Result

The skill is activated.

## What to do next

Configure AI indexing for the sources that this AI skill uses to retrieve data and generate summaries. For more information, see [Configure AI indexing for Agentic Contact Center for Banking](../../fso-front-office-banking/task/configure-ai-indexing-fso-contact-center.md).

You can choose which service provider to use for this skill [in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md).

