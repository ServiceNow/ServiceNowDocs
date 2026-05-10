---
title: Customize a Now Assist for IT Service Management \(ITSM\) Incident Summarization skill
description: If you have the admin role, you can customize a Now Assist for IT Service Management \(ITSM\) skill so that agents can use the generative AI skills in Service Operations Workspace for ITSM and in Core UI. Use the Now Assist Skill Kit \(NASK\) to customize your prompts.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Customize a Now Assist for IT Service Management \(ITSM\) Incident Summarization skill

If you have the admin role, you can customize a Now Assist for IT Service Management \(ITSM\) skill so that agents can use the generative AI skills in Service Operations Workspace for ITSM and in Core UI. Use the Now Assist Skill Kit \(NASK\) to customize your prompts.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

You need the sn\_skill\_builder.admin role to customize the prompt in the Now Assist Skill Kit \(NASK\).

## About this task

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin**.

2.  Select the **Now Assist Skills** tab.

3.  In the **Technology** feature group, select **ITSM** from the product list.

4.  Activate and copy the Now Assist for ITSM feature skill for customization.

    1.  On the feature card that is associated with the skill that you would like to activate, select **View details**.

    2.  In the All available skills section, locate the skill that you would like to activate and select **Activate skill**.

        You can choose to make a copy of the skill before activating it.

    3.  Select the more actions icon ![More actions icon.](../../itsm-workspace/image/more-actions-icon.png) for the skill in the Active skills section, and create a copy that you can customize by selecting **Make a copy**.

        The copy that you make is listed in the Active skills section.

    4.  Select the copied skill from the Active skills section to open it.

        A guided setup leads you through the configuration of the general details, input, availability, display, review, and activation of the customized skill.

5.  In the General details step, fill in the fields.

    For information about the inputs and triggers for each skill, see [Skill inputs and triggers for Now Assist for IT Service Management \(ITSM\)](../reference/now-assist-itsm-skills.md).

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

6.  Choose input data.

    The input data is read-only.

    ![Choose input data screen that contains the input tables and fields to define the prompt.](../image/now-assist-itsm-inc-summ-choose-input.png)

    The following table lists the base input table fields and descriptions, including a relevant example.

<table id="table_pxf_tq4_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

For example, `Description`.

 Field in the Incident table, for example, `Description`. The LLM uses the values in this field as one of inputs to generate a response.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Short description of incident, provides quick info about the issue.`

</td></tr></tbody>
</table>    1.  For each input template state \(New, WIP, Resolved, and Closed\), configure the rule conditions by using the condition builder to filter the data further.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        The following table lists the input template states.

        |State|Description|
        |-----|-----------|
        |New|State is New.|
        |WIP|State is Work in Progress.|
        |Resolved|State is Resolved.|
        |Closed|State is Closed.|

    2.  For each input template state \(New, WIP, Resolved, and Closed\), select **+New data source** to configure the additional related table and activity stream data, as needed.

        Adding the input data sources, such as the related tables and activity streams, provide more context to the Now LLM Service in a related list.

        You can also add the rule conditions to these additional related table and activity stream data sources.

        The following table lists the data sources you can add to the input data.

<table id="table_wc1_wt5_dbc"><thead><tr><th>

Data source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Related Table

</td><td>

Fields for a related list:

-   Select related input table
-   Related table field
-   Field description
 Configuring the related table fields follows the same format as the base input table fields in the Choose input step.

</td></tr><tr><td>

Activity: Email

</td><td>

Email that is attached to the incident in the incident summarization.

</td></tr><tr><td>

Activity: Attachment

</td><td>

**Important:** To summarize attachments, make sure that the Incident summarization skill is active.

In the Activity stream:-   You can summarize new attachments of type PNG, JPEG or JPG, PDF, DOCX in the Incident summarization skill record using Document Intelligence.
-   You can also extract the summarized content from the attachment in any of these languages:
    -   English
    -   Dutch
    -   French
    -   German
    -   Portuguese
    -   Spanish
When you use [translate with Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/using-dynamic-translation.md), you can also translate user-generated content live on your instance in additional languages. For more information, see [Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/using-dynamic-translation.md).**Note:**

-   Attachment summaries aren't available in child incident records and are only supported in the English language.
-   If you have one or more existing attachments, you must add new attachments to the incident for the existing attachments to be summarized.


</td></tr></tbody>
</table>    3.  Select **Save and continue** to go to the next step.

7.  Customize the prompt.

    **Important:** You need the sn\_skill\_builder.admin role to activate and customize the prompt in the Now Assist Skill Kit \(NASK\).

<table id="choicetable_ipx_pkr_2hc"><thead><tr><th align="left" id="d440769e568">

To

</th><th align="left" id="d440769e571">

Do this

</th></tr></thead><tbody><tr><td id="d440769e577">

**Evaluate a prompt for each input template**

</td><td>

1.  Select an incident record in any of the incident states such as:
    -   New
    -   Work in progress
    -   Resolved
    -   Closed
2.  Select **Run Test**.![Run test for the selected incident record](../image/now-assist-itsm-evaluate-prompt.png)
Review and test the prompt for each input template configuration and make sure it meets your expectations.The prompt response is shown. You can make changes to the incident state selections and retest as needed.

</td></tr><tr><td id="d440769e616">

**Edit the prompt in the Now Assist Skill Kit and test the prompt**

</td><td>

1.  Select **Edit prompt in Now Assist Skill Kit**.
2.  Select **Go to Now Assist Skill Kit**.![Edit prompts in the Now Assist Skill Kit](../image/now-assist-itsm-edit-prompt-nask.png)

**Note:**

In the Now Assist Skill Kit, you can select the more actions icon ![More actions icon.](../../itsm-workspace/image/more-actions-icon.png)and select **Clone** to make a copy of the prompt configuration and edit as needed.

3.  In the **Skill contents** pane, select the**Inputs** edit icon and add any inputs that you'd like to add to the prompt.![Edit prompt input screen in the Now Assist Skill Kit](../image/now-assist-itsm-edit-skill-input.png)
4.  In the **Prompt** screen, select the edit icon and add the desired inputs to the prompt.![Add inputs for the skill](../image/now-assist-itsm-edit-prompt-window.png)
5.  Select **Run test**.

The prompt displays in the Test prompt screen where you can run the test.

</td></tr></tbody>
</table>8.  In the Now Assist Admin tab, select **Save and continue**.

9.  Define availability.

    Define how the skill will be available to users.

    1.  Configure the skill to be always available to users, or select the conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

    2.  Select **Save and continue** to go to the next step.

10. Select display.

    Configure where to display the incident summarization.

    1.  Select either **In-product**, or **Now Assist panel**.

        -   **In-product**: When selected, Now Assist skills are displayed in all ITSM products \(on forms and in workspaces\).

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

11. Review and activate.

    Review your choices and select **Activate** to complete the skill customization.

    You can now select **Summarize** in an incident and generate the custom incident summary.


