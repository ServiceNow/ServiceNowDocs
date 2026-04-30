---
title: Configure the Monitor project tasks agentic workflow in AI Agent Studio
description: Monitor project tasks agentic workflow in the AI Agent Studio.
locale: en-US
release: xanadu
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2025-02-20"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Configure the Monitor project tasks agentic workflow in AI Agent Studio

Monitor project tasks agentic workflow in the AI Agent Studio.

## Before you begin

To use Monitor project tasks, make sure that the email project summary skill is activated. For more information on how to activate the skill, see [Configure Now Assist for Strategic Portfolio Management \(SPM\)](configure-now-assist-for-spm.md).

Role required: admin or it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  Select **Monitor project tasks**.

3.  From the Monitor project tasks agentic workflow, each AI agent is shipped as active by default.

    **Note:** Only users with the Now Assist panel \(NAP\) role can access agents, even if the current agentic workflow doesn’t require that role.

4.  Enable the Monitor project tasks agentic workflow trigger:

    1.  Select the Describe and connect screen and select **Continue**.
    2.  From the Define trigger screen, select the existing trigger name and turn on the Active toggle on the Edit trigger window, and then select **Continue**.
    3.  In the Select display screen, select **Save and test**.
    The agentic workflow trigger defines the events that invoke AI agents for this agentic workflow. The trigger ensures that the AI agents can only start working upon specific key updates to project tasks.

5.  Navigate to **Workspaces** &gt; **Project Workspace** and select the project.

    The project managers must enable the project email summary skill for a specific project and set up a cadence for the project summary email. For more information on how to set up an email cadence, see the [Schedule the project summary emails with Email project summary skill](email-project-summary-skill-pw.md).

6.  To enable the AI agent for a specific project, you can directly enable the AI agent on the Email project summary modal:

    1.  Navigate to **Workspaces** &gt; **Project Workspace** and open any project.
    2.  From the planning page, select the more actions icon \(![More actions icon.](../../innovation-management/image/more-options-icon.png)\) and then select **Email project summary**.
    3.  From the Email project summary window, select the **Cadence** as Weekly, Bi-weekly, or Monthly according to your requirement.
    4.  Select **On this day**, as days for weekly or bi-weekly or dates for monthly cadence.
    5.  Select **Users** and select the **Include critical path task changes**
    6.  Select **Schedule** or **Schedule and send** to schedule and send the email cadence for the project.
    **Note:** You can select **Schedule** to schedule the project summary email and the project summary is shared as per the selected cadence. You can also choose **Schedule and send** to instantly sent the summary and schedules as per select cadence. For more information, see [Schedule the project summary emails with Email project summary skill](email-project-summary-skill-pw.md).

    The Monitor project tasks agents are enabled for the selected project.


**Related topics**  


[Configuring Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Install Now Assist AI agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Using AI agent agentic workflows in Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-na-spm-ai-agents.md)

[Strategic Portfolio Management AI agents for the monitor project tasks agentic workflow](../concept/na-spm-task-monitoring-usecase.md)

