---
title: Customize a Now Assist for IT Service Management \(ITSM\) Incident activity response generation skill
description: If you have the admin role, you can customize a Now Assist for IT Service Management \(ITSM\) skill so that agents can use the generative AI skills in Service Operations Workspace for ITSM and in Core UI.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Customize a Now Assist for IT Service Management \(ITSM\) Incident activity response generation skill

If you have the admin role, you can customize a Now Assist for IT Service Management \(ITSM\) skill so that agents can use the generative AI skills in Service Operations Workspace for ITSM and in Core UI.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin**.

2.  Select the **Now Assist Skills** tab.

3.  In the **Technology** feature group, select **ITSM** from the product list.

4.  Select the **Incident activity response generation** skill and open it.

5.  Choose input data.

    The skill relies on the Incident input table and following input fields to provide context for the Now LLM Service in the incident activity response:

    -   Short description
    -   Description
    -   Priority
    -   State
    -   Work notes
    -   Comments
    The table input table and the input fields are read-only.

    ![Choose input data screen for activity response generation that contains the input table and fields to define the prompt.](../image/now-assist-itsm-activity-resp-gen-input.png)

6.  Define availability.

    Define how the skill will be available to users.

    1.  Configure the skill to be always available to users, or select the conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

7.  Define access.

    Define the user access and role restrictions that you need for the skill. For information on role restrictions, see [Role masking](../concept/supporting-information-now-assist-itsm.md).

8.  Select display.

    1.  Enable the In-product display so that the Now Assist skills are displayed in all ITSM products \(on forms and in workspaces\).

        For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

9.  Review and activate.

    Review your choices and select **Activate** to complete the skill customization. The popup that shows that the activation was successful appears.

10. Configure the Now Assist context menu \(NACM\) to generate an activity response and refine the content.

    You can also access the Now Assist context menu by doing the following:

    1.  In the **Now Assist Admin** screen, select **Now Assist Experiences**.
    2.  Select **Now Assist context menu**.
    3.  Select the **Configurations** tab.
    4.  Select **Incident activity response in NACM**.
    1.  Select **Go to Now Assist context menu**.

        The **Incident activity response in NACM** screen appears.

        **Note:** In the **General details** screen:

        -   The table name is **Incident** by default and is read-only.
        -   You can configure the skill to generate a response for any of these options shown in the table below in the work notes and comments in the incident's activity stream.
        |Options|Description|
        |-------|-----------|
        |Acknowledge task|Acknowledge the receipt of the task record.|
        |Post response|Generate a reply for specific questions from the user.|
        |Summarize actions taken|Generate a summary of all actions taken.|
        |Follow up|Ask follow-up questions.|

    2.  Select **Save and Continue**.

        The **Configure experience** screen displays.

        **Note:**

        -   The default trigger actions are as follows:
            -   For Work notes, the actions are Summarize actions, and Post response.
            -   For Additional comments, the actions are Follow up, Post response, and Acknowledge task.
        -   The **Insert** action is selected by default.
        When you select the Now Assist icon in the **Preview** panel, it shows how the generated activity response will display in NACM.

    3.  Select **Save and continue**.

        The **Define access** screen displays.

        **Note:** By default this screen shows that an itil user can access the **Incident activity response in NACM** skill. The role restrictions defined in the **Define access** screen overrides the user access defined in this screen. For information on role restrictions, see [Role masking](../concept/supporting-information-now-assist-itsm.md).

        ![Define access screen in the Incident activity response in NACM screen](../image/now-assist-itsm-act-resp-define-access.png)

    4.  Select **Save and continue**.

        The **Select display** screen displays. The **Display** button is enabled by default and displays the NACM configuration in all ITSM products.

    5.  Select **Save and continue**.

        The **Review and activate** screen displays. In the **Select a record to test configurations** field, select an incident number for which you want to preview the activity response generated for the selected incident and select **Preview**. You can preview the generated content in NACM.

    6.  Select **Done**.


