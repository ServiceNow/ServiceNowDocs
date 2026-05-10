---
title: Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection recommend risk signal solutions agentic workflow
description: Use the Analyze risk and recommend solutions agentic workflow to monitor and mitigate risks in customer engagements with minimal user intervention.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer Success Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection recommend risk signal solutions agentic workflow

Use the Analyze risk and recommend solutions agentic workflow to monitor and mitigate risks in customer engagements with minimal user intervention.

## Recommend risk signal solutions agentic workflow overview

**Note:** Before you use this agentic workflow, you must activate the AI Agents for Customer Success Management plugin \(com.sn\_cust\_succ\_ai\_agent\).

Use the Recommend risk signal solutions agentic workflow to:

-   Provide real-time risk analysis and generate detailed reports.
-   Identify common solutions and provide proactive recommendations.

Customer success managers can collaborate with customer success squad members to monitor risks, perform real-time risk analysis, generate detailed reports with proactive recommendations. This helps prevent escalations, improve customer retention, and enhance service quality. The agentic workflow can be used to assess and offer solutions for a risk signal.

You can trigger this workflow in two ways:

1.  **Recommend solutions button**
    1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.
    2.  From the **Customer Success** menu, select **All Risks and issues** and open a risk signal record.
    3.  Select the **Recommend solutions** button in the risk record
2.  Navigate to the [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md) panel in the **CSM/FSM Configurable Workspace** and specify a risk number to be resolved.

For information on how risks are generated, see [Define risk criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-setup-risk-defn.md).

## Configure the Recommend risk signal solutions agentic workflow

Before you use the agentic workflow, do the following:

-   Configure the Engagement risk solutions decision table to map risk categories to Customer Success definitions. The Recommend risk signal solutions agentic workflow uses these mappings to identify and recommend success plays for an unaddressed risk signal. The decision table contains the following columns:

    -   Rank: The order in which the conditions are evaluated.
    -   Category: The category of the risk signal, from the Risk Signal and Issues table.
    -   Customer Success Definition: The Customer Success definition to use for the risk category. Each Customer Success definition specifies the subflow to execute when the solution option is selected. See [Create a customer success definition record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-create-ale-defn.md) for details. You can map multiple definitions to the same category.![Engagement risk definition table](../image/risk-decision-table.jpg)
    See [Using decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/using-decision-builder.md) for details on configuring the decision table.

-   The solution subflow must contain the following input:

    Risk system ID: This is the system ID of the risk signal for which the solution is being created.

-   The solution subflow must return the following output:

    Generated record: An array of objects representing the solution records to be associated with the risk signal. Each object must contain the table name and sys\_id of the solution record.


You can define additional inputs as needed, such as Due Date, to be used in subflow steps or to override default values.

**Note:** If you're using an earlier version of this agentic workflow, see [KB2764672](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2764672) for steps on how to update your decision table configuration.

## AI agents used in the Recommend risk signal solutions agentic workflow

The Analyze risks and recommend solutions agentic workflow uses specific AI agents to retrieve all unaddressed risks and recommend solutions.

|AI agent|AI agent role|
|--------|-------------|
|Success risk manager AI agent|Retrieves the unaddressed risk signal and provides solution recommendations.|

