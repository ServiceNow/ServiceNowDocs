---
title: Customize a Now Assist for Integrated Risk Management \(IRM\) skill
description: If you have the admin role, you can customize a Now Assist for Integrated Risk Management \(IRM\) skill so that agents can use the generative AI skills in Service Operations Workspace for Now Assist for IRM and in Core UI.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Configure, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Customize a Now Assist for Integrated Risk Management \(IRM\) skill

If you have the admin role, you can customize a Now Assist for Integrated Risk Management \(IRM\) skill so that agents can use the generative AI skills in Service Operations Workspace for Now Assist for IRM and in Core UI.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

From the Now Assist Admin console, you can select the input tables, related lists, and fields for each input template of the incident summarization skill.

## Procedure

1.  Navigate to **Admin** &gt; **Now Assist Admin**.

2.  Select the **Now Assist Skills** tab.

3.  In the **Technology** feature group, select **Risk &amp; Sustainability** from the product list.

4.  Activate and copy the Now Assist for IRM feature skill for customization.

    1.  On the feature card that is associated with the skill that you would like to activate, select **View details**.

    2.  In the All available skills section, locate the skill that you would like to activate and select **Activate skill**.

        You can choose to make a copy of the skill before activating it.

    3.  Select the more actions icon for the skill in the Active skills section, and create a copy that you can customize by selecting **Make a copy**.

        The copy that you make is listed in the Active skills section.

        **Note:** You can only duplicate a summarization skill or the Change risk explanation skill. The fields for the skills that you can’t duplicate have read-only values.

    4.  Select the copied skill from the Active skills section to open it.

        A guided setup leads you through the configuration of the general details, input, availability, display, review, and activation of the customized skill.

5.  In the General details step, fill in the fields.

    1.  Enter a name and description for the skill.

    2.  Select **Save and continue** to go to the next step.

6.  Choose input data.

    Configure the base input table fields and related lists for the different input templates \(New, WIP, Resolved, and Closed states\) for the skill.

    Each skill relies on a base input table and input fields with descriptions to provide context for the Now LLM Service to generate a response.

    Select only those related tables that are offered with the base system as part of the input data.

    1.  For each input template state \(New, WIP, Resolved, and Closed\), select **+New related table field** and configure the base input table fields.

        Add multiple base input fields if more inputs are needed.

        ![Choose input data screen that contains the input tables and fields to define the prompt.](../image/choose-input-data.png)

        The following table lists the base input table fields and descriptions, including a relevant example.

<table id="table_c53_vp5_dbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base input field

</td><td>

Field in the Incident table whose value this skill uses in its response.

 For example, `Short description`.

</td></tr><tr><td>

Field description

</td><td>

Description of the base input field value.

 For example, `Short description of incident, provides quick info about the issue.`

</td></tr></tbody>
</table>    2.  For each input template state \(New, WIP, Resolved, and Closed\), configure the rule conditions by using the condition builder to filter the data further.

        The rule conditions determine when the input template is used. By default, the record state determines the input template that the Now LLM Service uses.

        You can build the condition out further by selecting **+New condition** and configuring additional parameters.

        The following table lists the input template states.

        |State|Description|
        |-----|-----------|
        |New|State is New.|
        |WIP|State is Work in Progress.|
        |Resolved|State is Resolved.|
        |Closed|State is Closed.|

    3.  For each input template state \(New, WIP, Resolved, and Closed\), select **+New data source** to configure the additional related table and activity stream data, as needed.

        Adding the input data sources, such as the related tables and activity streams, provide more context to the Now LLM Service in a related list.

        You can also add the rule conditions to these additional related table and activity stream data sources.

        ![Choose input data screen that contains the input tables and fields to define the prompt.](../image/choosing-input.png)

        The following table lists the data sources that you can add to the input data.

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

Summarizes attachments of type PNG or JPEG in the Incident summarization skill record using Document Intelligence.**Note:** Attachment summaries aren't available in child incident records and are only supported in the English language.

</td></tr></tbody>
</table>    4.  Select **Save and continue** to go to the next step.

7.  Trigger frequency

    Refreshes the sentiments for all updated incidents. You can set the trigger frequency for the refresh using the **Sentiment Analysis Scheduled Job \(Incident\)** scheduled job.

8.  Customize the prompt.

    Review and test the prompt for each input template configuration. You can edit the prompt by adding new predefined sections and ordering the sections as needed.

    1.  For each input template state \(New, WIP, Resolved, and Closed\), select the prompt sections from the list of available sections to include in the generated summary.

        To add a section, you must configure the relevant input data in the Choose input data step before you do this step.

        The available prompt sections that you can select:

        -   **Issue**
        -   **Key Actions Taken**
        -   **Resolution**
        -   **Service Level Agreement**
        -   **Affected CIs and Impacted Services**
        -   **Child Incidents**

            **Note:** When there are too many child incidents and the size of the data goes beyond the LLM token limit, the child incidents section shows the "Too much information and cannot be shown" message.

        The following table lists the mandatory prompt headers.

<table id="table_av3_xhw_2bc"><thead><tr><th>

Input template state

</th><th>

Mandatory prompt header

</th></tr></thead><tbody><tr><td>

New

</td><td>

Issue

</td></tr><tr><td>

Work in progress

</td><td>

-   Issue
-   Key Actions Taken


</td></tr><tr><td>

Resolved

</td><td>

-   Issue
-   Key Actions Taken
-   Resolution


</td></tr><tr><td>

Closed

</td><td>

-   Issue
-   Key Actions Taken
-   Resolution


</td></tr></tbody>
</table>    2.  Select **Save** to continue to the test response.

    3.  Select the incident record in the Test response section, and test the prompt response output format by selecting **Run Test**.

        The prompt response is shown. You can make changes to the incident state selections and retest as needed.

    4.  Select **Edit prompt in Now Assist Skill Kit** to make necessary changes to the prompt in the Now Assist Skill Kit.

    5.  Select **Save and continue** to go to the next step.

9.  Define availability.

    Define how the skill will be available to users.

    1.  Configure the skill to be always available to users, or select the conditions that must be met before the skill is available.

        Selecting **Customize skill availability** displays a condition builder to filter the data further.

        **Note:**

        -   To enable the **Create Knowledge** button to create knowledge articles in any incident state, in the condition builder, select the **\[State\]\[is one of\]\[New, Resolved, In Progress, Closed, Canceled\]** filter condition.
        -   Use the **com.snc.incident.create\_knowledge.multistate.enable** system property to set for which incident states you would want the **Create Knowledge** button to appear. In the value column, enter the corresponding number for the incident state. The incident state numbers are as follows:

            -   1-New
            -   2-In Progress
            -   3-On Hold
            -   6-Resolved
            -   7-Closed
            -   8-Canceled
            You can create a custom state and add a number for that state.

    2.  Select **Save and continue** to go to the next step.

10. Select display.

    Configure where to display the incident summarization.

    1.  Select either **In-product**, or **Now Assist panel**.

        -   **In-product**: When selected, Now Assist skills are displayed in all **Risk &amp; Sustainability** products \(on forms and in workspaces\).

            For the skills that appear in-product, select the down arrow to identify the roles that can use the skill.

        -   **Now Assist panel**: When selected, Now Assist skills are available in the Now Assist panel.

            If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

            For the skills that appear in the Now Assist panel, select the down arrow to identify the roles that can use the skill.

    2.  Select **Save and continue** to go to the next step.

11. Review and activate.

    Review your choices and select **Activate** to complete the skill customization.

    You can now select **Summarize** in an incident and generate the custom incident summary.


