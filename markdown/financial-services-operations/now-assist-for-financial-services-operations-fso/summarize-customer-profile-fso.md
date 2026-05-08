---
title: Summarize a customer profile in the Customer 360 page
description: Use the Customer profile summarization skill to generate an AI-powered overview of a customer's status and information within the Customer 360 page. This feature helps customer service representatives quickly understand a customer's status to provide personalized, real-time support.
locale: en-US
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Summarize a customer profile in the Customer 360 page

Use the Customer profile summarization skill to generate an AI-powered overview of a customer's status and information within the Customer 360 page. This feature helps customer service representatives quickly understand a customer's status to provide personalized, real-time support.

## Before you begin

Role required: sn\_fso\_csr.business\_agent, sn\_fso\_csr.personal\_agent

**Note:** These roles are the default list of roles that are defined for this task. Administrators can modify the list of roles in the Now Assist Admin console.

## About this task

The Customer profile summarization skill provides a concise, comprehensive summary of a customer's status in the Customer 360 workspace as part of Agentic Contact Center for Banking.

![Customer profile summary panel showing profile and status information.](../../fso-front-office-banking/images/agentic-contact-center-c360-context-summary.png)

## Procedure

1.  Navigate to **Workspaces** &gt; **Financial Services Workspace**.

2.  Open a customer record.

    The **Customer summary** component will generate a concise, comprehensive summary of the customer.

3.  After the summary is generated, you can perform additional actions.

<table id="choicetable_ybr_pjr_mbc"><thead><tr><th align="left" id="d43848e117">

Option

</th><th align="left" id="d43848e120">

Procedure

</th></tr></thead><tbody><tr><td id="d43848e126">

**Refresh the customer summary**

</td><td>

Select the refresh icon \(![Refresh icon.](../../fso-common/image/icon-refresh.png)\) to generate another customer summary.

</td></tr><tr><td id="d43848e141">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../../customer-service-management/image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../../customer-service-management/image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d43848e164">

**View the information about the case summary**

</td><td>

If you want to review details about the summary, select the more info icon \(![More info icon.](../../customer-service-management/image/icon-more-info.png)\).

</td></tr><tr><td id="d43848e179">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![Expand card icon.](../../customer-service-management/image/icon-expand.png)\) or the collapse card icon \(![Collapse card icon.](../../customer-service-management/image/icon-collapse.png)\) to see more details or fewer summary details.

</td></tr></tbody>
</table>
## What to do next

Use an AI agent to engage in Q&amp;A, anticipate customer needs, and surface insights. For more information, see [Generate customer insights in the Customer 360 page](generate-customer-insights-customer-360-workspace.md).

**Parent Topic:**[Using generative AI in Now Assist for Financial Services Operations \(FSO\)](../../fso-common/concept/using-now-assist-for-financial-services-operations-fso.md)

**Related topics**  


[Using generative AI in Now Assist for Financial Services Operations \(FSO\)](../../fso-common/concept/using-now-assist-for-financial-services-operations-fso.md)

[Configure customer profile summarization in Now Assist for FSO](configure-customer-profile-summarization-fso.md)

