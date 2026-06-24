---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) Support renewals and expansion
description: Assess contracts due for renewal, analyze trends, and recommend renewal strategies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-renewal-analyzer.html
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Customer Success Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) Support renewals and expansion

Assess contracts due for renewal, analyze trends, and recommend renewal strategies.

## Support renewals and expansion agentic workflow overview

The Support renewals and expansion agentic workflow enables customer success agents to assess the health, value, and product adoption of a contract. It provides data driven insights and renewal play recommendations and enables customer success agents to manage multiple customer engagements efficiently. Customer success managers can use the Support renewals and expansion agentic workflow to:

-   Track how much value has been delivered since onboarding.
-   Measure progress against goals and service delivery metrics.
-   Retrieve and calculate health and adoption scores.
-   Analyze trends to support informed adoption decisions.

**Note:** The Support renewals and expansion agentic workflow is available in read-only mode. Before using the workflow, you must make a copy and adjust the settings according to your requirements. See [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/clone-aia-usecase.md) for details.

## Role masking

Required role: sn\_acct\_lc.customer\_success\_agent

[Role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).

## Configure the Support renewals and expansion agentic workflow

Before you use the agentic workflow, you must configure the following fields in the Renewal analysis AI agent:

-   Engagement adoption source sysID
-   Contract adoption source sysID
-   Health source sysID
-   Time period \(in days\)
-   Metric aggregation type

**Note:** The source sysIDs must be configured correctly in the Data Context Engine as follows:

-   Health: Source and context table must be set to Engagement.
-   Engagement: Source table must be set to Sold Products and the context table must be set to Engagement.
-   Contract: Source table must be set to Sold Products and the context table must be set to Contract.

For more details on configuring the data sources, see [Set up the Data Context Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-setup-dce.md).

## Support renewals and expansion agentic workflow

**Note:** Before running the workflow, you must configure the generic prompt as follows:

1.  Navigate to the OneExtend Capability \(sys\_one\_extend\_capability\) table by entering `sys_one_extend_capability.list` in the navigator.
2.  Search for `generic prompt` and open the record.
3.  In OneExtend Capability Attributes related list, set the **Default** to **True** for any of these definitions:
    -   Generic Prompt \(Azure OpenAI Chat\)
    -   Generic Prompt \(Now LLM\)
    -   Generic Prompt Vertex AI \(Google Cloud Chat Completion\)
    -   Generic Prompt \(Amazon Bedrock Chat Completions\)

When a contract is due to expire in 90 days, the customer success manager receives a notification and the Support renewals and expansion workflow is automatically triggered. The contract health, value, and usage scans are initiated and the customer success manager can monitor the progress in the [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/now-assist-panel-overview.md).

When the workflow is completed, two reports are generated for the engagement and the associated contract \(that is due to expire in 90 days\) with the following details:

-   Renewal likelihood
-   Expansion potential
-   Recommended actions
-   Adoption trend
-   Health trend \(this is available only for engagements\)
-   Value score

You can then select the appropriate renewal play based on the report.

## Testing the agentic workflow

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  Follow the instructions in the [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/test-aia-use-case.md) section to test the agentic workflow.

**Example of Support renewals and expansion agentic workflow output in the ServiceNow**

\[Omitted image "renewal-analysis.png"\] Alt text: Support renewals and expansion agentic workflow output

## AI agents used in the Support renewals and expansion agentic workflow

The following AI agents are used to execute the instructions for the agentic workflow.

|AI agent|AI agent role|
|--------|-------------|
|Renewal analysis AI agent|Analyzes renewal possibilities and triggers appropriate renewal flows based on assessment results.|
|Value realization assessor AI agent|Analyzes value realized by tracking service metrics and customer goal achievement over time.|
|Success insight AI agent|Populates score data and delivers trend analysis to support informed decisions.|

**Parent Topic:**[Customer Success Management agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-health-risk.md)

