---
title: Compare draft and published versions of your NLU model
description: Compare a draft trained Natural Language Understanding \(NLU\) model to its most recent published version. Test and review the changes to make sure that your draft model will have increased performance.
locale: en-US
release: yokohama
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Test and publish your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Compare draft and published versions of your NLU model

Compare a draft trained Natural Language Understanding \(NLU\) model to its most recent published version. Test and review the changes to make sure that your draft model will have increased performance.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Workbench - Advanced Features plugin and Predictive Intelligence plugin are installed and activated.
-   Role required: nlu\_editor, nlu\_admin, or admin. The editor must be assigned to the model.

## About this task

In this example scenario, you're training and trying a published NLU model in the NLU Workbench iteratively with the goal of improving its prediction confidence scores.

When you try an utterance against an NLU model:

-   If the model is trained and never published, the Test Model panel shows only trained model results.
-   If the model is trained and published, the Test Model panel shows only published model results.
-   If you've made changes to a published model and trained it, the Test Model panel shows both the trained model results and the published model results for comparison.

In this example procedure, you've cloned the model from a pre-built read-only HR model. You've cloned the model to create your own business-specific version of it while leveraging the existing intents from the pre-built model.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab corresponding to your model's application, then select the name of your published model.

3.  From the model's overview page, locate the **Build and train your model** card and click its **View phase**.

4.  Make a change to the intents, utterances, entities, or vocabulary.

    In this example scenario, you add a few more training utterances to the \#UpdateEmail intent.

5.  Train and try the changed model so you can see its prediction scores compared to the published version's scores.

    1.  On the **Train model** tab, click the **Train** button.

    2.  When training is finished, the system displays The model has been successfully trained.

    3.  In the **Try model** tab, enter this utterance: `wrong email address`.

    4.  Click **Go**.

    The panel displays predictions results for both the published model and the trained model. Compare the results of the two versions of the model, before and after your changes. In this example, the confidence score increased by a small margin. By making significant changes to the model content, the confidence score or even the intent predictions may change.

    ![Intent page with the comparing prediction results feature in the test panel.](../images/compare-draft-published01.png)


## What to do next

Use the information in the test panel to see if the changes you make will improve the model's performance. Once you are satisfied with your changes, test your model before publishing. Then, publish your model to replace the current published version.

**Parent Topic:**[Test and publish your model](../concept/testing-your-model.md)

