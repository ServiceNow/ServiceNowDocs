---
title: Configure insurance customer interaction context summary skill in Now Assist for FSO
description: Configure the Insurance interaction context summary skill in Now Assist for FSO to enable AI-powered real-time summaries of insurance customer interactions in the Interaction page of Agentic Contact Center for Insurance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-insurance-interaction-summary-skill.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 2
breadcrumb: [Configure AI skills, Configure, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Configure insurance customer interaction context summary skill in Now Assist for FSO

Configure the Insurance interaction context summary skill in Now Assist for FSO to enable AI-powered real-time summaries of insurance customer interactions in the Interaction page of Agentic Contact Center for Insurance.

## Before you begin

Verify the Now Assist for Financial Services Operations \(FSO\) plugin \(`sn_fso_now_assist`\) and the Agentic Contact Center for Insurance plugin \(`com.sn_ins_csr`\) are installed.

-   For information about the plugin dependencies and plugin activation order, see [Application information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/supporting-information-for-now-assist-for-financial-services-operations-fso.md).
-   For information about the installation process, see .

**Note:** This skill is dependent on the Insurance Customer Profile Summarization skill. Configure that skill before continuing. For more information, see [Configure insurance customer profile summarization in Now Assist for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-insurance-customer-profile-summarization.md).

Role required: admin

## About this task

The Insurance interaction context summary skill provides real-time interaction summaries with relevant customer context for insurance customers in the Interaction page. The skill surfaces key customer details, product ownership information, open cases, and recent activity within the conversation flow, allowing agents to access comprehensive customer information without navigating away from their workspace.

When activated, the skill generates the **Relevant details for this call** card in the Interaction page. The card is only displayed when the customer's identity has been verified and call context is available. For more information about the card, see &lt;xref to explore page&gt;.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Select the **Customer** &gt; **FSO** workflow group.

3.  In the **Insurance interaction context summary** feature card, select **Activate skill**.

4.  In the **Define access** step, define the user access for the skill using Access Control Lists \(ACLs\).

    The roles `sn_ins_csr.servicing_agent` and `sn_ins_csr.claims_agent` are defined by default.

5.  Select **Save and continue**.

6.  In the **Select display** step, enable these options:

    -   In-product desktop
    -   Now Assist context menu
    For each option, select the arrow icon \(&gt;\) to define the roles that can use the skill.

7.  Select **Save and continue**.

8.  In the **Review and activate** step, review your choices and select **Activate** to complete the configuration.


## Result

The skill is activated. The **Relevant details for this call** card is displayed in the Interaction page for agents with the `sn_ins_csr.servicing_agent` or `sn_ins_csr.claims_agent` role when a verified customer interaction is in progress.

## What to do next

Configure AI indexing for the sources that this skill uses to retrieve insurance data and generate summaries. For more information, see &lt;xref to configure AI indexing&gt;.

You can choose which service provider to use for this skill in the Now Assist Admin console.

**Parent Topic:**[Configure Financial Services Operations Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-fso-now-assist-skills.md)

