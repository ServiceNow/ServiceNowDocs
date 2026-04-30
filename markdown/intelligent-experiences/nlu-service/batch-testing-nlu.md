---
title: Multi-model Batch Testing
description: Test multiple Natural Language Understanding \(NLU\) models against a large set of utterances to evaluate the performance of the models. Add test sets, test multiple models, and see test results.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# Multi-model Batch Testing

Test multiple Natural Language Understanding \(NLU\) models against a large set of utterances to evaluate the performance of the models. Add test sets, test multiple models, and see test results.

## Summary usage

Use Multi-model Batch Testing to create and upload test sets comprised of utterances and their expected intents. You can then run tests against your NLU models.

Multi-model Batch Testing works with models for all supported NLU languages. See [NLU language support](nlu-language-support.md).

## Installation

Multi-model Batch Testing is part of the NLU Workbench - Advanced Features app available on the ServiceNow® Store.

To use Multi-model Batch Testing, ensure that the NLU Workbench - Advanced Features \(com.snc.nlu.workbench.advanced\) plugin is active on your instance. For more information, see [Install NLU Workbench - Advanced Features](../task/install-nlu-workbench-adv-features.md) and [Activate the NLU Workbench](../task/activate-nlu-workbench.md).

## Test sets

Test sets are lists of utterances and matched intents. Create a test set by using a table in a CSV or XLSX \(Excel workbook\) file. The table should contain two columns: one for utterances, and one for the expected intent. Your test set can include up to 10,000 rows.

To get the most out of testing your NLU models, your test sets should include utterances that the model is likely to encounter from your users. Test utterances should be in the same language as the model to be tested. The test set should also include utterances with no expected intents. Including utterances with no expected intent helps assess your model's ability to detect utterances which are irrelevant and shouldn't have any intent predicted.

By including these types of utterances, the test better assesses the model's ability to perceive intents and respond to your users. If your test set does not cover at least 60% of the intents of the models, you can still run the test but the recommended threshold may not be optimal.

**Note:** Certain test utterances are skipped during the test if their expected intent does not match any intents in the models.

To create a test set, see [Create a test set](../task/import-batch-test-set.md).

After you have a test set, you can test trained NLU models. To begin testing, see [Run a multi-model batch test](../task/run-batch-test.md).

After running a test, your results appear on the **Test results** page.

## Test results

The **Test results** page lists your completed and in-progress tests. At a glance, the results page shows the models tested against, the number of utterances, and prediction percentages.

![Multi-model Batch Testing page with completed tests.](../images/batch-testing-nlu01.png)

To see the details of a test result, click the name of the test set.

The **Overview** page shows summary information about the results and includes a graphic with a breakdown of predictions.

The **Intents that need attention \(Current model\)** shows the top 5 missed and incorrect intents. Click the intent name to drill down into the test utterances that were predicted incorrectly. Use this information to improve the model.

The **Detailed results** tab lists information about each utterance that was tested. From here, you can see the prediction outcome and confidence per model for each utterance. Filter the results by using the search bar or interacting with the filter tools and column headers.

You can also export the test results to a CSV file by clicking **Export**. The file includes the same columns as the detailed results page.

For more information on understanding your test results, see [Test and publish your model](testing-your-model.md).

-   **[Create a test set](../task/import-batch-test-set.md)**  
To create or add to an NLU test set, you can upload a file of test utterances matched with correct intents. Use the test set to assess the performance of your model.
-   **[Run a multi-model batch test](../task/run-batch-test.md)**  
Test multiple Natural Language Understanding \(NLU\) models against a test set. Evaluate the quality of your models and refine them to improve intent prediction.

**Parent Topic:**[NLU Workbench - Advanced Features](nlu-workbench-advanced-features.md)

