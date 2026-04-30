---
title: Configure Now Assist for Customer Service Management \(CSM\)
description: If you have the admin role, you can configure the Now Assist for Customer Service Management \(CSM\) application so that your agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.
locale: en-US
release: xanadu
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Configure Now Assist for Customer Service Management \(CSM\)

If you have the admin role, you can configure the Now Assist for Customer Service Management \(CSM\) application so that your agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for CSM. This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

<table id="table_ipf_bbd_wyb"><thead><tr><th>

CSM features

</th><th>

Skills

</th></tr></thead><tbody><tr><td>

Chat

</td><td>

-   Chat summarization
-   Chat recommendation
-   Sidebar recommendation

</td></tr><tr><td>

Case

</td><td>

-   Case summarization
-   Resolution notes generation
-   Email response
-   Suggested steps generation
-   Sentiment analysis

</td></tr><tr><td>

Knowledge

</td><td>

KB generation

</td></tr><tr><td>

Call

</td><td>

Call summarization

</td></tr></tbody>
</table>**Note:**

-   Now LLM Service is currently the only provider for this Now Assist application's skills.

-   The minimum version of the workspace required to support Now Assist for CSM features:
    -   CSM and FSM Configurable Workspace Foundation \(sn\_cwf\_wrkspc\): 24.2.1.

    -   CSM Configurable Workspace \(sn\_csm\_wrkspc\): 24.2.0.


For earlier versions, go to [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) to upgrade it to a later version.

## Procedure

1.  Install the Now Assist for CSM plugin \(sn\_csm\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Application information](now-assist-csm-supporting-info.md#section_j5w_3dz_byb).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
    -   For information about the CSM Configurable Workspace, see [Set up CSM Configurable Workspace](csm-config-workspace-set-up.md).
    -   For information about Now Assist AI agents, see [Install Now Assist AI Agents](https://www.servicenow.com/docs/access?context=install-ai-agents-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). To access AI agents in the Now Assist panel, you need to [turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) and ensure that the case summarization is active on the instance.
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills** to access the **Skills** tab of the Now Assist Admin console.

3.  Activate and configure the skills for the Now Assist for CSM features.

    These features are grouped under the **Customer** workflow group. Each feature has its associated skills.

4.  On the tile for your skills, select **Activate skill**.

5.  Select the inputs or triggers for the selected skill.

    For information about the inputs and triggers for each skill, see [Skill inputs and triggers for Now Assist for Customer Service Management \(CSM\)](now-assist-csm-skill-inputs.md).

    ![Define triggers screen for the chat skill.](../image/now-assist-csm-define-trigger.png "Example Define trigger screen for the Chat summarization skill")

6.  After you configure the inputs or triggers for the selected skill, select **Save and continue** to go to the next step.

    -   You can return to a previous step by using the **Back** button.
    -   Choose output is available as an additional step in the guided flow for the admin to select the output field where they want to enable Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) and generate resolution notes. All the multi-line text field will be automatically available in the drop down list to select. If a customer has set a custom field for resolution notes, it can also be selected from the drop down.

        By default, we see the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) in the resolution notes field. When we select another field, for example description, the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) will show here automatically. The resolution notes can be generated in the description field.

7.  Define the availability of the skill.

    You can configure the skill to be always available to users or you can select conditions that must be met before the skill is available. Selecting **Customize skill availability** displays a condition builder.

    **Note:**

    -   This step applies to the case summarization, resolution notes generation, chat summarization, KB generation, chat reply recommendation, and email response skill.
    -   If you’re configuring the chat summarization, chat recommendation sentiment analysis or suggested steps generation skill, you will see the next step as **Choose input**. You can select the customer-facing portals that you want to use as the source of the input data. The default product portal and portals that are already in use by other products can't be selected.
    -   For suggested step generation skill, the next step after choose input is to launch record clustering to generate more relevant suggested steps based on similar cases.

        **Important:** This process might take several hours. While record clustering is in progress, you won't be able to progress to the next page of the setup. You will be notified by email when it is complete. When the clustering process is complete, you can explore the clusters in more details, monitor the re-clustered schedule or regenerate clusters.

    ![Choose input screen for the Chat summarization skill.](../image/now-assist-csm-choose-input-chat-summary.jpg "Example Choose input screen for the Chat summarization skill")

8.  After you configure the skill availability, select **Save and continue** to go to the next step.

9.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_esm\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

10. Select where you would like to display the skill.

    -   **In-product**: When selected, the Now Assist skills are displayed on forms and workspaces.

        For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

        For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

11. After you configure the display for the selected skill, select **Save and continue** to go to the next step.

12. Review your choices and select **Activate** to complete the configuration.

    Your skill is configured.

13. Configure the Now Assist for CSM Propose Solution UI action and declarative action.

    The Propose Solution UI action and declarative action that are included with the Now Assist for CSM application provide generative AI-specific functionality to the Case form. An agent can use these actions to propose solutions that include the AI-generated resolution notes.

    For more information, see [Configure the Propose Solution UI action and declarative action](../task/now-assist-csm-config-propose-solution.md).

    **Note:** You can skip this step if you are using the Now Assist Content menu experience for Resolution Notes Generation skill.

14. Set the **CSM default record page** and **CSM Interaction record page** as the default pages in UI Builder.

    A record page provides the base structure for how a record is displayed in CSM Configurable Workspace. When the system displays information in CSM Configurable Workspace, such as the case records and interactions, it uses the pages that have been set as the default record pages.

    Setting these record pages as the default pages also enables the generative AI icon and banner in CSM Configurable Workspace.

    Setting a page as the default page includes activating the page and setting the order value. For more information, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).


**Related topics**  


[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Configuring Now Assist settings and features](https://www.servicenow.com/docs/access?context=configuring-na-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Record summarization](https://www.servicenow.com/docs/access?context=now-assist-case-summary&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Chat summarization](https://www.servicenow.com/docs/access?context=now-assist-chat-summary&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Using agentic workflows in Now Assist for Customer Service Management \(CSM\)](csm-ai-agents-use-cases.md)

[Customer Service Management AI agent collection triage cases agentic workflow](case-resolving-use-case.md)

