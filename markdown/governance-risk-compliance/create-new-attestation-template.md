---
title: Create and edit the attestation template
description: Create a customized attestation template in the Operational Resilience application that suits your business needs. By customizing an attestation template, you can add your own questions for your self-attestation. You can also edit an existing attestation template for your own business needs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Completing general administrative tasks, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Create and edit the attestation template

Create a customized attestation template in the Operational Resilience application that suits your business needs. By customizing an attestation template, you can add your own questions for your self-attestation. You can also edit an existing attestation template for your own business needs.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

The Operational Resilience application provides you with an attestation template as part of the base system. Creating an attestation template is optional.

If you have the sn\_oper\_res.admin role, you can also edit an existing attestation template for your own business needs. You can select and update the questions in the attestation template as shown in the following example.

![Modifying questions in the template.](../image/opres-modifying-questions-att-template.png)

You can update the questions according to your business requirements as shown in the following example.

![Updating the questions.](../image/opres-modifying-att-template.png)

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** to access the Assessment Workspace landing page.

2.  Select **New template** and then fill in the Template details in the Create assessment template form.

    1.  Enter the name of the template in the **Template name** field in the Details section of the **General** tab.

        You can add the name for the self-attestation template, for example, the self attestation assessment template.

    2.  Add details about the template in the **Description** field.

    3.  Select **Self attestation assessment** as the purpose from the Assessment templates list.

        Ensure that you select the correct purpose, as it is crucial for the self-attestation process.

    4.  Select the assessment target as **Self attestation**.

    5.  Select **Create**.

    6.  In the Settings section, add the duration of the assessment in the number of days, assign Assessment reader role such as sn\_oper\_res.user, and select **Save**.

    7.  Add questions and set up automation in the **Questions** and **Automation** tabs respectively.

        For more information, see [Add instructions and questions to an assessment template](../../assessment-engine/task/sae-asmnt-template-populate.md) and [Automate response](../../assessment-engine/concept/automate-response.md).

    8.  To publish the template, select **Publish**.

3.  To update the legacy template, complete the following steps.

    1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Admin** &gt; **Attestation Templates**.

    2.  To create a customized template, select **New**.

        ![Customized attestation template.](../image/attestation-template-new.png "Customized attestation template")

        ![Attestation template.](../image/new-attestation-template.png "Attestation template")

    3.  On the Assessment Metric Type New Record form, enter the name for the attestation template and select **Submit**.

        For a description of the field values on the form, see [Assessment Metric Type New Record form](../reference/attestation-template-reference.md).

        The attestation template is displayed in the templates list view as shown in the following example.

        ![Attestation template in the list view.](../image/attestation-template-list.png "Attestation template in the list view")

        By selecting **Submit**, you add the Operational Resilience tables and the application users to your customized attestation template.


