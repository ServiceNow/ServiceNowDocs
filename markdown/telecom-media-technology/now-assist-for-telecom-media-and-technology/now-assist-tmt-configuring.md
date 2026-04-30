---
title: Configuring Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Configure the Now Assist for Telecommunications, Media and Technology \(TMT\) application so that your agents can use the generative AI skills in the CSM/FSM Configurable Workspace and in Core UI.
locale: en-US
release: yokohama
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Now Assist for Telecommunications, Media and Technology \(TMT\), Telecommunications, Media, and Technology]
---

# Configuring Now Assist for Telecommunications, Media and Technology \(TMT\)

Configure the Now Assist for Telecommunications, Media and Technology \(TMT\) application so that your agents can use the generative AI skills in the CSM/FSM Configurable Workspace and in Core UI.

## Before you begin

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for TMT. For information needed to install the Now Assist plugins and configure generative AI skills, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

<table id="table_vy3_nbk_5bc"><thead><tr><th>

TMT features

</th><th>

Skills

</th></tr></thead><tbody><tr><td>

Service Problem Case

</td><td>

-   Case summarization
-   Resolution notes generation
-   Test summarization
-   Knowledge generation
-   Customer service summary

</td></tr><tr><td>

Customer Success Management

</td><td>

-   Account onboarding case summarization
-   Engagement summarization
-   Touchpoint summarization
-   Customer play summarization
-   Internal play summarization
-   Success initiative summarization
-   Analyze metric trend
-   Risk signal and issues summarization

</td></tr><tr><td>

Service Exchange

</td><td>

Transform mapping

</td></tr></tbody>
</table>**Note:** The ServiceNow® large language model \(Now LLM Service\) is currently the only provider for this Now Assist application's skills.

## Procedure

1.  Install the Now Assist for Telecommunications, Media and Technology \(TMT\) plugin \(sn\_tmt\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Application information](../concept/now-assist-tmt-supporting-info.md).
    -   For information about the installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

    If you’re already in the Now Assist Admin console, you can select the **Now Assist Skills** tab on the screen.

3.  Activate and configure the skills for the Now Assist for TMT features.

    These features are grouped under the Customer workflow group. Each feature has its associated skills.

4.  Select **TMT** under the **Customer** workflow group.

5.  On the Now Assist skills for TMT page, select **Activate skill** for the skill that you would like to activate.

    The page for the skill that you activated opens with the General details section highlighted.

6.  Review the inputs for the selected skill.

    The input table fields are read-only. For information about the inputs and triggers for each skill, see [Skill inputs for Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-skill-inputs.md).

7.  After reviewing the inputs for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

8.  In the Define availability section, choose one of the following:

    -   To enable the skill everywhere it is available, select **Skill is always available**.
    -   To manually set the conditions for when the skill is available, select **Customize skill availability**.
9.  After you configure the skill availability, select **Save and continue** to go to the next step.

10. Select where you would like to display the skill.

    -   To display the skill on the Mobile Agent app, select **In-product**.
    -   To display the skill in the Now Assist panel, select **Now Assist panel**.

        For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

11. After you configure the display for the selected skill, select **Save and continue** to go to the next step.

12. Review your choices and select **Activate** to complete the configuration.


## Result

Your skill is configured.

