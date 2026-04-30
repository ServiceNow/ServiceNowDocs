---
title: Handle failures caused by dynamic inputs in user testing of Virtual Agent topics
description: Avoid failures when performing automated tests for topics in Virtual Agent by controlling which inputs that you want to run as part of a test case.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-10-23"
reading_time_minutes: 1
breadcrumb: [Automated testing for Virtual Agent topics that use NLU topic discovery, Testing NLU/Keyword topics, Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Handle failures caused by dynamic inputs in user testing of Virtual Agent topics

Avoid failures when performing automated tests for topics in Virtual Agent by controlling which inputs that you want to run as part of a test case.

## Before you begin

Set up a test case for a topic that includes dynamic inputs. See [Create an automated test in Virtual Agent Designer](create-automated-test-vad.md) for more information.

Role required: virtual\_agent\_admin or admin

## About this task

When running a test in Virtual Agent Designer, some tests may fail even when a topic has fully functional components. These failures can happen based on various cases, such as timestamps based on a function that always returns the current time. The timestamp is created correctly when the test runs, but isn’t a match with the recorded timestamp in the test case. Similar examples include different users entering different names, email or physical addresses, or other information specific to each user. Any topic that returns different data based on time or other changing conditions is a potential failing point in testing. By deactivating test steps that use dynamic input, you can run tests that won't fail due to a change in the data found in those steps.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Slide the discovery type toggle switch to **NLU/keyword**, then select **Manage test cases**.

3.  Under the **Test Steps** tab, select the Active column of the test step you want to exclude, and set its value to `False`.

4.  Repeat Step 3 with as many test steps as you want to deactivate.

5.  Run or debug your test case.


**Parent Topic:**[Automated testing for Virtual Agent topics that use NLU topic discovery](../concept/automated-testing-va-topics.md)

