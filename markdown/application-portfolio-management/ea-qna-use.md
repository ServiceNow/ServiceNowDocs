---
title: Use Enterprise Architecture query agent
description: You can ask the Enterprise Architecture query agent natural language questions about your enterprise architecture portfolio using the Now Assist panel in Enterprise Architecture Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/ea-qna-use.html
release: australia
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 2
breadcrumb: [Use Now Assist, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture]
---

# Use Enterprise Architecture query agent

You can ask the Enterprise Architecture query agent natural language questions about your enterprise architecture portfolio using the Now Assist panel in Enterprise Architecture Workspace.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Before using the Enterprise Architecture query agent with CMDB relationship data, confirm that an administrator has activated the required Knowledge Graph system properties. For information, see [Enable Knowledge Graph system properties for the Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/set-kg-system-properties-ea-qna.md). Also, check if the Now Assist panel is active. For information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

Role required:

-   sn\_apm.apm\_user or sn\_apm.apm\_read
-   now\_assist\_panel\_user

## About this task

The Enterprise Architecture query agent returns structured answers based on your enterprise architecture data. Depending on the question, the response may include a list of records, field values, trend comparisons, or an impact summary. The agent retains context within a session, so follow-up questions the agent interprets without requiring you to restate the original question.

Example questions:

-   List business apps with CSAT score greater than 6 and technical risk score greater than 8
-   List all capabilities of a business application along with all their scores
-   Get the owner of a business application
-   List business apps supported by multiple capabilities
-   Get business applications without owners
-   List top-level capabilities
-   List business applications not assigned to capabilities
-   List applications that are candidates for retirement

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Now Assist panel.

    Use one of the following methods:

    -   Select the Now Assist icon \(\[Omitted image "now-assist-panel-icon.png"\] Alt text: Now Assist icon\) in the navigation bar.
    -   Select the **Ask Now Assist** button on the Enterprise Architecture Workspace homepage.
    \[Omitted image "ea-qna-icons.png"\] Alt text: The Enterprise Architecture Workspace home page with the Now Assist icon and Ask Now Assist icons highlighted.

3.  In the **Reply to Now Assist** field, type your question in natural language.

4.  Press Enter or select the send icon.

    The agent searches for relevant data and actions. A **Processing** indicator appears while the agent works.

5.  Review the response.

    After returning a response, the agent may display related questions. Select a suggestion or type a follow-up question to continue exploring your enterprise architecture data.


## Result

The Enterprise Architecture query agent returns a structured answer based on your enterprise architecture data. The agent retains context within a session, so follow-up questions such as `Now show me their owners` the agent interprets without requiring you to restate the original question.

**Parent Topic:**[Using Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/using-now-assist-for-ea.md)

**Related topics**  


[Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ea-qna-overview.md)

[Using AI agent agentic workflow in Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/using-na-ea-ai-agents.md)

[Enable Knowledge Graph system properties for the Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/set-kg-system-properties-ea-qna.md)

