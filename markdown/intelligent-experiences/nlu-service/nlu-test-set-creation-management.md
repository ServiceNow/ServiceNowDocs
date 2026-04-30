---
title: Test set creation and management
description: Use the default test set of your NLU model to test the model's performance and accuracy. Manage your test set over time by building or updating its content in the NLU Workbench.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Test set creation and management

Use the default test set of your NLU model to test the model's performance and accuracy. Manage your test set over time by building or updating its content in the NLU Workbench.

Embedded video: Test set management in NLU Workbench

**Note:** To test your model, install the ServiceNow® Store application NLU Workbench - Advanced Features. For more information, see [Install NLU Workbench - Advanced Features](../task/install-nlu-workbench-adv-features.md).

When you create an NLU model for Virtual Agent or AI Search, a default test set is created and associated to the model. You can use the default test set to evaluate the model’s performance. Initially the test set is empty, ready to be populated with your content.

## Access your default test set

Access your default test set with one of the following methods.

-   Navigate to **All** &gt; **NLU Workbench** &gt; **Models**. Select the tab for your model's application, then the name of your model from the list. On the model's overview page, find the **Build and Train your model** card and select its **View phase** button. Then select the **Test set** tab. ![On the NLU model overview page, the Test set tab is highlighted.](../images/nlu-test-set-creation-management1.png)
-   Navigate to **All** &gt; **NLU Workbench** &gt; **Models**. Select the tab for your model's application, then the name of your model from the list. On the model's overview page, select the **Test Coverage** tile. ![On the model overview page, the Test Coverage tile is highlighted.](../images/nlu-test-set-creation-management2U.png)
-   Navigate to **All** &gt; **Multi-model Batch Testing** &gt; **Test sets** tab. Find the name of your model. Default test sets are labeled as **Default**.![An entry in Multi-model Batch Testing's Test sets table.](../images/nlu-test-set-creation-management3.png)

## Add content to your default test set

Add utterances and their expected intents to build and manage your test set over time. You can add content to the default test set with the following methods:

-   Add test utterances and their expected intents manually. From the model's overview page navigate to **Build and train your model** &gt; **Test set** tab. Type your input into the Type a test utterance here field, select an appropriate intent, then select the **Add** button.

    These test utterances are assigned a source of Manual.

-   Import test utterances and their expected intents from a CSV file or from other models. To import content to a default test set, from the model's overview page navigate to **Build and train your model** &gt; **Test set** tab. Select **Import test utterances**.

    Imported test utterances are assigned a source of Manual.

-   The Expert Feedback Loop feature lets you add actual user utterances from Virtual Agent chat logs to the test set.

    These test utterances are assigned a source of Expert Feedback. For more information, see [NLU Expert Feedback Loop](nlu-expert-feedback-loop.md).


## Test Coverage

The Test Coverage score is the percentage of a model's enabled intents that have test utterances in the default test set. Before testing your model, ensure that there is at least 60% coverage. The higher the Test Coverage score, the more accurate the performance testing results.

Your test coverage needs to be at least 60%, with at least 5 test utterances per intent, in order for the system to provide an optimal confidence threshold during batch testing. For more information about the confidence threshold, see [NLU model settings](nlu-model-settings.md).

Aim to have about 10 percent of a model's test utterances marked as "not relevant", meaning that there is no intent associated. This helps assess how the model handles irrelevant utterances which should not have any intent predicted. For more information about irrelevant utterances, see [Irrelevance detection in NLU](irrelevance-detection-nlu.md).

## Use the test set

To use the default test set from the **Test and publish your model** phase, see [Test and publish your model](testing-your-model.md).

To use the test set in Multi-model Batch Testing, see [Multi-model Batch Testing](batch-testing-nlu.md).

## Characteristics of default test sets

When an instance is upgraded, default test sets are created for any existing models that don't already have them.

When you copy a model using **Duplicate this model**, the original's default test set is copied into the new model. For more information, see [Duplicate an NLU model](../task/clone-nlu-model.md).

The utterances in the test set shouldn't be the same as the utterances in the training set.

Default test sets can't be deleted separately from their models.

Test set utterances should be in the same language as their model.

Test sets are available for Virtual Agent or AI Search models.

## Downloading or moving default test sets

Default test sets can be downloaded or moved as follows.

-   Default test sets can be separately downloaded in CSV format. To download the test set, from the model's overview page navigate to **Build and train your model** &gt; **Test set** tab. Select **Download test set**.

    **Note:** Test sets that are downloaded from **Download test set** contain test utterances and their expected intents, but not the sources.

-   Default test sets can be moved with update sets. When you add an NLU model to an update set, its default test set is added, including test utterances, expected intents, and sources. For more information, see [Add an NLU model to an update set](../task/add-model-update-set.md).
-   When using the **Export model as CSV** function in the **All existing models** table, the default test set is not included. For more information, see [Export an NLU model](../task/export-nlu-model.md).

**Parent Topic:**[Build and train your model](managing-model-content.md)

