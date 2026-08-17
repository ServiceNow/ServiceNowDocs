---
title: Configure the Monitor project tasks AI agent in AI Agent Studio
description: Monitor project tasks autonomously by configuring the AI agent in the AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/now-assist-for-strategic-portfolio-management-spm/configure-agents-project-task-monitoring.html
release: zurich
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [AI Agents, Agentic AI]
breadcrumb: [Configure, ServiceNow Otto for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Configure the Monitor project tasks AI agent in AI Agent Studio

Monitor project tasks autonomously by configuring the AI agent in the AI Agent Studio.

## Before you begin

Role required: admin or it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  From the Agentic workflows list, select Monitor project tasks AI agent.

    From the Monitor project tasks agentic workflow, each AI agent is shipped as active by default.

    **Note:** Only users with the AI admin role can access agents, even if the current agentic workflow doesn’t require that role.

3.  Enable the Monitor project tasks AI agent:

    1.  From Define key requirements screen, select **Continue**.
    2.  From Define user access screen, select **Continue**.
    3.  From Define data access screen, select **Continue**.
    4.  From Add triggers screen, select the Project task update monitoring and turn on the Trigger. Select **Save** and select **Continue**.
    5.  From the Select channels and status screen, select **Save and test**.
    The agentic workflow trigger defines the events that invoke AI agents for this agentic workflow. The trigger ensures that the AI agents can only start working upon specific key updates to project tasks.

4.  Navigate to **Workspaces** &gt; **Project Workspace** and select the project.

    The admin must enable the project insights generation skill for a specific project and set up a cadence for the project insights email. For more information on how to set up an email cadence, see the .

5.  Enable the AI agent for a specific project:

    1.  .
    2.  From the planning page, select the more actions icon \(\[Omitted image "more-options-icon.png"\] Alt text: More actions icon.\) and then select **Enable critical task alerts**.

        **Note:** Enable critical task alerts option is only available when the email is scheduled. To disable the AI agent, select the more actions icon \(\[Omitted image "more-options-icon.png"\] Alt text: More actions icon.\) and then select **Disable critical task alerts**.

    The Monitor project tasks agents are enabled for the selected project.


**Parent Topic:**[Configure AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/now-assist-for-strategic-portfolio-management-spm/configuring-na-spm.md)

**Related topics**  


[Configure AI agents and AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-ai-agents.md)

[Install ServiceNow Otto AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-ai-agents-plugins.md)

[Using AI agent or agentic workflows in ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/now-assist-for-strategic-portfolio-management-spm/using-na-spm-ai-agents.md)

[Strategic Portfolio Management AI agents for the monitor project tasks agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/now-assist-for-strategic-portfolio-management-spm/na-spm-task-monitoring-usecase.md)

