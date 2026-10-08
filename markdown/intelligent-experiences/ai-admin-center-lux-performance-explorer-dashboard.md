---
title: Performance Explorer dashboard in AI Admin Center \(Lux UI\)
description: Use the Performance Explorer dashboard on the Analytics page to review and analyze the execution details of assistants and AI agents across your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-admin-center-lux-performance-explorer-dashboard.html
release: brazil
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, performance]
breadcrumb: [View AI assets usage and performance \(Lux UI\), Monitor, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Performance Explorer dashboard in AI Admin Center \(Lux UI\)

Use the Performance Explorer dashboard on the Analytics page to review and analyze the execution details of assistants and AI agents across your organization.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

**Note:** This topic describes the AI Admin Center feature based on the Lux user interface \(UI\). If you're using the Next Experience UI for AI Admin Center, see the Next Experience UI version of this topic.

## AI Admin Center Performance Explorer dashboard

The Performance Explorer dashboard displays execution-level details for AI agents, skills, and assistants. Use the dashboard to investigate individual executions, analyze performance metrics, and identify patterns across your AI asset deployments.

The Performance Explorer dashboard includes the following sub-tabs: **Skills**, **Assistants**, and **Agents**. Each sub-tab displays a table of individual executions for the selected asset type.

## Skills

The **Skills** tab displays a list of individual generative AI skill executions. Use the **Date**, **Type**, and **Product** filters, or the **Search name** field, to narrow results. Select **Reset Filters** to clear all applied filters.

\[Omitted image "ai-admin-center-lux-analytics-performance-explorer-skills.png"\] Alt text: Skills tab on the AI Admin Center Analytics page.

-   **Skill Name**

    The name of the AI skill that was executed.

-   **Invocation Count**

    The number of invocations made to the skill.

-   **Assist Count**

    The number of assist credits consumed by the skill during the execution.

-   **Positive Feedback**

    The total number of positive feedback records received for the skill execution.

-   **Negative Feedback**

    The total number of negative feedback records received for the skill execution.

-   **Unique User Count**

    The number of unique users during the execution.


## Assistants

The **Assistants** tab displays a list of individual assistant executions. Use the **Date** filter to narrow results.

\[Omitted image "ai-admin-center-lux-analytics-performance-explorer-assistants.png"\] Alt text: Assistants tab on the AI Admin Center Analytics page.

-   **Assistant Name**

    The name of the assistant that was executed. Select the assistant name to view the full execution record.

-   **Total conversations**

    The total number of conversations where the assistant was executed.

-   **Cumulative AI-Assisted Actions**

    The number of all AI-assisted actions performed by the assistant during the execution.

-   **Average Distinct Users**

    The average number of distinct users during the execution.

-   **Deflection Rate**

    The rate of deflection success for the execution.

-   **Overall Average Conversation CSAT**

    The average customer satisfaction score for the conversation, calculated based on conversation signals.

-   **Total Assist Usage**

    The number of assist credits consumed by the assistant during the execution.


## Agents

The **Agents** tab displays a list of individual AI agent executions. Use the **Date**, **Type**, **Source**, and **Agent Type** filters, or the **Agent Name** field, to narrow results. Select **Reset filter** to clear all applied filters.

\[Omitted image "ai-admin-center-lux-analytics-performance-explorer.png"\] Alt text: Agents tab on the AI Admin Center Analytics page.

-   **Agent Name**

    The name of the AI agent that was executed.

-   **Type**

    The type of agentic AI asset, agent or agentic workflow.

-   **Executions**

    The total number of executions made by the agentic AI asset.

-   **Assist consumption**

    The number of assist credits consumed by the agentic AI asset during the execution.

-   **Tasks closed**

    The number of tasks closed resulting from the execution.

-   **Avg CSAT**

    The average customer satisfaction score for the execution, calculated based on interaction signals.


**Parent Topic:**[View AI assets usage and performance in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-view-ai-usage.md)

