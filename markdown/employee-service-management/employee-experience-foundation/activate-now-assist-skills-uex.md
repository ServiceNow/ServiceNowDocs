---
title: Activate Now Assist for Employee Experience skills
description: You can activate the Now Assist for Employee Experience skills..
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Generative AI for Employee Center, generative AI for UEX, configuration]
breadcrumb: [Now Assist for Employee Experience, Unified Employee Experience, Employee Service Management]
---

# Activate Now Assist for Employee Experience skills

You can activate the Now Assist for Employee Experience skills..

## Before you begin

Before activating the Now Assist for Employee Experience skills, you must install the Now Assist for Employee Experience plugin.

**Note:** By default, the summary appears in Approvals ion Employee Center and service portals.

Role required: admin

## About this task

Activate the Now Assist for Employee Experience plugin to enable generative AI on your instance.

-   Admins can select the roles for whom the skill is available.
-   When you don't have the required role to read the record, you can't see the skill summary.
-   When you activate the skill, you can see the skill or summary.
-   The OOB Applicability record includes a filter for the Employee Center portal. To display a summary on any portal, add an applicability record for that portal. The filter format is `{"URL Suffix of portal" + table : <tableName>}`.
-   By default, the availability filter isn't available. Any changes or customization can affect the availability of the summary widget.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

    If you’re already in the Now Assist Admin console, select the **Now Assist Skills** tab.

2.  On the navigation panel, select **Employee** &gt; ****Employee Center to review the skill set.

    ![Illustration of available skills in Employee Center](../images/uex-skill-activation.png "Now Assist for Employee Experience")

    Toggle between the list and grid layouts for optimum viewing experience.

3.  Verify and use the out-of-box settings in **General details**, **Choose input**, and so on.

    Use the options in the default setup for the most common use cases.

    -   Select the step in the guided setup navigation.
    -   Return to a previous step by selecting **Back**.
    -   Select **Save and continue** to go to the next step.
4.  [Clone and edit a ServiceNow skill](https://www.servicenow.com/docs/access?context=clone-and-edit-servicenow-skill&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

5.  Go to **Define Trigger** and select one of the following triggers.

    -   Automatic \(Default\) - Generates auto-summarization for the request, requested item, or case for approval task.
    -   Manual - Requires user to trigger summarization for the request, requested item, or case for approval task.
    ![Triggers selected for Now Assist chat summarization.](../images/uex-skill-trigger.png "Define triggers")

6.  Choose where to display Now Assist skills.

    For Now Assist for Employee Experience, use **In-product desktop**.

7.  Review your choices and complete the configuration by selecting **Activate**.

8.  Select **Activate skill**.

    On activation, the skill state changes to active.


## Result

On successful configuration, approval users can see summarization for approvals. For more information, see [View summarization for approvals](view-summarization-approvals.md).

**Note:** After installing Now Assist for Employee Experience \[sn\_ex\_gen\_ai\] plugin and activating the skills in the Now Assist Admin Center, the Summary appears in Approvals on Employee Center and service portals. To enable the summary on the custom portals, follow the instructions available in [KB2739995](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2739995) and update the `sn_nowassist_skill_config` table.

**Related topics**  


[Configuring Now Assist settings and features](https://www.servicenow.com/docs/access?context=configuring-na-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

