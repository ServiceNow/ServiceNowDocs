---
title: Customize a Now Assist for Security Incident Response skill
description: Customize some of the input fields of a generative AI skill to suit the requirements of your environment.
locale: en-US
release: xanadu
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2025-05-16"
reading_time_minutes: 3
keywords: [Now Assist Security Operations]
breadcrumb: [Configuring Now Assist for Security Incident Response, Now Assist for Security Incident Response, Security Operations]
---

# Customize a Now Assist for Security Incident Response skill

Customize some of the input fields of a generative AI skill to suit the requirements of your environment.

## Before you begin

Roles required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  Select **Security Operations** from the list.

    These Security Incident Response skills are displayed:

    -   Resolution notes generation
    -   Security incident summarization
    -   Security operations metrics analysis

        This skill is activated for use with an AI agent. See [Analyze security operations metrics agentic workflow](assess-metrics-sir-aiagent.md) for more information.

    -   Correlation insights generation
    -   Post incident analysis
    -   Security incident recommended actions

        The AI Search application must be enabled so that the Recommended Actions skill works for security incidents. To verify AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates AI Search is not enabled.

3.  Create a copy of a skill and customize the input fields.

    1.  Select the more actions icon \(![More actions icon.](../../security-incident-response/image/cj-sir-flow-more-icon.png)\) on a card.

    2.  Select **Make a copy**.

    3.  Confirm your choice in the modal.

        The guided setup is displayed.

    4.  In **General details**, enter a unique name and description for the skill.

    5.  Proceed to the next step by selecting **Save and continue**.

    6.  Select **Choose input**.

        **Note:** Some skills do not require all the configuration steps listed below. Select the only tasks that are displayed in the left panel and follow the prompts. After you have completed all the tasks, activate the skill.

        Some, or all of the following input templates for the skill are listed: **Work In Progress**, **Review**, and **Closed**. The **Work In Progress** template is selected.

        You can configure some of the base input table fields, the conditions, and the related lists for the templates. Select only from the related tables supported on the lists for your input data.

        You can’t modify the base input table \[sn\_si\_incident\] or add a new data source for your copy of the security incident summarization skill.

    7.  Continue to modify the editable fields in the templates with filtering conditions.

    8.  Continue to modify the editable fields in the Work In Progress template with the condition builder and filtering conditions.

    9.  Select **Save template** to save your changes to a template.

    10. Proceed to the next step in the Guided Setup for the Work In Progress template by selecting **Save and continue**.

        -   **Customize prompt**: Edit the prompt by reordering or removing the predefined sections. You can review and test the prompt on a security incident record for each input template configuration.
        -   **Define availability**:

<table id="table_jpw_4wj_1cc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skill is always available

</td><td>

The skill is always available to users.

</td></tr><tr><td>

Customize skill availability

</td><td>

The skill is available only when the conditions are met \(Default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>        -   **Select display**:

<table id="table_nmb_b4j_1cc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

In-product desktop

</td><td>

Select the **Display** toggle so that Now Assist skills with this option are displayed on forms and workspaces.

</td></tr><tr><td>

Now Assist panel

</td><td>

Select the **Display** toggle to display the skill in the Now Assist panel. **Note:** If you don't see this option, you must activate the Now Assist panel. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The security incident recommended actions and post-incident analysis skills are not available from the Now Assist panel.

</td></tr></tbody>
</table>    11. Select **Save and continue** to proceed to the next step in the Guided Setup.

    12. Select **Review and Activate** to review your skill and make any additional modifications.

4.  Review your choices and select **Activate** to complete the configuration for the skill.

5.  Select **Select back to skills** to return to the Now Assist skills page.


