---
title: Customize a Now Assist for Security Incident Response skill
description: Customize some of the input fields of a generative AI skill to suit the requirements of your environment.
locale: en-US
release: zurich
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Now Assist Security Operations]
breadcrumb: [Configure, Now Assist for Security Incident Response, Security Operations]
---

# Customize a Now Assist for Security Incident Response skill

Customize some of the input fields of a generative AI skill to suit the requirements of your environment.

## Before you begin

Roles required: sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  Select **Technology** &gt; **Security Operations**.

    These Security Incident Response skills are displayed:

    -   Security incident recommended actions

        The AI Search application must be enabled so that the Recommended Actions skill works for security incidents. To verify AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates AI Search is not enabled.

    -   Post incident analysis
    -   Security operations metrics analysis

        This skill is activated for use with an AI agent. See [Analyze security operations metrics agentic workflow](assess-metrics-sir-aiagent.md) for more information.

    -   Correlation insights generation
    -   Security incident summarization
    -   Resolution notes generation
    -   Security operations metrics analysis
    -   Generate content for shift handover
    -   Security Incident Quality Assessment
3.  Create a copy of a skill and customize the input fields.

    1.  Select **![More actions icon.](../../security-incident-response/image/cj-sir-flow-more-icon.png)** &gt; **Make a copy**.

    2.  Confirm your choice in the modal.

        The guided setup is displayed.

    3.  In **General details**, enter a unique name and description for the skill.

    4.  Proceed to the next step by selecting **Save and continue**.

    5.  Select **Choose input**.

        **Note:** Some skills do not require all the configuration steps listed below. Select the only tasks that are displayed in the left panel and follow the prompts. After you have completed all the tasks, activate the skill.

        If **Choose input** is selected, these input templates for the skill are listed: Work In Progress, Review, and Closed. The Work In Progress template is selected.

        You can configure some of the base input table fields, the conditions, and the related lists for the templates. Select only from the related tables supported on the lists for your input data.

        You can’t modify the base input table \[sn\_si\_incident\] or add a new data source for your copy of the security incident summarization skill.

    6.  Continue to modify the editable fields in the Work In Progress template with the condition builder and filtering conditions.

    7.  Select **Save template** to save your changes to a template.

    8.  Proceed to the next step in the Guided Setup for the Work In Progress template by selecting **Save and continue**.

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

In-product

</td><td>

Show security incident summarization in all Security products. Now Assist skills are displayed on forms and workspaces.

</td></tr><tr><td>

User roles

</td><td>

Select the expand icon \(![Expand icon.](../image/icon-expand.png)\)

</td></tr><tr><td>

Now Assist panel

</td><td>

Now Assist skills are available in the Now Assist panel. **Note:** If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

Conversational experiences

</td><td>

Verify where the skill is displayed and add roles for who can view it.Select **Now Assist Panel** in the Conversational experiences field to display the skill in the Now Assist panel.

</td></tr></tbody>
</table>    9.  Select **Save template** to save your changes to the Work In Progress template.

    10. Select the Review template.

    11. Continue to modify the editable fields in the Review and Closed templates with filtering conditions as described in the previous steps.

    12. Select **Save and continue** to proceed to the next step in the Guided Setup.

    13. Select **Save template** to save your changes to a template.

    14. Select **Review and Activate** to review your skill and make any additional modifications.

4.  Select **Activate**.

    Your skill is displayed on the Security Incident page in the All available Security Incident skills section.

5.  Select **Activate skill**.


