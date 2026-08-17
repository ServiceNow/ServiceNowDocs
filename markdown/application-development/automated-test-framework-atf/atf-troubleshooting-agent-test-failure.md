---
title: Troubleshoot test failures
description: Use ATF troubleshooting agent to significantly reduce the skills and resources needed to troubleshoot test failures on covered metadata.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-troubleshooting-agent-test-failure.html
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ATF troubleshooting agent, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
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

7.  Select **Triage with Otto** on the Test Results form.

    The ServiceNow IDE or ServiceNow Studio interface shows up.

8.  Review the prompt that is pre-populated depending on the test you're running and the selected summary record with a Failure status.

9.  Follow the automatic triaging process for the failed record.

    When a test fails, the agent automatically starts the troubleshooting process. It identifies the step where the failure occurred and analyzes the root cause. The agent then recommends possible fixes. After you select a recommended option, the agent applies the fix, updates the test code, and reruns the test automatically. When the test passes, it provides a summary of the changes made to resolve the failure.

    **Note:** See [Author, execute, and troubleshoot tests with Test Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/test-agent-use.md) if you want to execute a new application or a test.


