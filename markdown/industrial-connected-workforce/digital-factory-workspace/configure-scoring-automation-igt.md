---
title: Configure scoring and automation in Industrial Guided Tasks
description: Configure scoring and automation for guided tasks to provide a measure of task performance and automation of processes.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Industrial Guided Tasks, Configure, Digital Factory Workspace, Industrial Connected Workforce]
---

# Configure scoring and automation in Industrial Guided Tasks

Configure scoring and automation for guided tasks to provide a measure of task performance and automation of processes.

## Before you begin

Role required: sn\_icw\_igt.standard\_author

## Procedure

1.  Navigate to **Standards hub** &gt; **Standards**.

2.  Open the standard that you want to configure.

3.  Select **Advanced configuration**.

    You’re in the Smart Assessment Workspace.

4.  Configure the following advanced features in the Smart Assessment Workspace:

    1.  Configure automation of guided tasks by selecting the **Automations** tab.

        The availability of the Automation feature is dependent on the installation of Automation plugins described in [Smart Assessment Engine automation plugin dependencies](../reference/sae-automation-plugin-dependencies.md). For the detailed information about configuring automations in Smart Assessment Engine, see [Configure post-assessment actions](https://www.servicenow.com/docs/access?context=configure-post-assessment-actions&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

    2.  Configure scoring for guided tasks by selecting the **Scoring** tab.

        For detailed information about configuring Scoring in Smart Assessment Engine, see [Configure scoring for an assessment](https://www.servicenow.com/docs/access?context=configure-scoring-for-assessments&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

    3.  Enable normalized scoring for the standard.

        Normalized scoring applies advanced calculations that adjust raw assessment scores for guided tasks. To enable normalized scoring on a standard:

        1.  In the Smart Assessment Workspace, navigate to the scoring configuration for the standard.
        2.  Enable the normalization option for the standard.
        **Note:** Normalization must first be enabled on the assessment template category by an ICW administrator. To enable normalization, select **Enable Normalization** on the Industrial Guided Task category. For more information, see [Create an assessment template category](create-assessment-template-category-icw.md).

        When normalization is enabled and a normalized score is calculated on the assessment metric, the system saves the normalized score to the guided task instead of the raw score.


**Parent Topic:**[Configuring Industrial Guided Tasks](../concept/configuring-industrial-guided-tasks.md)

**Related topics**  


[Scoring assessments](https://www.servicenow.com/docs/access?context=scoring-in-assessments&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)

[Post-assessment automations](https://www.servicenow.com/docs/access?context=impact-automation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)

