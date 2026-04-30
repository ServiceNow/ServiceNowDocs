---
title: Configure a skill in Now Assist for Public Sector Digital Services \(PSDS\)
description: Configure the triggers, settings, and display locations for Now Assist skills to enable GenAI capabilities across the Public Sector Digital Services agent platform.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Configure a skill in Now Assist for Public Sector Digital Services \(PSDS\)

Configure the triggers, settings, and display locations for Now Assist skills to enable GenAI capabilities across the Public Sector Digital Services agent platform.

## About this task

The following skills can be enabled and customized in Now Assist for PSDS:

-   AI Agents
-   Chat Summarization
-   Case Summarization

The Now Assist Admin console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Features** tab of the Now Assist Admin console.

    ![Menu dropdown showing Now Assist Admin](../image/nowassist_psds_admin.png)

2.  Activate and configure the skills for the Now Assist for PSDS.

    The following Now Assist for PSDS skills can be customized:

    -   Case Summarization
    -   Chat Summarization
    These features are grouped under the **Customer** workflow group. Select **PSDS** in the dropdown to access the skills for Now Assist for Public Sector Digital Services \(PSDS\). Each feature has its associated skills.

    ![Menu dropdown showing PSDS in the list of Now Assist Products](../image/now-assist-psds-panel.png)

3.  On the feature card that is associated with the skill that you would like to activate, select **View details**.

    For the Government case summarization skill, select **View details** under the Government case feature card.

    ![Feature card showing option to view skill details](../image/nowassist_psds_viewdetails.png)

4.  In the All available skills section for the desired feature, select **Activate skill**.

5.  Select the inputs or triggers for the selected skill.

    ![Example Define triggers screen for the chat skill.](../image/chat-summ-define-triggers-na-psds.png "Example Define trigger screen for the Chat summarization skill")

6.  After you configure all inputs or triggers for the selected skill, select **Save and continue** to go to the next step.

    You can return to a previous step by using the **Back** button.

7.  Define the availability of the skill.

    **Note:** This step applies to the case summarization and resolution notes generation skill. If you’re configuring the chat summarization skill, you will see the next step as **Choose input**. You can select the customer-facing portals that you want to use as the source of the input data. The default product portal and portals that are already in use by other products can't be selected.

    You can configure the skill to be always available to users, or you can select conditions that must be met before the skill is available. Selecting **Customize skill availability** displays a condition builder.

8.  After you configure the skill availability, select **Save and continue** to go to the next step.

9.  Select where you would like to display the skill.

    -   **In-product**: When selected, the Now Assist skills are displayed on forms and workspaces. For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.
    -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel. If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

        **Note:** Selecting **In-product** will allow the case summarization card to show on the process based experience playbook page in the CSM Configurable Workspace. For Government case summarization, select **In-product**.

10. After you configure the display for the selected skill, select **Save and continue** to go to the next step.

11. Review your choices and select **Activate** to complete the configuration.

    ![Modal showing Activate option for the government case summarization skill](../image/nowassist_psds_activate.png)


## Result

Your skill is configured.

## What to do next

You can go back to the Now Assist Features page to configure another skill.

**Related topics**  


[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

[Install and configure Now Assist for Public Sector Digital Services \(PSDS\)](now-assist-psds-configuring.md)

[Using Now Assist for Public Sector Digital Services \(PSDS\)](now-assist-psds-using.md)

