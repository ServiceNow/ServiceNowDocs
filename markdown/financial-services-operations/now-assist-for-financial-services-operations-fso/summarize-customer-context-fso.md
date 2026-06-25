---
title: Summarize banking customer interaction context in the Interaction page
description: The Customer Interaction Context Summary skill is used in the Interaction page. It automatically generates a structured summary of customer service interactions, helping banking service representatives quickly understand customer context and interaction history.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-customer-context-fso.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Summarize banking customer interaction context in the Interaction page

The Customer Interaction Context Summary skill is used in the Interaction page. It automatically generates a structured summary of customer service interactions, helping banking service representatives quickly understand customer context and interaction history.

## Before you begin

This skill uses indexed sources for AI search that requires configuration after install. For more information, see [Configure AI indexing for Agentic Contact Center for Banking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/configure-ai-indexing-fso-contact-center.md).

Role required: sn\_fso\_csr.business\_agent, sn\_fso\_csr.personal\_agent

**Note:** These roles are the default list of roles that are defined for this task. Administrators can modify the list of roles in the Now Assist Admin console.

## About this task

The customer interaction context summary skill provides a structured, context-aware summary of a customer service interaction in the Interaction page as part of Agentic Contact Center for Banking.

\[Omitted image "agentic-contact-center-interaction-context-summary.png"\] Alt text: Customer context summary panel showing customer information, contact reason, related cases, and related products with balances.

## Procedure

1.  Navigate to **Workspaces** &gt; **Financial Services Workspace**.

2.  Initiate an interaction.

    -   When a customer initiates a call, select **Accept** in the inbox item.
    -   Manually create a new phone interaction record in the workspace.
    The Interaction page displays.

    The **Relevant details for this call** component generates a contextual summary of the customer's interaction.

3.  After the summary is generated, you can perform additional actions.

<table id="choicetable_ybr_pjr_mbc"><thead><tr><th align="left" id="d56290e150">

Option

</th><th align="left" id="d56290e153">

Procedure

</th></tr></thead><tbody><tr><td id="d56290e159">

**Provide feedback for the summary**

</td><td>

If you think the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text:\). If you think the summary wasn't helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text:\).This feedback improves the generative AI model and can help improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d56290e180">

**View the information about the case summary**

</td><td>

To review details about the summary, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text:\).

</td></tr><tr><td id="d56290e194">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(\[Omitted image "icon-expand.png"\] Alt text:\) or the collapse card icon \(\[Omitted image "icon-collapse.png"\] Alt text:\) to see more details or fewer summary details.

</td></tr></tbody>
</table>
## What to do next

Engage with an AI agent to get further analysis and suggested responses for this interaction. For more information, see [Request AI agent support in the Interaction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/request-ai-agent-interaction-workspace.md).

**Parent Topic:**[Using generative AI in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/using-now-assist-for-financial-services-operations-fso.md)

**Related topics**  


[Using generative AI in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/using-now-assist-for-financial-services-operations-fso.md)

[Configure banking customer interaction context summary skill in Now Assist for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-customer-contextual-summarization-fso.md)

