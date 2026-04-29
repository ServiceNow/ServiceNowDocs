---
title: Troubleshoot test failures
description: Use ATF troubleshooting agent to significantly reduce the skills and resources needed to troubleshoot test failures on covered metadata.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ATF troubleshooting agent, Use agentic AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Troubleshoot test failures

Use ATF troubleshooting agent to significantly reduce the skills and resources needed to troubleshoot test failures on covered metadata.

## Before you begin

**Note:** You must have either of these roles to access the ATF module and test results tables.

-   system\_admin
-   atf\_test\_admin
-   atf\_test\_designer
-   atf\_ws\_designer

Role required: atf\_triager + now\_assist\_panel\_user

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Tests**.

2.  Select the test you want to run.

    **Note:** You can also select **New** if you want to create a new test.

3.  On the Test new record form, enter all the details to create the test.

    **Note:** This step is applicable only if you have created a new test in the previous step.

4.  Add new test steps to the existing or newly created test.

5.  Select **Run Test**.

    The Run Test modal shows up.

6.  Select **Go to Result** to view the information on the test execution.

    If you instead select the Test Results related list after the test execution is completed, a list of step summary shows up. You are required to select a step summary record with a Failure status to know more about the reasons of its failure.

    The Test Results form shows up.

    **Note:** You can access the Test Results form by selecting **Go to Result** on the Run Test modal or from the Test Results related list.

7.  Select **Triage test failure** on the Test Results form.

    The Triage test failure modal shows up with the progress bar.

    The ATF troubleshooting agent shows up.

8.  Review the information in the ATF troubleshooting agent.

    You can read the complete analysis of the failed summary record. The ATF troubleshooting agent modal first starts with the planning of next steps that includes figuring out the next steps, executing the troubleshooting agent, analyzing the test steps and logs, traced, and changed metadata. The ATF troubleshooting agent finally gives you the root cause of the failure of the selected summary record. Select Show more to view the detailed analysis of the root cause. You can also see some tips suggested by the agent to fix the issue.


**Parent Topic:**[ATF troubleshooting agent](../reference/atf-troubleshooting-agent-landing-page.md)

