---
title: Configure the Now Assist Readiness Evaluation guided setup
description: Before you can review the Now Assist assessments in Workspaces Now Assist Readiness Evaluation , you must first complete the configuration for the five Now Assist jobs.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-09-29"
reading_time_minutes: 2
keywords: [Now Assist Readiness Evaluation, Now Assist Readiness Evaluation app, Now Assist Readiness, Now Assist assessment, GenAI assessment, AI assessment, Agentic AI assessment]
breadcrumb: [Configure, Now Assist Readiness Evaluation, Enable AI experiences]
---

# Configure the Now Assist Readiness Evaluation guided setup

Before you can review the Now Assist assessments in **Workspaces** &gt; **Now Assist Readiness Evaluation**, you must first complete the configuration for the five Now Assist jobs.

## Before you begin

Before completing this guided setup, you must first run the generative AI and agentic AI scheduled jobs. For more information, see [Run the GenAI/AgenticAI Assessment scheduled job](run-genai-agenticai-assessment-scheduled-job.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  In the search bar, search for `Now Assist Readiness Evaluation`.

3.  Select the Installed tab to view the installed store application **Now Assist Readiness Evaluation** App id: sn\_assess.

4.  Select **Now Assist Readiness Evaluation**.

5.  In the Get started area, select **Configure**.

6.  Review the Want to know how it works? screen, and then select **Continue**.

    You’re redirected to the Agentic AI Assessment Guided Setup.

    **Tip:** You can also access the Agentic AI Assessment Guided Setup screen by navigating directly to **All** &gt; **Now Assist Readiness Evaluation** &gt; **Guided Setup**.

    Three sections appear: Scheduled Jobs, Restricted Caller Access Privileges, and System Properties. The Restricted Caller Access Privileges and System Properties sections are only applicable if you want to work with Now Assist for HR Service Delivery \(HRSD\).

7.  Select **Start** in the Scheduled Jobs section.

    You’re redirected to the five scheduled Now Assist generative AI jobs.

    **Note:** You’re unable to run agentic AI scheduled jobs from this guided setup. To run agentic AI scheduled jobs, you must do so through the GenAI/AgenticAI Assessment scheduled job. For more information on running the agentic AI scheduled job, see [Run the GenAI/AgenticAI Assessment scheduled job](run-genai-agenticai-assessment-scheduled-job.md).

8.  Select the link to the specific scheduled job to have that job open in a new browser tab.

    For example, if you select the Now Assist Assessment - AI Search link, that scheduled job appears in a new browser tab.

9.  Select **Execute Now** to begin that job.

    The job begins and you’re redirected back to the guided setup.

10. Select **Next** in the guided setup.

11. Repeat steps [8](configure-nare-guided-setup.md#select-job-link-step)-[10](configure-nare-guided-setup.md#step-next-guided-setup) until you have run the scheduled jobs for the five Now Assist assessments.

    You have completed the Now Assist assessment jobs. If you ran the HRSD job, continue to the following optional steps.

12. If you have run the job for HRSD, select the **Change The State to Allowed for the following records** link on the Restricted Caller Access Privileges screen.

    **Note:** The following sub-steps can only be completed when in the Human Resources: Core application scope. For more information on changing application scopes, see [Select an application from the application picker](https://www.servicenow.com/docs/access?context=t_SelectAnAppFromTheAppPicker&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    1.  Change the Status column from `Requested` to `Allowed` on the Restricted Caller Access Privileges table, and then go back to the guided setup.

    2.  Select **Next** on the Restricted Caller Access Privileges screen.

    3.  Select the **Configure System Properties** link on the System Properties screen to review the system properties.

    4.  Select **Mark Complete**.

13. Select **Close**.


## Result

You have completed configuration for the Now Assist assessments.

## What to do next

You can navigate to **Workspaces** &gt; **Now Assist Readiness Evaluation** to review your assessment results.

