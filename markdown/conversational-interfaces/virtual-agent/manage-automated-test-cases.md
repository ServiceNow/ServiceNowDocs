---
title: Manage and run automated test cases in Virtual Agent Designer
description: Run reusable test cases of your published topics using the Automated Test Framework through Virtual Agent Designer to identify performance issues and prevent regressions before production.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Automated testing for Virtual Agent topics that use NLU topic discovery, Testing NLU/Keyword topics, Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Manage and run automated test cases in Virtual Agent Designer

Run reusable test cases of your published topics using the Automated Test Framework through Virtual Agent Designer to identify performance issues and prevent regressions before production.

## Before you begin

Plugin required: com.glide.cs.atf.

Role required: atf\_test\_designer, atf\_ws\_designer, atf\_test\_admin, virtual\_agent\_admin, or admin

## About this task

The **Manage test cases** button opens the **Run test cases** tab. Before you can run a test case, you previously must have created a test case. The **Create test cases** tab displays published topics that don't have associated automated tests. These topics appear in order from their last published date. After you select a topic name, a new window opens and you're directed to that topic in Virtual Agent Designer. From the topic, you can select **Test** to create a test case. For more information, see [Create an automated test in Virtual Agent Designer](create-automated-test-vad.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Slide the discovery type toggle switch to **NLU/keyword**, then select **Manage test cases** in the Resources list on the sidebar.

    You either see the **Run test cases** tab or the **Get started** button. The **Run test cases** tab displays topics that have had test cases previously created. The **Get started** button redirects you to the **Create test cases** tab to begin creating your topics' automated testing.

3.  In the list view, review the columns.

<table id="table_mzk_vst_nvb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Test case

</td><td>

Displays the linked test case name. Selecting the linked name opens a new window and directs you to that test within the Automated Test Framework. From the Automated Test Framework you can view test details, including test steps.

</td></tr><tr><td>

Topic

</td><td>

Displays the linked topic name. Selecting the linked name opens a new window and directs you to that topic in Virtual Agent Designer. Topics with multiple test cases are grouped.

</td></tr><tr><td>

Run status

</td><td>

Displays the run status of the test. Three statuses are possible:-   Ready: The test case is ready to be run.
-   In-progress: A temporary test case status that appears while the test case is running. After the test runs, the status returns to Ready.
-   Run recommended: The topic's published date is more recent than the test cases latest run date so there may be published updates for the topic. A run is recommended because the latest published topic and its related test cases are potentially out of synchronization.


</td></tr><tr><td>

Last run

</td><td>

Displays the date and timestamp of when the test was last run. Topics are grouped and sorted by the last test run date or if the same run happened across multiple topics, the topic's last published date.

</td></tr><tr><td>

Result

</td><td>

Displays either **Failed** or **Passed**. Pointing to the linked result displays a brief explanation of either the passing or failing step details. Selecting the linked result opens a new window and directs you to that test's **Test Results** in the Automated Test Framework where you can view more specific step fail or pass details. If the test case has passed, no changes happened between the latest published topic and its saved test case. If the test case has failed, a change happened between the latest published topic and its saved test case. For more information, see [View test results](https://www.servicenow.com/docs/access?context=atf-view-results-consolidated&version=australia&pubname=australia-application-development&ft:locale=en-US).**Tip:** You can view the test suite of all topics created and tested through Virtual Agent Designer by navigating to **Automated Test Framework \(ATF\)** &gt; **Suites**, and then selecting **Virtual Agent Topics**. For more information, see [Run an automated test suite](https://www.servicenow.com/docs/access?context=atf-run-suite&version=australia&pubname=australia-application-development&ft:locale=en-US).

</td></tr><tr><td>

Actions

</td><td>

Displays the **Delete** button that deletes the test case from this page and the Automated Test Framework.

</td></tr></tbody>
</table>4.  Select one, multiple, or all test case check boxes, and then select **Run**.

    **Tip:** The **sn\_atf.runner.enabled** property must be turned on to run test cases. After the property is turned on, you can select **Run**. Also, you can select the check box next to the Test case column header to select all test cases to be run.

    An in-progress banner appears and changes to a completion banner after your test results are ready. The Last run column updates and the last run test cases are moved to the top of the table.


**Parent Topic:**[Automated testing for Virtual Agent topics that use NLU topic discovery](../concept/automated-testing-va-topics.md)

