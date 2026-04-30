---
title: Create a Smart Assessment template
description: Create a Smart Assessment template and impact automation that can be used in the vulnerability types of an operational vulnerability.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Completing general administrative tasks, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Create a Smart Assessment template

Create a Smart Assessment template and impact automation that can be used in the vulnerability types of an operational vulnerability.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

Operational Resilience administrators contain the flow\_designer role, enabling them to update automation flows as needed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** or navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Template Categories**.

2.  Select **New template**.

    You can create assessment templates to manage your assessments in the Assessment Workspace. The following example shows demo data in an instance.

    ![Assessment Workspace.](../../grc-business-continuity-management/image/asmt-workspace.png)

    When you select **New template**, the **General** and **Questions** tabs are displayed.

3.  In the Create assessment template form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Template name|Unique meaningful name for the template, for example, BIA template using Smart Assessment.|
    |Description|Description of the template such as why it is being used.|
    |Purpose|Purpose or intended use of the template, such as, Self attestation assessment.|
    |Assessment target|Table records that are used for the assessment.|

    You can now fill in the template with instructions, questions, and optional guidance for responding to a question, as well as sections that group the related questions.

4.  Navigate to the **General** tab.

    1.  Verify the template details, displayed in the **Details** section of the **General** tab.

    2.  In the Settings section, assign the Assessment reader role in the **Assessment reader role** field.

    3.  Select **Save**.

    For information on creating an assessment template, see [Create an assessment template](../../assessment-engine/task/sae-asmnt-template-create.md).

5.  Navigate to the **Questions** tab and set up the assessment questions.

    For information on adding instructions and questions to the assessment template, see [Add instructions and questions to an assessment template](../../assessment-engine/task/sae-asmnt-template-populate.md).

    ![Questions.](../../grc-business-continuity-management/image/asmt-temp-questions-tab.png)

6.  In the **Automations** tab, view the user responses and select **Open** to view the actions that are automatically triggered based on user responses.

7.  Select **Save** and **Publish**.

    A message is displayed that the assessment template is published and it can be used to send assessments. You can select **OK** or select **Return to template list**. The **Automations** and **Scoring** tabs are displayed in the assessment template. The Smart Assessment template is created and saved in the instance.


## What to do next

Configure the vulnerability type after adding the Smart Assessment template. For more information, see [Set up the Operational vulnerability type](set-up-op-vul-type.md).

