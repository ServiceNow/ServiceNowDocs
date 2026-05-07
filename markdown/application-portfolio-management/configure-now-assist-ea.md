---
title: Configure Now Assist for Enterprise Architecture \(EA\)
description: If you have the admin role, you can configure the Now Assist for Enterprise Architecture \(EA\) to enable generative AI skills in Enterprise Architecture Workspace \(EA\).
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture]
---

# Configure Now Assist for Enterprise Architecture \(EA\)

If you have the admin role, you can configure the Now Assist for Enterprise Architecture \(EA\) to enable generative AI skills in Enterprise Architecture Workspace \(EA\).

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for EA. While all Now Assist for EA skills are activated by default, you can use this console to activate the plugins in case it’s turned off or configure the generative AI skills. For additional information, see [Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

The following table lists the features and skills that you can access from the Now Assist Admin console.

|EA feature|Skill|
|----------|-----|
|Architectural decision record \(ADR\)|Architectural decision record doc summarization and actions \(Enterprise Architecture Workspace\)|
|Business application|Business application insights \(Enterprise Architecture Workspace\)|
|Enterprise architecture diagrams|Diagram change analysis \(Enterprise Architecture Workspace\)|
|Form fields associated with business applications, business capabilities, business processes, value stream stages, and information objects|Refine text \(Enterprise Architecture Workspace\)|

**Note:** Now LLM Service is the default provider for this Now Assist application's skills.

The Now Assist for Enterprise Architecture \(EA\) system requirements are as follows:

-   Now Assist for Platform \(v7.0.1\)
-   Enterprise Architecture Workspace \(v3.4.0\)

## Procedure

1.  Install the Now Assist for Enterprise Architecture \(EA\) plugin \(sn\_ea\_gen\_ai\).

    -   For information about the application dependencies, see [Supporting information for Now Assist for Enterprise Architecture \(EA\)](../concept/supporting-info-now-assist-ea.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

    If you’re already in the Now Assist Admin console, you can select the **Now Assist Skills** tab on the screen.

3.  Select the expand row icon ![Expand row icon.](../../application-portfolio-management/image/ExpandIcon.png) next to **Technology**.

4.  Select **EA**.

5.  Activate and configure the skill for Now Assist for Enterprise Architecture \(EA\).

<table id="choicetable_wnn_hyf_b2c"><thead><tr><th align="left" id="d33996e339">

Skill

</th><th align="left" id="d33996e342">

Action

</th></tr></thead><tbody><tr><td id="d33996e348">

**ADR Doc Summarization and Actions**

</td><td>

1.  On the **Enterprise Architecture Workspace** skill card, select **View details**.
2.  Select **Activate skill**.
3.  Go to step 6 and review the details.


</td></tr><tr><td id="d33996e379">

**Business application insights**

</td><td>

1.  Select **Activate Skill**.
2.  On the **Choose input** tab, view the table, fields, and related list details that Now Assist leverages to generate business application insights.
3.  On the **Define availability** tab, configure when and under what conditions the skill will be available and select **Save and continue**. The available options are:
    -   **Skill is always available**: Select this option if you want the skill to be available at all times.
    -   **Customize skill availability**: Select this option if you want to define specific conditions for the availability of the skill. For example, you can define whether you want this skill to be available for active business applications.
4.  On the **Define access** tab, verify the roles that have access to the skill.

If you want to provide access to more roles, perform the following:

    1.  Select the edit icon ![](../image/edit-icon.png).
    2.  Verify that your application scope is set to Now Assist for Enterprise Architecture \(EA\). For information on how to change the application scope, see [Select an application from the application picker](https://www.servicenow.com/docs/access?context=t_SelectAnAppFromTheAppPicker&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    3.  Select the user access level, according to your requirement.
        -   **Any authenticated user**: Selecting this option enables any logged-in user to use the skill.
        -   **Select Roles**: Selecting this option enables you to add specific roles in the **Roles** field.
5.  Select **Apply**.

The new role is added to the access list.

**Note:** The **Role restrictions to skill** section displays the roles that have access to the skill, by default.

6.  Select **Activate**.

The Business application insights skill is activated.

 **Note:** An admin user can also define and configure custom parameters for the prompt. To define and configure custom parameters, perform the following:

1.  Select the context menu icon \(![Row context menu icon.](../../application-portfolio-management/image/eaw-image/eaw-icon-menu.png)\) next on the **Business applications insights** card.
2.  Select **Make a copy**.

The You are making a copy of a skill dialog box appears.

3.  Select **Make a copy**.
4.  Perform the following:
    1.  On the **General details** tab, modify the name or description of the skill and select **Save and continue**.
    2.  On the **Choose input** tab, modify the table, fields, and related list details that Now Assist leverages to generate business application insights and select **Save and continue**.
    3.  On the **Define availability** tab, configure when and under what conditions the skill will be available and select **Save and continue**.
    4.  On the **Define access** tab, modify the roles that have access to the skill and select **Save and continue**.
    5.  On the **Select display** tab, enable the **Display** toggle and then elect **Save and continue**.
    6.  On the **Review and activate** tab, review the summary of your choices and select **Activate**.


</td></tr><tr><td id="d33996e593">

**Diagram change analysis**

</td><td>

1.  Select **Activate Skill**.
2.  On the **Turn on Diagram change analysis** page, verify the roles that have access to the skill.
3.  If you want to provide access to more roles, perform the following:

    1.  Select the edit icon ![](../image/edit-icon.png).
    2.  Verify that your application scope is set to Now Assist for Enterprise Architecture \(EA\). For information on how to change the application scope, see [Select an application from the application picker](https://www.servicenow.com/docs/access?context=t_SelectAnAppFromTheAppPicker&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    3.  Select the user access level, according to your requirement.
        -   **Any authenticated user**: Selecting this option enables any logged-in user to use the skill.
        -   **Select Roles**: Selecting this option enables you to add specific roles in the **Roles** field.
4.  Select **Apply**.

The new role is added to the access list.

**Note:** The **Role restrictions to skill** section displays the roles that have access to the skill, by default.

5.  Select **Activate**.

The diagram change analysis skill is activated.

</td></tr><tr><td id="d33996e682">

**Refine text**

</td><td>

1.  Select **Activate Skill**.
2.  Select **Define access** and go to step 6 and review the details.


</td></tr></tbody>
</table>6.  Review the following parameters for the selected skill.

    1.  Review the roles than can access the skill. If necessary, select the edit icon ![](../image/edit-icon.png) if you want to add access to more roles.

        You must verify that your application scope is set to Now Assist for Enterprise Architecture \(EA\). For information on how to change the application scope, see [Select an application from the application picker](https://www.servicenow.com/docs/access?context=t_SelectAnAppFromTheAppPicker&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

        **Note:**

        -   For the ADR doc summarization and actions skill, the sn\_apm.apm\_user and sn\_apm.apm\_read roles are selected by default.

            To learn more about security in Now Assist AI agents with access control lists \(ACLs\), see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

        -   The **Role restrictions to skill** section displays the roles that have access to the skill, by default.
    2.  **Select display**: Review where the skill appears.

        **Note:** When the **In-product desktop** option is selected, the skill is displayed in all EA products.

        Select **Save and continue**.

    3.  **Review and activate**: Review the summary of your choices.
7.  Complete the configuration and activate the skill by selecting **Activate**.

    The skill is configured and activated.


-   **[Now Assist for Enterprise Architecture \(EA\) access roles](../reference/sn-otto-access-roles.md)**  
The following roles help you to configure and use each Now Assist for Enterprise Architecture \(EA\) skill.
-   **[Configure AI Data Explorer and Query Generation skills](configure-ai-data-explr-qry-genr-skills.md)**  
You can configure the AI Data Explorer and Query Generation skills to provide AI-assisted data exploration features and generate insights in Enterprise Architecture Workspace.

**Parent Topic:**[Now Assist for Enterprise Architecture \(EA\)](../concept/now-assist-ea.md)

