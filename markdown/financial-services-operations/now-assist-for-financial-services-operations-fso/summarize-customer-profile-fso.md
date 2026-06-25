---
title: Summarize a banking customer profile in the Customer 360 page
description: Use the Customer Profile Summarization skill to generate an AI-powered overview of a customer's status and information within the Customer 360 page in Agentic Contact Center for Banking. This feature helps customer service representatives quickly understand a customer's status to provide personalized, real-time support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/summarize-customer-profile-fso.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Summarize a banking customer profile in the Customer 360 page

Use the Customer Profile Summarization skill to generate an AI-powered overview of a customer's status and information within the Customer 360 page in Agentic Contact Center for Banking. This feature helps customer service representatives quickly understand a customer's status to provide personalized, real-time support.

## Before you begin

Role required: sn\_fso\_csr.business\_agent, sn\_fso\_csr.personal\_agent

**Note:** These roles are the default list of roles that are defined for this task. Administrators can modify the list of roles in the Now Assist Admin console.

## About this task

The Customer profile summarization skill provides a concise, comprehensive summary of a customer's status in the Customer 360 workspace as part of Agentic Contact Center for Banking.

\[Omitted image "agentic-contact-center-c360-context-summary.png"\] Alt text: Customer profile summary panel showing profile and status information.

## Procedure

1.  Navigate to **Workspaces** &gt; **Financial Services Workspace**.

2.  Open a customer record.

    The **Customer summary** component will generate a concise, comprehensive summary of the customer.

3.  After the summary is generated, you can perform additional actions.

<table id="choicetable_ybr_pjr_mbc"><thead><tr><th align="left" id="d44584e120">

Option

</th><th align="left" id="d44584e123">

Procedure

</th></tr></thead><tbody><tr><td id="d44584e129">

**Refresh the customer summary**

</td><td>

Select the refresh icon \(\[Omitted image "icon-refresh.png"\] Alt text: Refresh icon.\) to generate another customer summary.

</td></tr><tr><td id="d44584e144">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\). If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d44584e167">

**View the information about the case summary**

</td><td>

If you want to review details about the summary, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text: More info icon.\).

</td></tr><tr><td id="d44584e182">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(\[Omitted image "icon-expand.png"\] Alt text: Expand card icon.\) or the collapse card icon \(\[Omitted image "icon-collapse.png"\] Alt text: Collapse card icon.\) to see more details or fewer summary details.

</td></tr></tbody>
</table>
## What to do next

Use an AI agent to engage in Q&amp;A, anticipate customer needs, and surface insights. For more information, see [Generate customer insights in the Customer 360 page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/generate-customer-insights-customer-360-workspace.md).

**Parent Topic:**[Using generative AI in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/using-now-assist-for-financial-services-operations-fso.md)

**Related topics**  


[Using generative AI in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/using-now-assist-for-financial-services-operations-fso.md)

[Configure banking customer profile summarization in Now Assist for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-customer-profile-summarization-fso.md)

