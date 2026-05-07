---
title: Create a test set
description: To create or add to an NLU test set, you can upload a file of test utterances matched with correct intents. Use the test set to assess the performance of your model.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Multi-model Batch Testing, NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# Create a test set

To create or add to an NLU test set, you can upload a file of test utterances matched with correct intents. Use the test set to assess the performance of your model.

## Before you begin

-   Ensure that the NLU Workbench - Core plugin, NLU Workbench plugin, NLU Workbench - Advanced Features plugin and Predictive Intelligence plugin are all installed and activated
-   You can use test sets with NLU models for Virtual Agent and AI Search.
-   Role required: nlu\_editor, nlu\_admin, or admin. The editor must be assigned to the model.

## About this task

Your CSV or XLSX \(Excel Workbook\) file should contain a table that pairs your test utterances with the intents that you expect for them. Your file can contain up to 10,000 utterances. Ensure that the file has columns titled "Utterance" and "Expected intent".

**Note:** For test sets in languages other than English, you must add the glide.import.csv.charset system property with the value UTF-8. See [Import sets properties](https://www.servicenow.com/docs/access?context=r_ImportSetsProperties&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

For the most accurate test results, include utterances that the model is likely to encounter from your users. Ensure that you have test utterances covering all the intents in your model.

Aim to include about 10% of test utterances with no expected intents. Including utterances with no expected intent helps assess your model's ability to detect irrelevant utterances that should not have any intent predicted.

**Note:** To indicate that a test utterance in your file has no expected intent, the value for "Expected intent" should be empty.

|Utterance|Expected intent|
|---------|---------------|
|Let me have a burger|Order|
|I want to pay|Payment|
|Get me something sweet|Order|
|Is the restaurant open| |
|Something wrong with my payment|Order, Payment|
|Total cost|Payment|

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **NLU Advanced Features** &gt; **Multi-model Batch Testing**.

2.  Click **Test sets**

3.  Click **Create test set**.

    ![Create new test set window.](../images/import_test_set_window.png)

4.  Choose a name for the test set.

5.  Choose a language.

6.  Click **Select file** and choose a CSV or XLSX \(Excel Workbook\) file.

7.  Click **Create**.

    Your test set appears in the list.


## What to do next

Use the test set to run a test on your models. To learn how, see [Test your model](test-your-model.md) or [Run a multi-model batch test](run-batch-test.md).

After you have created a test set, you can add more utterances to it. When viewing a test set, click **Import utterances**.

![Test set page with import utterances button.](../images/batch_test_import_utterances.png "Test set page with import utterances button")

Select a CSV or XLSX \(Excel Workbook\) file with your additional utterances to import.

![Import utterances window.](../images/import_utterances_window.png "Import utterances window")

Click **Import**. The system adds your utterances to the test set. After importing, rerun any tests that use the test set.

