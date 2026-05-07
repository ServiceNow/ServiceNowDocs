---
title: Configure the Monitor project tasks AI agent in AI Agent Studio
description: Monitor project tasks autonomously by configuring the AI agent in the AI Agent Studio.
locale: en-US
release: australia
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Configure the Monitor project tasks AI agent in AI Agent Studio

Monitor project tasks autonomously by configuring the AI agent in the AI Agent Studio.

## Before you begin

The Project insights generation skill is activated by default. For more information on how to activate the skill if it isn't automatically activated or if you want to change the skill configuration, see [Configure Now Assist Admin features](../concept/configuring-na-spm.md).

Role required: admin or it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  From the Agentic workflows list, select Monitor project tasks AI agent.

    From the Monitor project tasks agentic workflow, each AI agent is shipped as active by default.

    **Note:** Only users with the Now Assist panel \(NAP\) role can access agents, even if the current agentic workflow doesn’t require that role.

3.  Enable the Monitor project tasks AI agent:

    1.  From Define key requirements screen, select **Continue**.
    2.  From Define user access screen, select **Continue**.
    3.  From Define data access screen, select **Continue**.
    4.  From Add triggers screen, select the **Project task update monitoring** and turn on the Trigger. Select **Save** and select **Continue**.
    5.  From the Select channels and status screen, select **Save and test**.
    The agentic workflow trigger defines the events that invoke AI agents for this agentic workflow. The trigger ensures that the AI agents can only start working upon specific key updates to project tasks.

4.  Navigate to **Workspaces** &gt; **Project Workspace** and select the project.

    The admin must enable the project insights generation skill for a specific project and set up a cadence for the project insights email. For more information on how to set up an email cadence, see the [Schedule the project insights email](email-project-summary-skill-pw.md).

5.  Enable the AI agent for a specific project:

    1.  [Schedule the project insights email](email-project-summary-skill-pw.md).
    2.  From the planning page, select the more actions icon \(![More actions icon.](../../innovation-management/image/more-options-icon.png)\) and then select **Enable critical task alerts**.

        **Note:** Enable critical task alerts option is only available when the email is scheduled. To disable the AI agent, select the more actions icon \(![More actions icon.](../../innovation-management/image/more-options-icon.png)\) and then select **Disable critical task alerts**.


## Result

The Monitor project tasks agents are enabled for the selected project.

**Related topics**  


[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

[Use AI agent or agentic workflows in Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-na-spm-ai-agents.md)

[Strategic Portfolio Management AI agents for the monitor project tasks agentic workflow](../concept/na-spm-task-monitoring-usecase.md)

