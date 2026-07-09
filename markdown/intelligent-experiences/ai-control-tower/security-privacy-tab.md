---
title: Security &amp; Privacy tab in AI Control Tower
description: Review AI security metrics such as access issues, dormant and privileged AI agents, and map the relationships of your ServiceNow Agents, agentic workflows, and tools. Check your entitlements to determine whether you have access to AI Control Tower Security and Privacy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/intelligent-experiences/ai-control-tower/security-privacy-tab.html
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [AI Control Tower Home, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Security &amp; Privacy tab in AI Control Tower

Review AI security metrics such as access issues, dormant and privileged AI agents, and map the relationships of your ServiceNow Agents, agentic workflows, and tools. Check your entitlements to determine whether you have access to AI Control Tower Security and Privacy.

The **Security &amp; Privacy** tab of AI Control Tower offers a dashboard-based overview of your AI security metrics. The dashboard contains several visualizations detailing AI security metrics. In addition to tracking metrics the **Security &amp; Privacy** tab contains the access map, a tool that gives an node-graph visualization of the relationships between your ServiceNow Agents, agentic workflows, and tools. You can use the map to investigate the relationships between your AI agents and workflows further.

**Note:** You can drill down into the data on each widget by selecting the chart.

## Dashboard

\[Omitted image "sp-tab-dashboard.png"\] Alt text: The AI Control Tower dashboard

-   **Access issues**

    The chart displays the proportion of AI Agents experiencing access issues to AI agents without any issues, and lists the top AI systems with access issues. Agents with access issues may be unable to complete their workflows due to the access issue. Hover over a portion of the chart to see the exact proportion and count of agents.

    \[Omitted image "sp-tab-access-chart.png"\] Alt text: A donut chart detailing AI access

    You can create AI security tasks directly from the list view by selecting **Create AI task**. See all active AI security tasks in **AI assets** in the AI Task section. \(Role required: sn\_vsc.task\_manager.\)

    AI security tasks that are resolved and over 180 days old are archived. Archival days can be configured in system properties.

-   **Autonomous vs. supervised agentic tools**

    The chart displays the proportion of autonomous \(self-driven\) to supervised \(human-guided\) agentic tools in use. Hover over a portion of the chart to see the exact proportion and count of agents.

    To show AWS agent metrics, filter the metrics by selecting **AWS Bedrock** in the provider dropdown list. You must have an AWS account configured for your instance. For more details, see [AI connections setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/ai-control-tower/ai-discovery-setup.md).

    \[Omitted image "sp-tab-workflow-chart.png"\] Alt text: A donut chart detailing agentic tools.

-   **Privileged AI Agents**

    The area chart shows AI agents with elevated permissions such as an agent with admin or security admin permissions that can perform critical actions. Some workflows require AI agents have elevated permissions to complete. Hover over a portion of the chart to see the exact number of privileged agents on that day.

    To show AWS agent metrics, filter the metrics by selecting **AWS Bedrock** in the provider dropdown list. You must have an AWS account configured for your instance and the Now Assist AiSP AWS IAM Privileged Policy Checker skill enabled. For more details, see [AI connections setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/ai-control-tower/ai-discovery-setup.md) and [Activate a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/configure-a-now-assist-skill.md).

    \[Omitted image "sp-tab-privilage-chart.png"\] Alt text: An area chart detailing privileged AI agents

    You can create AI security tasks directly from the list view by selecting **Create AI task**. See all active AI security tasks in **AI assets** in the AI Task section. \(Role required: sn\_vsc.task\_manager.\)

    AI security tasks that are resolved and over 180 days old are archived. Archival days can be configured in system properties.

-   **Dormant AI systems**

    The area chart shows AI agents that have not been active for over 90 days. Review dormant AI agent permissions to reduce security risk. Hover over a portion of the chart to see the exact number of dormant AI systems for that day.

    To show AWS agent metrics, filter the metrics by selecting **AWS Bedrock** in the provider dropdown list. You must have an AWS account configured for your instance. For more details, see [AI connections setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/ai-control-tower/ai-discovery-setup.md).

    \[Omitted image "sp-tab-dormant-chart.png"\] Alt text: An area chart detailing dormant AI systems.

    When an AI agent becomes dormant, an AI security task is created automatically to streamline your workflow and quickly resolve issues. The AI security task is assigned to the agent’s owner. See all active AI security tasks in **AI assets** in the AI Task section.

    AI security tasks that are resolved and over 180 days old are archived. Archival days can be configured in system properties.

-   **Prompt injection**

    These charts show prompt injection data provided by Now Assist Guardian. To see data, enable Now Assist Guardian for your instance. For more details, see [Now Assist Guardian analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-guardian-analytics.md).

-   **Offensive content**

    These charts show offensive content data provided by Now Assist Guardian. To see data, enable Now Assist Guardian for your instance. For more details, see [Now Assist Guardian analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-guardian-analytics.md).


## Access map

The **Access map** displays a node map detailing the relationships of your ServiceNow® agents, agentic workflows, and tools. You can use the map to review these relationships, configure agent details, and resolve access issues. The map includes filters for both agents and agentic workflows. You can open the access map by either navigating to **All** &gt; **AI Security and Privacy** &gt; **Access Map**, or selecting the link in the dashboard. \[Omitted image "sp-tab-access-map.png"\] Alt text: The AI control tower access map

If a warning icon appears on any agent, that agent has access issues. Select the warning icon to see details such as the workflow, agent, and tool associated with the access issue.

In Access issues, the User ID is the ID of the user who ran the agent.

## ServiceNow AI Insights

ServiceNow AI Insights require that the Now Assist AICT Security Posture Summarizer skill is enabled. For more details, see [Activate a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/configure-a-now-assist-skill.md).

ServiceNow AI insights summarize positives and potential issues to remediate to improve your overall security posture of your instance.

-   Positives – Enabled settings and features that improve your security posture.
-   Areas for Attention – Low- to medium-risk items to resolve.
-   High Impact Observations – High-risk items to resolve.
-   Actions – Suggested action items to address Areas for Attention and High-Impact Observations.

## ServiceNow AI Security Score

The ServiceNow AI security score is a measure of the health of your ServiceNow AI assets in terms of access issues, privileged AI agents, and dormant AI systems.\[Omitted image "image.sp-tab-ai-score"\] Alt text: ServiceNow AI security score

-   **AI assets impacting your score**

    To see more information about your score, select **See details** in the Security and Privacy tab. A list view shows the ServiceNow AI assets that are included in your AI security score calculation. Your score is the average of all ServiceNow AI assets listed.

    You can exclude an asset from your score by selecting a row and selecting **Mute**. For example, you can mute an AI asset if you determine that remediating the asset’s issue would be a risky change.

<table id="simpletable_nqz_1sl_mhc"><thead><tr><th align="left" id="d108865e19">

Column

</th><th align="left" id="d108865e22">

Description

</th></tr></thead><tbody><tr><td>

AI system

</td><td>

Name of the ServiceNow asset.

</td></tr><tr><td>

Category

</td><td>

Type of issue, such as dormant AI system, privileged AI agent, or access issue.

</td></tr><tr><td>

Provider

</td><td>

This is always ServiceNow.

</td></tr><tr><td>

Score impact

</td><td>

The percentage impact to your AI security score.

</td></tr><tr><td>

Date

</td><td>

Date the issue occurred.

</td></tr><tr><td>

AI Task

</td><td>

The AI security task to remediate the issue, if applicable.

</td></tr></tbody>
</table>
