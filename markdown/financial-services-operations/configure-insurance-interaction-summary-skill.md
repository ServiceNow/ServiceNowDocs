---
title: Configure insurance customer interaction context summary skill in ServiceNow Otto for FSO
description: Configure the Insurance interaction context summary skill in ServiceNow Otto for FSO to enable AI-powered real-time summaries of insurance customer interactions in the Interaction page of Agentic Contact Center for Insurance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/configure-insurance-interaction-summary-skill.html
release: australia
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 2
breadcrumb: [Configuring Agentic Contact Center for Insurance, Agentic Contact Center for Insurance, Insurance applications, Financial Services Operations \(FSO\)]
---

# Configure insurance customer interaction context summary skill in ServiceNow Otto for FSO

Configure the Insurance interaction context summary skill in ServiceNow Otto for FSO to enable AI-powered real-time summaries of insurance customer interactions in the Interaction page of Agentic Contact Center for Insurance.

## Before you begin

Verify the ServiceNow Otto for Financial Services Operations \(FSO\) plugin \(`sn_fso_now_assist`\) and the Agentic Contact Center for Insurance plugin \(`com.sn_ins_csr`\) are installed.

-   For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
-   For general information about configuring AI skills in FSO, see [Configure Financial Services Operations AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-fso-now-assist-skills.md).

**Note:** This skill is dependent on the Insurance Customer Profile Summarization skill. Configure that skill before continuing. For more information, see [Configure insurance customer profile summarization in ServiceNow Otto for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-insurance-customer-profile-summarization.md).

Role required: admin

## About this task

The Insurance interaction context summary skill provides real-time interaction summaries with relevant customer context for insurance customers in the Interaction page. The skill surfaces key customer details, product ownership information, open cases, and recent activity within the conversation flow, allowing agents to access comprehensive customer information without navigating away from their workspace.

When activated, the skill generates the **Relevant details for this call** card in the Interaction page. The card is only displayed when the customer's identity has been verified and call context is available. For more information about the card, see &lt;xref to explore page&gt;.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills** to access the **Now Assist Skills** tab of the AI Admin Hub console.

2.  Select the **Customer** &gt; **FSO** workflow group.

3.  In the **Insurance interaction context summary** feature card, select **Activate skill**.

4.  In the **Define access** step, define the user access for the skill using Access Control Lists \(ACLs\).

    The roles `sn_ins_csr.servicing_agent` and `sn_ins_csr.claims_agent` are defined by default.

5.  Select **Save and continue**.

6.  In the **Select display** step, enable these options:

    -   In-product desktop
    -   ServiceNow Otto context menu
    For each option, select the arrow icon \(&gt;\) to define the roles that can use the skill.

7.  Select **Save and continue**.

8.  In the **Review and activate** step, review your choices and select **Activate** to complete the configuration.


## Result

The skill is activated. The **Relevant details for this call** card is displayed in the Interaction page for agents with the `sn_ins_csr.servicing_agent` or `sn_ins_csr.claims_agent` role when a verified customer interaction is in progress.

## What to do next

Configure AI indexing for the sources that this skill uses to retrieve insurance data and generate summaries. For more information, see [Configure AI indexing for Agentic Contact Center for Insurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-ai-indexing-agentic-contact-center-insurance.md).

You can choose which service provider to use for this skill [in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md).

