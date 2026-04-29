---
title: Initiate a breakdown analysis
description: Start a breakdown analysis to investigate the root cause of a recurring or complex issue.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Breakdown Management, Industrial Workflows, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Initiate a breakdown analysis

Start a breakdown analysis to investigate the root cause of a recurring or complex issue.

## Before you begin

Role required: sn\_icw.deviation\_user or sn\_icw.deviation\_expert

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Factory Workspace** &gt; **Lists** \(![image.list-view-icon-dark]\).

2.  From the list of breakdowns, select the breakdown task for which you want to initiate the root cause analysis.

3.  Select the three-dot menu in the top corner and select **Start breakdown analysis**.

4.  On the Breakdown analysis form, fill in the field Description and change other fields as needed.

    For a description of the field values, see [Root cause analysis form](../reference/root-cause-analysis-form.md).

5.  Select **Save**.

    The Playbook opens that helps you get to the root of the breakdown. To learn more about Playbook Experience, see [About Playbook Experience](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

6.  From the Recommendations sidebar, attach a standard related to the breakdown analysis.

    To learn more about the Recommended Actions in the Digital Factory Workspace, see [Recommended Actions for the Industrial Connected Workforce](../../icw-industrial-connected-workforce/concept/recommended-actions-icw.md).

7.  On the Review information form, fill in the fields.

    For a description of the field values, see [Breakdown analysis form](../reference/breakdown-analysis-form.md).

8.  Select **Mark Complete**.

    The task state changes to Open and you’re navigated to the first step of the Playbook, which is Data Validation.

9.  After you're done with the first section called Input fix details, select **Mark complete**.

    This step and any of the subsequent steps can be reopened if needed.

    The Action results page opens where you can describe the corrective action taken, similarity with past events, and estimated costs of the breakdown.

10. After you're done with this step, select **Mark complete**.

    The Follow-up actions page opens, where you can create a follow-up action as a consequence of this event.

11. To create a follow-up action, select **Create New Follow-up Action** and fill in the fields.

    For a description of the field values, see [Action form](../reference/action-form.md).

12. After you're done with this step, select **Mark complete**.

    You're taken to the Monitoring step.

13. Check all the boxes to complete this step.

    The state of the breakdown has been moved to Monitoring.

14. To complete the analysis, select **Close analysis**.

15. Confirm your choice by selecting **OK**.


## Result

The state of the analysis moves to Closed and the record is displayed in **Lists** &gt; **Root cause analyses** &gt; **Done**.

**Parent Topic:**[Breakdown Management](../concept/breakdown-analysis.md)

