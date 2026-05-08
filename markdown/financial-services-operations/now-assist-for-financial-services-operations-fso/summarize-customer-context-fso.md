---
title: Summarize customer interaction context in the Interaction page
description: The customer interaction context summary skill is used in the Interaction page. It automatically generates a structured summary of customer service interactions, helping banking service representatives quickly understand customer context and interaction history.
locale: en-US
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Summarize customer interaction context in the Interaction page

The customer interaction context summary skill is used in the Interaction page. It automatically generates a structured summary of customer service interactions, helping banking service representatives quickly understand customer context and interaction history.

## Before you begin

This skill uses indexed sources for AI search that requires configuration after install. For more information, see [Configure AI indexing for Agentic Contact Center for Banking](../../fso-front-office-banking/task/configure-ai-indexing-fso-contact-center.md).

Role required: sn\_fso\_csr.business\_agent, sn\_fso\_csr.personal\_agent

**Note:** These roles are the default list of roles that are defined for this task. Administrators can modify the list of roles in the Now Assist Admin console.

## About this task

The customer interaction context summary skill provides a structured, context-aware summary of a customer service interaction in the Interaction page as part of Agentic Contact Center for Banking.

![Customer context summary panel showing customer information, contact reason, related cases, and related products with balances.](../../fso-front-office-banking/images/agentic-contact-center-interaction-context-summary.png)

## Procedure

1.  Navigate to **Workspaces** &gt; **Financial Services Workspace**.

2.  Initiate an interaction.

    -   When a customer initiates a call, select **Accept** in the inbox item.
    -   Manually create a new phone interaction record in the workspace.
    The Interaction page displays.

    The **Relevant details for this call** component generates a contextual summary of the customer's interaction.

3.  After the summary is generated, you can perform additional actions.

<table id="choicetable_ybr_pjr_mbc"><thead><tr><th align="left" id="d54410e150">

Option

</th><th align="left" id="d54410e153">

Procedure

</th></tr></thead><tbody><tr><td id="d54410e159">

**Provide feedback for the summary**

</td><td>

If you think the summary was helpful, select the helpful icon \(![](../../customer-service-management/image/icon-helpful.png)\). If you think the summary wasn't helpful, select the not helpful icon \(![](../../customer-service-management/image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d54410e180">

**View the information about the case summary**

</td><td>

To review details about the summary, select the more info icon \(![](../../customer-service-management/image/icon-more-info.png)\).

</td></tr><tr><td id="d54410e194">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![](../../customer-service-management/image/icon-expand.png)\) or the collapse card icon \(![](../../customer-service-management/image/icon-collapse.png)\) to see more details or fewer summary details.

</td></tr></tbody>
</table>
## What to do next

Engage with an AI agent to get further analysis and suggested responses for this interaction. For more information, see [Request AI agent support in the Interaction page](request-ai-agent-interaction-workspace.md).

**Parent Topic:**[Using generative AI in Now Assist for Financial Services Operations \(FSO\)](../../fso-common/concept/using-now-assist-for-financial-services-operations-fso.md)

**Related topics**  


[Using generative AI in Now Assist for Financial Services Operations \(FSO\)](../../fso-common/concept/using-now-assist-for-financial-services-operations-fso.md)

[Configure customer interaction context summary skill in Now Assist for FSO](configure-customer-contextual-summarization-fso.md)

