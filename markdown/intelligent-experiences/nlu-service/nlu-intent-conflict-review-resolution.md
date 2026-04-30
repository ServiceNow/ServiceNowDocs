---
title: Cross-model Conflict Review
description: Identify conflicting intents within or across models so you can take corrective actions, resolve such conflicts, and improve your NLU model performance.
locale: en-US
release: yokohama
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# Cross-model Conflict Review

Identify conflicting intents within or across models so you can take corrective actions, resolve such conflicts, and improve your NLU model performance.

## Summary usage

As the number of intents within a model increases, two intents may overlap in scope. This may occur when training utterances in one intent are almost identical to utterances in another intent. There may also be conflicting intents across models and even applications.

Utterances may also be marked as `Not relevant`, meaning that no intent should be predicted. When these irrelevant utterances are too similar to utterances assigned to an intent, they are displayed in Conflict Review. For more information, see [Irrelevance detection in NLU](irrelevance-detection-nlu.md).

To address and fix these issues, Cross-model Conflict Review runs an analysis on your models. Use the analysis to identify and resolve these issues prior to model publication and deployment.

## Installation

Cross-model Conflict Review is part of the NLU Workbench - Advanced Features app available on the ServiceNow® Store.

To use Cross-model Conflict Review, ensure that the NLU Workbench - Advanced Features \(com.snc.nlu.workbench.advanced\) plugin is active on your instance. For more information, see [Install NLU Workbench - Advanced Features](../task/install-nlu-workbench-adv-features.md) and [Activate the NLU Workbench](../task/activate-nlu-workbench.md).

## Roles

To access Cross-model Conflict Review, use the nlu\_admin or admin role. When assigned to a model, the nlu\_editor can resolve conflicts in that model.

## Running the analysis

The Conflict Review screen shows a list view of all conflict reviews created in your instance. When a review is completed, it's added to a running list of reviews. In this example scenario, you're creating the first review in your instance, so when it's completed, it's shown in the count as 1 of 1 reviews. As more conflicts arise over time, you will see multiple reviews in the list.

Conflict reviews are analyzed on either one or two NLU models. When you run an analysis on a single model, the system shows intents and utterances that are only in that model. When you run an analysis on 2 models, the system shows intents and utterances that are in both models.

Conflict reviews always run on the last trained version of the model\(s\) they analyze.

Conflict reviews have two types: Critical and Moderate. The standard approach is to begin with the critical ones.

When a conflict is detected, you can use one of following actions to resolve the conflict:

-   Ignore the conflict
-   Delete an identical or nearly identical utterance from one of the intents
-   Edit the utterances to make them more distinct from each other

In this example scenario, you're resolving a conflict where two different intents contain the exact same utterance.

1. Navigate to **All** &gt; **NLU Workbench** &gt; **NLU Advanced Features** &gt; **Cross-model Conflict Review**.

2. Select **Run analysis**.

3. In the **Model\(s\)** field on the Choose one or two models to analyze for conflicts screen, select two NLU models for the analysis. In this example scenario, you choose the demo\_hardware\_issue and demo\_it\_request models.

4. Select **Run Analysis**.

![You can choose one or two models for the conflict analysis and then click the Run Analysis button](../images/nlu-intent-conflict-review2.png "Running conflict analysis")

The Conflict Review screen refreshes to show the analysis, including the two models you selected for analysis, the counts of Critical and Moderate conflicts under review, the number of reviews that have been completed, and the run date for the analysis. If you point to the far right column on the screen you will see options to rerun the analysis, or delete it and start all over.

5. In the **Model\(s\)** column, select your two paired models so you can drill down into the review.

![Conflict review](../images/nlu-intent-conflict-review3.png "Conflict review")

The screen refreshes to show the details of the conflict review. Note the summary of the two models you chose for the analysis, their latest training dates, the types of conflicts they hold, and the version time stamp of the analysis. Note also the 0 of 1 count, which indicates that this is the first conflict review created in this instance. As the system detects more conflicts over time, and those conflicts are reviewed, the count increases.

If you were to determine the utterances in the image below are fine as they are, then you should click **Ignore**. Clicking Ignore tells the system you've completed your review, so it marks it as reviewed and moves on to the next conflict review. However, in this scenario, you don't ignore the conflict, because intents that share the same utterance are a conflict worthy of review.

![The Conflict Review details where two intents using the same utterance, which is a conflict worthy of review](../images/nlu-intent-conflict-review4.png "Reviewing conflict details")

To determine how you will resolve this conflict, consider the 2 intent names and the identical utterances they share. Consider which intent is more likely to use the laptop is really slow utterance. If you compare the 2 intent names closely, you might realize that a laptop that's really slow isn't the same as a laptop that doesn't work. However, a laptop that's really slow is indeed a laptop issue. So in this example scenario, you decide to dig deeper into the intents to scan the context of their other utterances.

Note also that when an intent uses unique utterances, it helps the system to more accurately predict which utterances belong to it. Hence, you will need to edit or delete the utterance from 1 of the 2 intents. In this example scenario, you decide to dig into the \#laptop\_not\_working intent.

6. Select **laptop\_not\_working**.

![You can open an intent to review the utterances inside it; this helps them determine which utterance to edit, delete, or ignore](../images/nlu-intent-conflict-review5.png "Reviewing overlapping utterances")

The \#laptop\_not\_working Intent screen appears, showing its current 3 utterances. You make the decision to delete the laptop is really slow utterance from the \#laptop\_not\_working intent.

![You can consider if you should edit, delete, or ignore the target utterance](../images/nlu-intent-conflict-review6.png "Reviewing the target utterance")

7. Click the **Delete this utterance** trash can icon.

![The user decision to delete the utterance in this intent because it's already being used in another intent; taking this action resolves the conflict](../images/nlu-intent-conflict-review7.png "Resolving conflicts")

The Confirm Delete screen appears.

8. Select **Delete**.

![A confirmation screen so users can confirm their decision to delete the utterance](../images/nlu-intent-conflict-review8.png "Deleting conflicts")

The Confirm Delete screen disappears, and the Utterances count drops from 3 to 2 because you've deleted the laptop is really slow utterance from the intent.

![Shows that the utterance count has dropped from 3 to 2 because they have deleted an utterance](../images/nlu-intent-conflict-review9.png "Confirmation of deleting an utterance")

9. Select **Train**.

A banner appears on the Intent screen, confirming the model is successfully trained.

10. Select **Conflict Review** in the navigator.

![A confirmation that shows the model has been successfully trained, and instructs the users to navigate back to the initial Conflict Review screen](../images/nlu-intent-conflict-review11.png "Confirmation of successfully training a model")

**Result:**

The Conflict Review list screen appears, showing your conflict review analysis is complete, and that it's been reviewed.

![A confirmation that shows the user's conflict has been reviewed, and appears as such on the final Conflict Review screen](../images/nlu-intent-conflict-review12.png "Confirmation that a conflict has been reviewed")

**Parent Topic:**[NLU Workbench - Advanced Features](nlu-workbench-advanced-features.md)

