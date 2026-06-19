---
title: Configure banking customer profile summarization in Now Assist for FSO
description: Configure the Customer Profile Summarization skill in Now Assist for FSO to enable AI-powered summaries of banking customer information in Agentic Contact Center for Banking.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-customer-profile-summarization-fso.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure AI skills, Configure, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Configure banking customer profile summarization in Now Assist for FSO

Configure the Customer Profile Summarization skill in Now Assist for FSO to enable AI-powered summaries of banking customer information in Agentic Contact Center for Banking.

## Before you begin

Verify the Now Assist for Financial Services Operations \(FSO\) plugin \(sn\_fso\_gen\_ai\) is installed.

-   For information about the plugin dependencies and plugin activation order, see [Application information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/supporting-information-for-now-assist-for-financial-services-operations-fso.md).
-   For information about the installation process, see .

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Select the **Customer** &gt; **FSO** workflow group.

3.  In the **Customer Profile Summarization** feature card, select **Activate skill**.

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

You can choose which service provider to use for this skill in the Now Assist Admin console.

**Parent Topic:**[Configure Financial Services Operations Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-fso-now-assist-skills.md)

