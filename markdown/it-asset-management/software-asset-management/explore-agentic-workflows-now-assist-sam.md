---
title: Agentic workflows in ServiceNow Otto for Software Asset Management \(SAM\)
description: Agentic workflows in ServiceNow Otto for Software Asset Management \(SAM\) enable ServiceNow Otto for SAM managers to manage software requests, create reclamation rules, and evaluate software removal candidates reducing manual effort and improving operational efficiency.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/explore-agentic-workflows-now-assist-sam.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 2
breadcrumb: [AI in Software Asset Management, Explore, Software Asset Management, IT Asset Management, Asset Management]
---

# Agentic workflows in ServiceNow Otto for Software Asset Management \(SAM\)

Agentic workflows in ServiceNow Otto for Software Asset Management \(SAM\) enable ServiceNow Otto for SAM managers to manage software requests, create reclamation rules, and evaluate software removal candidates reducing manual effort and improving operational efficiency.

<table id="table_hrp_zyl_m2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

[Help manage software request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/now-assist-sam-fulfill-sw-asset-requests-workflow.md)

</td><td>

Fulfill a software asset request by either allocating the available entitlements, if sufficient rights exist, or generating a purchase order with the necessary line items for the requested software model.

</td><td>

-   Software entitlement allocation AI agent
-   Purchase order creation AI agent
-   Microsoft license assignment AI agent

</td></tr><tr><td>

[Create software reclamation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/now-assist-sam-create-software-reclamation-rule-workflow.md)

</td><td>

Analyze the license usage of a product and if no reclamation rule exists, prompt the user to create one.

</td><td>

Software reclamation rule creation AI agent

</td></tr><tr><td>

[Evaluate software removal candidate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/now-assist-sam-evaluate-removal-candidate-workflow.md)

</td><td>

Examine installed or subscription-based removal candidates for a software product by evaluating its software product usage within a specified period and the eligible total number of reclaimable candidates

</td><td>

Software removal candidate evaluation AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read only.

You can run the agentic workflow as is by activating the workflow. Additionally, you can [duplicate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md) the workflow if you want to customize the workflow. If you duplicate the agentic workflow, adjust the settings according to your requirements and then activate the duplicated agentic workflow. You can also [test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md) the duplicated agentic workflow to analyze its performance in the AI Agent Studio, while it executes the instructions that you defined.

When you activate the agentic workflow, activate all agents within the agentic workflow.

Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

There might be AI agents installed on your instance that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

**Parent Topic:**[AI in Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/exploring-now-assist-sam.md)

