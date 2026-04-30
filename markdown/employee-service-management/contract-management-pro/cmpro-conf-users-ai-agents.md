---
title: Configuring user access and data permissions for AI agents
description: Configure the security controls to specify the users who can discover or use the agentic workflow, and provide data permissions for AI agents.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-11-20"
reading_time_minutes: 1
breadcrumb: [Configure agentic workflows, Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Configuring user access and data permissions for AI agents

Configure the security controls to specify the users who can discover or use the agentic workflow, and provide data permissions for AI agents.

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of AI agents during tool execution. AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

In Now Assist in Contract Management, the following roles are configured with the base system to provide data access to the AI agents in the agentic workflows of Contract Management Pro.

-   sn\_cm\_gen\_ai.ai\_contract\_fulfiller
-   sn\_lg\_cnt.contract\_fulfiller
-   sn\_lg\_ops.request\_fulfiller
-   sn\_cm\_core.contract\_fulfiller
-   contract\_manager
-   sn\_lg\_cnt.contract\_owner
-   sn\_cm\_obligation.obligation\_fulfiller

To ensure that the AI agent can access all the required information for your workspace, add the necessary roles for the AI agent in the AI Agent Studio.

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **.**
2.  Select the **AI agents** tab.
3.  Open the AI agent for which you want to configure the security controls.
4.  In the guided setup, navigate to **Define security controls** to define the security access.
    1.  In the **Define user access** tab, add the user roles who can discover or invoke the AI agent.
    2.  In the **Define data access** tab, add the user roles to define which roles the AI agent uses to access data during its execution.

        This configuration controls what information the AI agent can read, update, or share, based on the permissions of the selected roles.


For more information on configuring the security controls, see [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Configuring agentic workflows in Now Assist in Contract Management](cmpro-conf-agentic-workflow.md)

**Related topics**  


[Configuring user access and data permissions for agentic workflows](cmpro-conf-users-agentic-wf.md)

