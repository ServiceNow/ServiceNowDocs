---
title: Create Smart Assessment templates for BIA
description: Create Smart Assessment templates in the Assessment Workspace for the Business Impact Analysis \(BIA\) workflow.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Setup for a BIA, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create Smart Assessment templates for BIA

Create Smart Assessment templates in the Assessment Workspace for the Business Impact Analysis \(BIA\) workflow.

## Before you begin

Role required: sn\_bcm.admin

## About this task

**Note:** The flows shown in the examples are demo flows. You can configure the flows according to your requirements.

## Required and optional apps

The store apps for using the Smart Assessment Engine application in BIA are listed.

1.  Required apps: Smart Assessment Core \[com.sn\_smart\_asmt\], Smart Assessment Designer \[com.sn\_smart\_asmt\_desg\], Smart Assessment Connected \[com.sn\_smart\_asmt\_conn\]
2.  Optional apps: Smart Assessment Post-assessment Actions \[com.sn\_smart\_imp\_auto\]

For information about the initial setup checklist for Smart Assessment Engine, see [Configuring Smart Assessment Engine](../../assessment-engine/concept/smart-assessment-engine-cf-config.md). For more information on the Smart Assessment Engine, see [Smart Assessment Engine](../../assessment-engine/reference/smart-asmnt-engine-landing-page.md).

## About this task

To configure a BIA template using Smart Assessment, see [Configure BIA templates with Smart Assessment](conf-bia-temp-smart-asmt-type.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** and select **New template**.

    You can create assessment templates to manage your assessments in the Assessment Workspace. The example shows demo data in an instance.

    ![Assessment Workspace.](../image/asmt-workspace.png)

    The Create assessment template form is displayed.

    ![Create assessment template form.](../image/create-asmt-template.png)

2.  In the Create assessment template form, fill in the fields and select **Create**.

    |Field|Description|
    |-----|-----------|
    |Template name|Unique meaningful name for the template. For example, BIA template using Smart Assessment.|
    |Description|Brief explanation of purpose.|
    |Purpose|Intended use of the template. For example, Business impact assessment.|
    |Assessment target|Table records that are used for the assessment. For example, Impact analysis.|

    The newly created BIA template is displayed in the Assessment templates list as shown in the example.

    ![BIA template.](../image/bia-asmt-templates-list.png)

    When you select the template, the **General** and **Questions** tabs are displayed, enabling you to add instructions, questions, response guidance, and sections that group related questions. You can verify the template details displayed in the **Details** section of the **General** tab.

    -   Verify that the assessment template category selected in the Details section of the **General** tab is **Business impact assessment** as shown in the example. The Business impact assessment template category is associated with the sn\_bcm.core\_viewer role. Users with the sn\_bcm.core\_viewer role can view these templates in read-only mode.
    -   The assessment target in the **Assessment targets** field is set to **Impact analysis** only.
    -   Assessment reader role: Assign read-only access to users with the specified role.
    ![State.](../image/temp-published-state.png)

3.  Add the assessment duration in days and assign a role in the **Assessment reader** role field in the Settings section, then select **Save**.

    The Assessment reader role option in the Smart Assessment template enables designated users to view assessments in read-only mode without being the assessor. For BIAs, BCM administrators assign the BCM Core viewer \[sn\_bcm.core\_viewer\] role as the Assessment reader role to maintain the same functionality as the legacy assessment.

    ![Core viewer role.](../image/asmt-template-bcm-core-viewer-role.png)

    **Note:** For information on creating an assessment template, see [Create an assessment template](../../assessment-engine/task/sae-asmnt-template-create.md).

4.  Set up the assessment questions in the **Questions** tab.

    1.  Select **+Add section** to organize related questions, then select **Save**.

        A sample section is shown in the example.

        ![Sample question.](../image/bia-questions-tab.png)

    2.  Select **+Add question**, add questions marking them as required or optional and select the type of the answer.

        The example shows modals with different options.

        ![Modal.](../image/bia-given-questions-tab.png)![Example.](../image/bia-questions-tab-format.png)![Questions.](../image/asmt-temp-questions-tab.png)

    3.  To add reference data for the assessment, select **Add assessment reference**, choose the desired columns, and select **Add**.

        These cards are displayed on the side panel to add information about the assessment targets.

    4.  Add instructions in the text box to set the context and inform responders on how to answer the questions appropriately.

    For information on adding instructions and questions to the assessment template, see [Add instructions and questions to an assessment template](../../assessment-engine/task/sae-asmnt-template-populate.md).

5.  Select **Save**.

6.  To publish the template, select **Publish**.

    A message is displayed that the assessment template is published and you can use it to send assessments.

7.  Configure response-based automation and corresponding actions by creating automation rules in the **Automations** tab of the published template.

    Automation reduces manual data entry. The system analyzes responses and automatically populates RPO and RTO fields in your impact analysis records.

    1.  Select **+ Create automation**, add the name and description for the rule, and select **Create**.

        The automation is created in the Draft state.

    2.  Define rules that automatically trigger actions based on user responses in the "If" block.

        The Action set consists of an "If" block and a "Then" block. The "If" block sets conditions that trigger automation. The "Then" block defines the actions that execute automatically when those conditions are met.

        ![RPO.](../image/automations-tab-rpo.png)

    3.  Set an action in the "Then" block that is triggered automatically based on user responses.

        The system reviews user responses and suggests actions and the corresponding timeframes. For example, if data change frequency = "High", the system suggests a recovery timeframe = "Immediately" as shown in the example.

        ![Actions.](../image/automations-tab-set-actions.png)

        For the automation setup, two subflows are provided in the Workflow Studio as part of demo data.

        ![Flows.](../image/bia-flows-in-flow-designer.png)![RPO flow.](../image/bia-rpo-flow.png)

        In the properties of the subflow, the **Category** field is set to **Business impact assessment**. When the action category and the template category are mapped in the BIA as shown in the example, the **Set recovery point objective flow** is displayed in the **Action type** field in the Set actions dialog box.

        ![Mapping.](../image/mapping-of-action-and-template-category.png)![Actions.](../image/automations-tab-set-actions.png)

    4.  To activate the automation, select **Activate** in the **Automations** tab, confirm the details in the Activate dialog box, and select **Activate** again.

        Once activated, the automation appears in the **Automations** tab.

        For more information on automations, see [Automate response](../../assessment-engine/concept/automate-response.md) and [Configure post-assessment actions](../../assessment-engine/task/configure-post-assessment-actions.md).

8.  Configure scoring settings on the **Scoring** tab.

    For more information on assigning scores to the assessments, see [Scoring assessments](../../assessment-engine/concept/scoring-in-assessments.md).

9.  Select **Save**.

10. To copy a published template, select **Copy template**, update the fields, and save your changes.

11. To publish the assessment template, select **Publish**.

    A message confirms that the assessment template is published and ready to use.

    1.  To proceed, select **OK**.

    2.  To return to the template list on the Assessment Workspace landing page, select **Return to template list**.


## Result

You can use the published Smart Assessment template for the Business Impact Analysis \(BIA\) workflow.

**Parent Topic:**[Setup for a business impact analysis](../concept/bcm-admin-tasks.md)

