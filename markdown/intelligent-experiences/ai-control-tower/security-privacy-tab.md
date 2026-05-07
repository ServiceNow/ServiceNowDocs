---
title: Security &amp; Privacy tab in AI Control Tower
description: Review AI asset security metrics such as access issues, dormant and privileged AI agents, and map the relationships of your ServiceNow agents, agentic workflows, and tools.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [AI Control Tower Home, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Security &amp; Privacy tab in AI Control Tower

Review AI asset security metrics such as access issues, dormant and privileged AI agents, and map the relationships of your ServiceNow agents, agentic workflows, and tools.

The **Security &amp; Privacy** tab of AI Control Tower offers a dashboard-based overview of your AI asset security metrics. The dashboard contains several visualizations detailing AI asset security metrics. In addition to tracking metrics the **Security &amp; Privacy** tab contains the access map, a tool that gives an node-graph visualization of the relationships between your ServiceNow agents, agentic workflows, and tools. You can use the map to investigate the relationships between your AI agents and workflows further.

**Note:** You can drill down into the data on each widget by selecting the chart.

![The AI Control Tower Dashboard](../image/sp-tab-dashboard.png)

## ServiceNow AI Insights

ServiceNow AI Insights require that the Now Assist AICT Security Posture Summarizer skill is enabled. For more details, see [Activate a Now Assist skill](../../now-assist-admin/task/configure-a-now-assist-skill.md).

AI Control Tower AI insights summarize positives and potential issues to remediate to improve the overall security posture of your instance.

-   Positives: Enabled settings and features that help improve your security posture.
-   Areas for Attention: Low- to medium-risk items to resolve.
-   High Impact Observations: High-risk items to resolve.
-   Actions: Suggested action items to address Areas for Attention and High-Impact Observations.

## Access map

The **Access map** displays a node map detailing the relationships of your ServiceNow® agents, agentic workflows, and tools. You can use the map to review these relationships, configure agent details, and resolve access issues. The map includes filters for both agents and agentic workflows. You can open the access map by either navigating to **All** &gt; **AI Security and Privacy** &gt; **Access Map**, or selecting the link in the dashboard. See [Using the access map](../task/using-the-access-map.md) to learn how to use access map.

![AI Control Tower access map.](../image/sp-tab-access-map.png)

If a warning icon appears on any agent, that agent may have access issues. Select the warning icon to see details such as the workflow, agent, and tool associated with the access issue.

In Access issues, the User ID is the ID of the user who ran the agent.

![AI Control Tower access map with access issues shown.](../image/sp-tab-access-map-2.png)

## AI Asset Security Score

The AI asset security score is a measure of the health of your AI assets in terms of access issues, privileged AI agents, and dormant AI systems.

![ServiceNow AI asset security score.](../image/sp-tab-ai-score.png)

-   **AI assets impacting your score**

    To see more information about your score, select **See details** in the **Security &amp; Privacy** tab. A list view shows the AI assets that are included in your AI asset security score calculation. Your score is the average of all managed AI assets listed. Users should actively manage and review their agent assets and not rely solely on this AI asset security score.

    You can exclude an AI asset from your score by selecting a row and selecting **Mute**. For example, you can mute an AI asset if you determine that remediating the asset’s issue would be a risky change. You can also configure the score to remove LLM guardrail categories from the score or change the weights of categories. For more information, see [Data sharing, Data overflow processing, and Security &amp; privacy in AI Control Tower](data.md).

<table id="simpletable_nqz_1sl_mhc"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI system

</td><td>

Name of the AI asset.

</td></tr><tr><td>

Category

</td><td>

Type of issue, such as dormant AI system, privileged AI agent, or access issue.

</td></tr><tr><td>

Provider

</td><td>

Whether the asset is provided by ServiceNow or is external.

</td></tr><tr><td>

Score impact

</td><td>

The percentage impact to your AI asset security score.

</td></tr><tr><td>

Date

</td><td>

Date the issue occurred.

</td></tr><tr><td>

AI Task

</td><td>

The AI asset security task to remediate the issue, if applicable.

</td></tr></tbody>
</table>
## Access

-   **Access issues**

    The Access issues chart displays the proportion of AI agents that may be experiencing access-related issues and lists the top AI systems with access issues. AI agents with access issues may be unable to complete their workflows due to the access issue. Hover over a portion of the chart to see the exact proportion and count of agents.

    ![Donut chart detailing the AI agent access issues.](../image/sp-tab-access-chart.png)

    You can create AI asset security tasks directly from the list view by selecting **Create AI task**. See all active AI asset security tasks in **AI assets** in the AI Task section. Access to this section requires the sn\_vsc.task\_manager role.

    Resolved AI asset security tasks that are over 180 days old are archived. Archival days can be configured in system properties.

-   **Privileged AI Agents**

    The area chart shows AI agents with elevated permissions such as an agent with admin or security admin permissions that can perform critical actions. Some workflows require AI agents have elevated permissions to complete. Hover over a portion of the chart to see the exact number of privileged agents on that day.

    To show AWS agent metrics, filter the metrics by selecting **AWS Bedrock** in the provider drop-down list. You must have an AWS account configured for your instance and the Now Assist AiSP AWS IAM Privileged Policy Checker skill enabled. For more details, see [AI connections](ai-discovery-setup.md) and [Activate a Now Assist skill](../../now-assist-admin/task/configure-a-now-assist-skill.md).

    ![Area chart detailing the privileged AI agents.](../image/sp-tab-privilage-chart.png)

    You can create AI asset security tasks directly from the list view by selecting **Create AI task**. See all active AI asset security tasks in **AI assets** in the AI Task section. \(Role required: sn\_vsc.task\_manager.\)

    Resolved AI asset security tasks that are over 180 days old are archived. Archival days can be configured in system properties.

-   **Dormant AI systems**

    The area chart shows AI agents that have not been active for over 90 days. Review dormant AI agent permissions to reduce security risk. Hover over a portion of the chart to see the exact number of dormant AI systems for that day.

    To show AWS agent metrics, filter the metrics by selecting **AWS Bedrock** in the provider drop-down list. You must have an AWS account configured for your instance. For more details, see [AI connections](ai-discovery-setup.md).

    ![Area chart detailing dormant AI systems.](../image/sp-tab-dormant-chart.png)

    When an AI agent becomes dormant, an AI asset security task is created automatically to streamline your workflow, and quickly resolve issues. The AI asset security task is assigned to the agent’s owner. See all active AI asset security tasks in **AI assets** in the AI Task section.

    Resolved AI asset security tasks that are over 180 days old are archived. Archival days can be configured in system properties.


## ServiceNow instance access to MCP servers

MCP server access metrics include MCP client-server interactions routed through this instance's AI Gateway. Interactions that bypass the AI Gateway or are routed through another instance's AI Gateway aren't included.

-   **Clients connecting to MCP servers**

    The Clients connecting to MCP servers chart shows the top 10 clients \(ServiceNow AI agents or registered third-party MCP clients\) connecting to MCP servers through this instance's AI Gateway. MCP server access metrics are captured for all client-server interactions routed through the AI Gateway. To see more clients, select the chart to drill down into the data.

-   **Authorized access attempts to MCP servers**

    The Authorized access attempts to MCP servers chart shows successful access attempts from MCP clients to MCP servers through this instance's AI Gateway. Clients include ServiceNow AI agents and registered third-party MCP clients. To see more attempts, select the chart to drill down into the data.

-   **Failed access attempts to MCP servers**

    The Failed access attempts to MCP servers chart shows unsuccessful access attempts from MCP clients to MCP servers through this instance's AI Gateway. Clients include ServiceNow AI agents and registered third-party MCP clients. To see more data, select the chart to drill down into the data.


## Guardrails

-   **Prompt injection**

    These charts show prompt injection data provided by Now Assist Guardian. To see data, enable Now Assist Guardian for your instance. For more details, see [Now Assist Guardian analytics](../../now-assist-analytics/concept/now-assist-guardian-analytics.md).

-   **Offensive content**

    These charts show offensive content data provided by Now Assist Guardian. To see data, enable Now Assist Guardian for your instance. For more details, see [Now Assist Guardian analytics](../../now-assist-analytics/concept/now-assist-guardian-analytics.md).

-   **Sensitive data**

    The Sensitive data detected chart shows sensitive data that was identified in user responses to Now Assist prompts. Exposure of sensitive data is limited to the LLM in your instance.

    The Sensitive data anonymized chart shows prompt data that met configured data patterns. This data was anonymized based on the configuration for the pattern in Configuration Data Patterns in Data Privacy.

-   **Data integrity incident detection**

    The Data integrity incident detection chart is designed to help show potential violations of certain LLM guardrail policies. We analyze the AI agent’s output from each of its tasks deterministically to detect potential violations. You can choose to include or omit these policies. For more information about policies and how to configure data for this chart, see [Data sharing, Data overflow processing, and Security &amp; privacy in AI Control Tower](data.md).

-   **Agent goal deviation**

    The Agent goal deviation chart is designed to help identify when AI agents may have deviated from their intended role or objective during execution. Deviations include but aren’t limited to unauthorized actions or prompt injection attempts. The data is collected by analyzing agent execution history and then evaluated by AI. You can choose the data models to include or omit. Due to the probabilistic nature of the analysis by data model, not all occurrences may be identified. For information on how to configure data for this chart, see [Data sharing, Data overflow processing, and Security &amp; privacy in AI Control Tower](data.md).

-   **AI agent output with PII detected**

    The AI agent output with PII detected chart shows when agents' LLM output potentially contains personally identifiable information \(PII\). The data is collected by analyzing LLM output for PII sensitive data patterns specified in Data Privacy and additional PII patterns. These are the default Data Privacy sensitive data patterns: credit card, date of birth, email, Social Security number, U.S. bank ABA routing number, and U.S. phone number.

    We analyze the AI agent's output from each of its tasks deterministically based on the widely known patterns listed to find out potential security vulnerabilities. For example, U.S. phone number, credit card number, or Social Security number.

    You can choose to include or omit potential PII patterns to detect. For information on how to configure data for this chart, see [Data sharing, Data overflow processing, and Security &amp; privacy in AI Control Tower](data.md).

-   **Agentic output injection detection**

    The Agentic output injection detection chart shows when agents' LLM output potentially contains known security-vulnerable patterns. These patterns are Eval-Function-Audit, Html-Tag-injection, Non-printable-class, Script-Tag-injection, SQL-query-injection, and Terminal-RCE from the sn\_data\_discovery\_data\_pattern table in the AI Security and Privacy application.

    We analyze the AI agent's output from each of its tasks deterministically based on the patterns listed to find out potential security vulnerabilities. For example, HTML tags shouldn't have scripts associated with them for cross-site script attacks \(XSS\), or stacked SQL queries could result in SQL injection attacks.

    You can choose to include or omit potential patterns to detect. For information on how to configure data for this chart, see [Data sharing, Data overflow processing, and Security &amp; privacy in AI Control Tower](data.md).

    **Note:** These security-vulnerable patterns are ever-evolving, so not all patterns may be identified.


