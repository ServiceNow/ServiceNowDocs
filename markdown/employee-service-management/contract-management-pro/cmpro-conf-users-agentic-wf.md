---
title: Configuring user access and data permissions for agentic workflows
description: Configure the security controls to specify the users who can discover or use the agentic workflow, and provide data permissions for the agentic workflow.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Configure agentic workflows, Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Configuring user access and data permissions for agentic workflows

Configure the security controls to specify the users who can discover or use the agentic workflow, and provide data permissions for the agentic workflow.

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

In Now Assist in Contract Management, the following roles are configured with the base system to provide data access to the agentic workflows in Contract Management Pro.

-   sn\_cm\_gen\_ai.ai\_contract\_fulfiller
-   sn\_lg\_cnt.contract\_fulfiller
-   sn\_lg\_ops.request\_fulfiller
-   sn\_cm\_core.contract\_fulfiller
-   contract\_manager
-   sn\_lg\_cnt.contract\_owner
-   sn\_cm\_obligation.obligation\_fulfiller

To ensure that the agentic workflow can access all the required information for your workspace, add the necessary roles for the agentic workflow in the AI Agent Studio.

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **.**
2.  Select the **Agentic workflows** tab.
3.  Open the agentic workflow for which you want to configure the security controls.
4.  In the guided setup, navigate to **Define security controls** to define the security access.
    1.  In the **Define user access** tab, add the user roles who can discover or invoke the agentic workflow.
    2.  In the **Define data access** tab, add the user roles to define which roles the agentic workflow uses to access data during its execution.

        This configuration controls what information the agentic workflow can read, update, or share, based on the permissions of the selected roles.


For more information on configuring the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Configuring agentic workflows in Now Assist in Contract Management](cmpro-conf-agentic-workflow.md)

**Related topics**  


[Configuring user access and data permissions for AI agents](cmpro-conf-users-ai-agents.md)

