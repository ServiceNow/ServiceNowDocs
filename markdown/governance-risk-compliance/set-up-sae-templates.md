---
title: Set up DRI Smart Assessment templates
description: Set up the Smart Assessment templates in the Assessment Workspace. You can then use them to set up the action task configuration templates in the Regulatory Agency Profile for Digital resilience incident reporting.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Set up DRI Smart Assessment templates

Set up the Smart Assessment templates in the Assessment Workspace. You can then use them to set up the action task configuration templates in the Regulatory Agency Profile for Digital resilience incident reporting.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_dri\_inc\_rptg.digital\_resilience\_incident\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** to access the Assessment Workspace landing page.

2.  Select **New template** in the Assessment Workspace.

    You can create assessment templates in the Assessment Workspace to manage your assessments. The example shows the assessment templates included in the demo data.

    ![Demo data in the Assessment Workspace.](../image/dri-temp-sae.png)

    When you select **New template**, the Create assessment template form, **General** tab, and **Questions** tab are displayed.

3.  Fill in the fields in the Create assessment template form and select **Create**.

    The example shows the Create assessment template form.

    ![Create assessment template form.](../image/dri-create-asmt-template.png)

    |Field|Description|
    |-----|-----------|
    |Template name|Unique meaningful name for the template, for example, DRI initial report template.|
    |Assessment name|Name for the assessment.|
    |Description|Description of the template such as why it is used. For example, Regulatory reporting assessment of IT incidents.|
    |Purpose|Purpose or intended use of the template, such as, DRI template category.|
    |Assessment target|Table records that are used for the assessment. For example, Digital Resilience Incident Reporting Case, Action task.|

    For more information on creating templates, see [Create an assessment template](../../assessment-engine/task/sae-asmnt-template-create.md).

    The assessment template is created and displayed in the Details section of the **General** tab as shown in the example.

    ![Assessment template created.](../image/dri-sample-reporting-template-in-asmt-ws-details-section.png)

    You can now fill in the template with instructions, questions, and optional guidance for responding to a question, and sections that group the related questions. For more information on creating an assessment template, see [Create an assessment template](../../assessment-engine/task/sae-asmnt-template-create.md).

4.  Set up the assessment questions in the **Questions** tab.

    For information on adding instructions and questions to the assessment template, see [Add instructions and questions to an assessment template](../../assessment-engine/task/sae-asmnt-template-populate.md).

    The example shows how to set up the assessment questions.

    ![Example showing questions displayed in an assessment.](../image/asmt-temp-questions-tab.png)

    The example shows how questions are configured in the **Questions** tab.

    ![Questions tab configuration.](../image/dri-questions-asmt-ws.png)

5.  Select **Save**.

6.  To publish the template, select **Publish**.

    A message is displayed that the assessment template is published and you can use it to send assessments.

7.  Configure response-based automation and corresponding actions by creating automation rules in the **Automations** tab of the published template.

    Automation streamlines the assessment workflow by eliminating repetitive manual tasks, enabling assessors to focus on analysis rather than data entry. Pre-configured responses verify consistency and accuracy across assessments while significantly reducing completion time.

    The example shows an active automation named "Classify the incidents as Reportable or Not Reportable to the regulatory authorities" that automatically classifies incidents based on regulatory reporting requirements.

    **Note:** You can edit an existing automation only if you have access to it and the corresponding DRI template is published. Otherwise, the automation is available as read-only.

    ![Example showing the Automations tab.](../image/dri-regu-report-asmt-automations-tab.png)

    Follow these steps to add automations to your assessment template.

    1.  Select **+ Create automation**, add the name and description for the rule, and select **Create**.

        The example shows the Create automation modal where you can add the name and description of the automation rule.

        ![Example showing how to create automations.](../image/dri-regu-report-asmt-automations-tab-create-auto.png)

        The automation is created in the Draft state.

        ![Automation rule created in the draft state.](../image/dri-auto-created.png)

        The Action set in this example consists of an "If" block and a "Then" block. The "If" block sets conditions that trigger automation. The "Then" block defines the actions that execute automatically when those conditions are met.

    2.  Select **Set condition** in the "If" block.

    3.  To add a condition, select **+ New condition set** in the Set conditions dialog box and select **Save**.

        The example shows how you can add one or more conditions to automate actions based on user responses.

        ![Example showing to set conditions based on responses.](../image/dri-regu-report-asmt-automations-tab-set-condi-2.png)

        The conditional action set is saved and the automation conditions are now configured.

    4.  To set an automated action for a specified condition, select **Open** in the "Then" block, choose the action and the DRI record, then select **Close**.

        In this example, "DRI regulatory reporting status change" is the action that triggers automatically when the conditions in the "If" block are met. The associated DRI record is selected to complete the action setup.

        ![Example showing that conditions are set and how to set action type.](../image/dri-regu-report-asmt-automations-tab-set-condi-4.png)

    5.  To activate the automation, select **Activate** in the **Automations** tab, confirm the details in the Activate dialog box, and select **Activate** again.

        The Activate dialog box is shown in the example.

        ![Example showing the dialog box to activate the automation.](../image/dri-auto-activate-dialog-box.png)

        Once activated, the automation appears in the **Automations** tab.

        ![Activated automation displayed in the list on the Automations tab.](../image/dri-automation-activated.png)

        For more information on automations, see [Automate response](../../assessment-engine/concept/automate-response.md) and [Configure post-assessment actions](../../assessment-engine/task/configure-post-assessment-actions.md).

8.  Configure scoring settings on the **Scoring** tab.

    For more information on assigning scores to the assessments, see [Scoring assessments](../../assessment-engine/concept/scoring-in-assessments.md). For more information on the Smart Assessment Engine, see [Smart Assessment Engine](../../assessment-engine/reference/smart-asmnt-engine-landing-page.md).

9.  Select **Save**.

10. To copy a published template, select **Copy template**, update the fields, and save your changes.

11. To edit a published template, verify you have the required roles, select **Edit**, update the fields, and save your changes.

    **Note:** Templates that are associated with assessments cannot be moved to Draft status.

12. To publish the assessment template, select **Publish**.

    A message confirms that the assessment template is published and ready to use.

    1.  To proceed, select **OK**.

    2.  To return to the template list on the landing page, select **Return to template list**.

    The assessment template is now published and available in the Digital resilience incident reporting module.

    The examples display pre-configured DRI templates for DORA regulation.

    ![DRI template 1.](../image/dri-temp-sae-1.png)![DRI template 2.](../image/dri-temp-sae-2.png)![DRI template 3.](../image/dri-temp-sae-3.png)![DRI template 4.](../image/dri-temp-sae-4.png)

    The Smart Assessment templates for the action tasks are created and saved in the instance.

    The following example shows the demo data for action task configurations in the Regulatory agency profile.

    ![Demo data for the action task configurations. For the text description, refer to the text that precedes this image.](../image/action-task-config-dora-conditions.png)

    **Note:** After setting up Smart Assessment templates in the Assessment Workspace, you can use them to configure action task templates in the Regulatory Agency Profile table.

    For more information on setting up action task templates, see the [Set up action task templates in Regulatory agency profile](set-up-action-task-templates.md) section.


