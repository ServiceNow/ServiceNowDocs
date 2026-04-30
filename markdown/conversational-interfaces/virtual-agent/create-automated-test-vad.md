---
title: Create an automated test in Virtual Agent Designer
description: Create automated tests in Virtual Agent Designer and run tests regularly against ideal conversation topic flows. You can create multiple automated tests for a topic to capture different conversation flows for various situations such as ideal conversation paths or errors.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-06"
reading_time_minutes: 2
keywords: [Automated, Test, Virtual Agent, designer, om.glide.cs.atf]
breadcrumb: [Automated testing for Virtual Agent topics that use NLU topic discovery, Testing NLU/Keyword topics, Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create an automated test in Virtual Agent Designer

Create automated tests in Virtual Agent Designer and run tests regularly against ideal conversation topic flows. You can create multiple automated tests for a topic to capture different conversation flows for various situations such as ideal conversation paths or errors.

## Before you begin

Plugin required: com.glide.cs.atf.

Role required: atf\_test\_designer, atf\_ws\_designer, atf\_test\_admin, virtual\_agent\_admin, or admin

## About this task

As you work on a published topic, setup topic, or small talk topic, use the **Test** option in the topic header bar to run your conversation in a chat test window. The default test window is the web \(Service Portal\) chat client. Use the **Create test case** button to create a test case and save the test case in the Automated Test Framework.

**Note:** You can find a list of NLU/Keyword test cases by selecting the **Manage NLU/Keyword test cases** button on the Virtual Agent Designer main page. Automated tests are also listed on the Automated Test Framework \(ATF\) Tests \[sys\_atf\_test\] table. For more information on managing NLU/Keyword test cases, see [Manage and run automated test cases in Virtual Agent Designer](manage-automated-test-cases.md)

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Select a published topic.

3.  In the topic's header bar, select **Test**.

4.  Select **Create test case**.

    **Note:** The **Create test case** button is only available for published topics that are non-read only with one of the following topic types: **Topic**, **Setup Topic**, or **Small talk**.

    The topic's test client restarts and the test case begins to capture your ideal conversation. While capturing your test case, the **Include Topic Discovery** and the **Context** tabs are unavailable.

5.  Enter the conversational flow that you want to capture and test.

    **Tip:** Select **Restart** at any time to restart the topic conversation and test case capture.

6.  Select **Stop**.

    The **Test case name** field displays the topic's name along with the date and timestamp. For example: `[Topic name] 3/28/2022, 3:32:19 PM`.

7.  Perform one of the following actions.

<table id="choicetable_ezr_zt3_w5b"><thead><tr><th align="left" id="d127027e234">

Option

</th><th align="left" id="d127027e237">

Description

</th></tr></thead><tbody><tr><td id="d127027e243">

**Discard the test case**

</td><td>

1.  Select the trash can icon.
2.  Select **Discard**.

The test case is discarded and the testing conversation restarts.

</td></tr><tr><td id="d127027e266">

**Save the test case**

</td><td>

1.  Change the **Test case name** to your preferred test case name.
2.  Select **Save**.

The test case is saved. To review your saved test case, select **Manage** on the confirmation banner to open the **Manage test cases** tab in a new window, or go to **Manage NLU/keyword test cases** on the Topics page.

</td></tr></tbody>
</table>
**Parent Topic:**[Automated testing for Virtual Agent topics that use NLU topic discovery](../concept/automated-testing-va-topics.md)

