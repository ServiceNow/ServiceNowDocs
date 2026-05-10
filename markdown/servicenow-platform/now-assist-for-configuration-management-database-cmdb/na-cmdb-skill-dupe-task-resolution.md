---
title: Resolving de-duplication tasks with Now Assist
description: Now Assist recommends resolutions for duplication tasks by automating the choices that a user would typically make. Now Assist makes recommendations for the main CI, attribute relationship, and related item values to merge, and duplicate CI actions to perform. The process enhances accuracy and greatly reduces the time and effort needed to address CI duplication.
locale: en-US
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use generative AI skills, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Resolving de-duplication tasks with Now Assist

Now Assist recommends resolutions for duplication tasks by automating the choices that a user would typically make. Now Assist makes recommendations for the main CI, attribute relationship, and related item values to merge, and duplicate CI actions to perform. The process enhances accuracy and greatly reduces the time and effort needed to address CI duplication.

## Before you begin

The de-duplication task resolution assistant skill used in this process is supported starting with the Australia release. The skill is auto-activated when you activate the Now Assist for Configuration Management Database \(CMDB\) ServiceNow Store app.

Role required: cmdb\_dedup\_admin

## About this task

The skill uses optimal strategies to determine how best to remediate. The skill does not perform remediation actions, but displays the recommended actions and the reasoning behind them. You have the option to modify any suggestion and then perform remediation.

**Important:** After you remediate duplicates, be sure to fix the issue in the data source that generated the duplicate CIs and review downstream CIs. If the issue remains, the source will continue to generate duplicates.

This procedure describes how you can manually access the skill. In addition, any agentic workflow can use the skill.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **De-duplication Tasks**.

2.  Open the de-duplication task to remediate and on the task form, select **Remediate**.

3.  In the Remediate pop-up, select **Use the Duplicate CI Remediator \(Now Assist\)** and then select **Next**.

    The Reconcile Duplicate Task page displays the following sections:

    -   **A: Remediation steps that the skill evaluated**

        The skill precisely follows the sequence of manual remediation steps, presents the identical tabs that appear during manual de-duplication, and then goes directly to the final **Review and Confirm** tab.

        **Tip:** When you select one of the tabs, the selected de-duplication step page opens — exactly the page that you work in while performing the step manually as described in [Remediate a de-duplication task \(manual\)](../../configuration-management/task/reconcile-dup-task.md).

    -   **B: Summary section: Editable summaries of the proposed remediation steps**

        For any step in this section, select the down-arrow to expand and review the actions that the skill recommends. If you modify a proposed action, the reports in the Review and Confirm section immediately update to show the changes that would happen to CI data.

    -   **C: Review and Confirm section**

        The reports in this section are identical to the reports you see when you remediate manually. The reports display the number of changes and the tabs list the details of changes that would result with the currently proposed remediation actions. The reports are updated whenever you make changes to the proposed actions in the Summary section.

    ![Proposed remediation actions.](../image/na-cmdb-skill-dupe-task-res-assist.png)

4.  In the Summary section, review each recommendation in turn and assess whether to accept the recommended actions or modify them.

    See the example of reviewing the recommended attribute merges.

    **Important:** **Unique to main CI:** Each subsequent step depends on the selected main CI. If you change the main CI, then the Now Assist skill cannot proceed and you must perform remediation manually. None of the remaining steps \(merge attribute values, merge relationships, merge related items, and determine duplicate Cl actions\) have dependencies like main CI selection. You can therefore make changes and still proceed with the Now Assist process.

    The following caution appears if you change the main CI:

    ![Warning that changing the Main CI cancels the Now Assist process.](../image/na-cmdb-skill-dupe-change-main-ci.png)

5.  After you determine that all recommended actions are correct, select **Submit** and then select **Proceed** in the confirmation pop-up.

    ![Proceed with remediation.](../image/na-cmdb-skill-dupe-task-confirm.png)

    The system performs all remediation actions. The skill updates the Remediate Duplicate Task form with the `Closed Complete` value for **State** and documents all changes in the**Work notes**.


## Example: Review, possibly modify, and confirm recommended attribute merges

This example follows your work to determine whether the recommended attribute merges are the optimal choices. You will use a similar process for each of the other steps in the remediation process. For more information on the manual steps, see [Remediate a de-duplication task \(manual\)](../../configuration-management/task/reconcile-dup-task.md).

1.  Expand the **Merge Attribute Values** step to view the reasoning that led to the recommendations.

    ![Start the process of reviewing the attribute merge recommendations.](../image/na-cmdb-mng-dupe-attr-select.png)

2.  To view the merge recommendations, select the **Merge Attribute Values** tab.

    ![View the merge recommendations.](../image/na-cmdb-select-merge-attr-tab.png)

3.  Use your experienced judgment to evaluate whether the recommendations are the best choices and accept or modify the recommended merge values. Proceed to the next step when you have reviewed and possibly modified each recommendation.

4.  Review, assess, and update each step in turn.

    ![Be sure to verify or update the Now Assist recommendations in the remaining steps.](../image/na-cmdb-skill-dupe-task-summary.png)


**Note:** The **Reasoning** text that the skill displays is not updated when you make a change to any recommended step.

## What to do next

**Important:** After you remediate duplicates, be sure to fix the issue in the data source that generated the duplicate CIs and review downstream CIs. If the issue remains, the source will continue to generate duplicates.

**Related topics**  


[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md)

[Duplicate CIs remediation](../../configuration-management/concept/de-duplication-tasks.md)

[Detecting duplicate CIs](../../configuration-management/concept/id-detect-dup-ci.md)

[View CMDB Health Dashboard](../../configuration-management/concept/c_MonitorCMDBHealth.md)

