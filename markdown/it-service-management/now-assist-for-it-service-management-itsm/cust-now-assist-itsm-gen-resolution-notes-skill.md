---
title: Customize a Now Assist for IT Service Management \(ITSM\) resolution notes generation skill
description: If you have the admin role, you can customize a Now Assist for IT Service Management \(ITSM\) skill so that agents can use the generative AI skills in Service Operations Workspace for ITSM and in Core UI.
locale: en-US
release: yokohama
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Customize a Now Assist for IT Service Management \(ITSM\) resolution notes generation skill

If you have the admin role, you can customize a Now Assist for IT Service Management \(ITSM\) skill so that agents can use the generative AI skills in Service Operations Workspace for ITSM and in Core UI.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

From the Now Assist Admin console, you can select the input tables, related lists, and fields for each input template of the resolution notes generation skill.

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin**.

2.  Select the **Now Assist Skills** tab.

3.  In the **Technology** feature group, select **ITSM** from the product list.

4.  Activate and copy the **Resolution notes generation** skill.

    You can choose to make a copy of the skill before activating it.

    1.  Select the more actions icon ![More actions icon.](../../itsm-workspace/image/more-actions-icon.png) for the skill in the Active skills section, and create a copy that you can customize by selecting **Make a copy**.

        The copy that you make is listed in the Active skills section.

    2.  Select the copied skill from the Active skills section to open it.

        A guided setup leads you through the configuration of enabling user trigger, input, availability, access, display, review, and activation of the skill.

5.  In the **Define trigger** screen, enable the **User triggered** button if user input is required before resolution notes are generated.

    For information about the inputs and triggers for this skill, see [Skill inputs and triggers for Now Assist for IT Service Management \(ITSM\)](../reference/now-assist-itsm-skills.md).

6.  Select **Save and continue**.

7.  Choose input data.

    The skill relies on the Incident input table and following input fields to provide context for the Now LLM Service to generate the resolution notes:

    -   Short description
    -   Description
    -   Work notes
    -   Comments
    The input table and the input fields are read-only.

    ![Choose input data screen for the Generate resolution notes skill that contains the input table and fields to generate the resolution notes.](../image/now-assist-itsm-resolution-notes-gen-input.png)

8.  Select **Save and continue**.

9.  Define availability.

    Define how the skill will be available to users.

    1.  Configure the skill to be always available to users, or select the conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

10. Define access.

    Define the user access and role restrictions that you need for the skill. For information on role restrictions, see [Role masking](../concept/supporting-information-now-assist-itsm.md).

11. Select display.

    Configure where to display the generated resolution notes.

    1.  Select either **In-product**, or **Now Assist panel**.

        -   **In-product**: When selected, Now Assist skills are displayed in all ITSM products \(on forms and in workspaces\).

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

12. Review and activate.

    Review your choices and select **Activate** to complete the skill customization. The popup that shows that the activation was successful appears.

13. Configure the Now Assist context menu \(NACM\) to generate resolution notes and refine the content.

    You can also access the Now Assist context menu by doing the following:

    1.  In the **Now Assist Admin** screen, select **Now Assist Experiences**.
    2.  Select **Now Assist context menu**.
    3.  Select the **Configurations** tab.
    4.  Select **Resolution notes in NACM**.
    5.  Select the more actions icon ![More actions icon.](../../itsm-workspace/image/more-actions-icon.png)and select **Edit configuration**.
    1.  Select **Go to Now Assist context menu**.

        The **Resolution notes in NACM** screen appears.

        **Note:** In the **General details** screen:

        -   The table name is **Incident** by default and is read-only.
        -   The **Form fields** field displays the Now Assist icon \(![](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg)\). The default field that is displayed is **Close notes**. You can change this field based on where you would like to display the Now Assist icon \(![](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg)\).
        ![General details screen in the Resolution notes in NACM screen](../image/now-assist-itsm-res-notes-gen-details.png)

    2.  Select **Save and Continue**.

        The **Configure experience** screen displays.

        **Note:**

        -   The default action for the trigger is set to **Generate resolution notes** and is read-only.
        -   The default refinement actions are **Shorten** and **Elaborate** and are read-only.
        -   The **Insert** action is selected by default.
        When the Now Assist icon \(![](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg)\) is selected in the **Preview** panel, it shows how the generated resolution notes content will display in NACM.

    3.  Select **Save and continue**.

        The **Define access** screen displays.

        **Note:** By default this screen shows that an itil user can access the **Resolution notes in NACM** skill. The role restrictions defined in the **Define access** screen overrides the user access defined in this screen. For information on role restrictions, see [Role masking](../concept/supporting-information-now-assist-itsm.md).

        ![Define access screen in the Resolution notes in NACM screen](../image/now-assist-itsm-res-notes-define-access.png)

    4.  Select **Save and continue**.

        The **Select display** screen displays. The **Display** button is enabled by default and displays the NACM configuration in all ITSM products.

    5.  Select **Save and continue**.

        The **Review and activate** screen displays. In the **Select a record to test configurations** field, select an incident number for which you want to preview the generated resolution notes for the selected incident and select **Preview**. You can preview the generated content in NACM.

    6.  Select **Done**.

        **Important:** For important information, see [Transition to Resolution notes in NACM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).


