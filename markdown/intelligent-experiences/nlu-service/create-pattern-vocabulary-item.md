---
title: Create a pattern vocabulary item
description: Use regular expression \(regex\) encoding to establish a pattern format for vocabulary items such as email addresses, phone numbers, and record naming conventions. You can create your own patterns for the vocabulary data in your instance.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [NLU vocabulary, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create a pattern vocabulary item

Use regular expression \(regex\) encoding to establish a pattern format for vocabulary items such as email addresses, phone numbers, and record naming conventions. You can create your own patterns for the vocabulary data in your instance.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Create or use an existing NLU model for Virtual Agent or AI Search.
-   Role required: nlu\_editor, nlu\_admin, or admin. The editor must be assigned to the model.

## About this task

Pattern vocabulary items use regular expressions \(regex\) to find variations of words and phrases in your users' utterances. The pattern then maps these variations to the synonym you provide. The synonym is used during intent prediction.

In this example scenario, you've created an NLU Virtual Agent model for requests related to authentication. To refer to multi-factor authentication, your users often use "MFA", "mfa", or "mfa authentication". You can provide a pattern to cover these variations. They are replaced with the matching synonym multi-factor authentication when predicting an intent.

See [Using regular expressions in entities](../concept/using-regular-expressions-nlu.md) for further details on regular expressions.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab corresponding to your model's application, then select the name of your model.

3.  On the Model details tab, select the **Vocabulary** card.

4.  Click **Add a vocabulary**.

    ![Add a vocabulary button in the Vocabulary tab of the Manage your model content phase.](../images/create-pattern-vocabulary-item9.png)

5.  In the **Type** field of the **Add a vocabulary** window, select **Pattern**.

6.  Add a regular expression that covers words or phrases in your users' utterances, and a synonym the model uses to predict the intent.

    In this example, the regular expression covers several variations of "mfa authentication".

    ![Add a pattern vocabulary item, and provide a synonym.](../images/create-pattern-vocabulary-item8.png)

7.  Click **Save**.

    **Result:** Your pattern vocabulary item appears in the Vocabulary section of your Model screen. Each time a user's utterance contains one of the spelling variations, the system recognizes the meaning as multi-factor authentication, in this example.


**Parent Topic:**[NLU vocabulary](../concept/using-nlu-vocabulary.md)

**Related topics**  


[NLU vocabulary](../concept/using-nlu-vocabulary.md)

[Using regular expressions in entities](../concept/using-regular-expressions-nlu.md)

