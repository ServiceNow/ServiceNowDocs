---
title: Pause and resume individual workflows
description: Pause individual workflow contexts. Specify the date and time of day at which the workflow context should resume.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow pause utility, Workflow administration, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Pause and resume individual workflows

Pause individual workflow contexts. Specify the date and time of day at which the workflow context should resume.

## Before you begin

Install and activate the Workflow Pause Utility plugin.

Role required: Workflow\_admin or workflow\_publisher, workflow\_creator

## About this task

When a workflow context is paused, the system saves basic information about the pause request, such as the resume date and time, in the wf\_pause\_request table. A workflow context automatically resumes at a specified date and time of day, but the paused workflow context can be manually resumed as needed.

## Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Live Workflows** &gt; **Active Contexts**.

2.  Select the individual workflow context that you are pausing.

    **Workflow Context** appears.

3.  In **Related Links**, click **Pause**.

    A **Workflow Pause Inputs** dialog appears.

4.  In the **Workflow Pause Inputs** dialog:

    1.  Click the calendar icon \(![Calendar icon](../image/WorkflowPauseResumeAtCalendar.png)\) to select the date, and enter the time of day \(in hours, minutes, and seconds\) at which the workflow should resume.

        You can select the current date or future date, but you must enter a time of day in the future. For example, to pause the workflow context at 13:30:00 \(1:30 pm\), select the date from the calendar, and then enter `13`, `30`, and `00` into the respective **Time:** fields.

    2.  Click the green check mark icon \(![Green check mark icon.](../image/Check.png)\) when finished.

        The selected date and time of day appear in the **Resume At** field.

    3.  Click **OK** to return to Workflow Contexts.

        The selected workflow is now paused. Use [Workflow pause request](monitor-workflow-pause-requests.md) to monitor its status.

5.  Manually resume a currently paused workflow context:

    Paused workflows resume on the date and time of day specified in the **Resume At** field.

    1.  Navigate to **Workflow** &gt; **Live Workflows** &gt; **Active Contexts**.

    2.  Select the individual workflow context that you are pausing.

        **Workflow Context** appears.

    3.  In **Related Links**, click **Resume**.


**Parent Topic:**[Workflow pause utility](../concept/workflow-pause-utility.md)

