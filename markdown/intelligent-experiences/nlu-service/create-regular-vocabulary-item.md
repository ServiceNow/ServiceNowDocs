---
title: Create a regular vocabulary item
description: Add a word or phrase that your users might use, and match that vocabulary item to a synonym. Your model uses the synonym during intent prediction.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [NLU vocabulary, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create a regular vocabulary item

Add a word or phrase that your users might use, and match that vocabulary item to a synonym. Your model uses the synonym during intent prediction.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Create or use an existing NLU model for Virtual Agent or AI Search.
-   Role required: nlu\_editor, nlu\_admin, or admin. The editor must be assigned to the model.

## About this task

Regular vocabulary items provide the model with a synonym for words or phrases your users might use in an utterance. The model uses the synonym to replace the vocabulary when predicting the intent. Use a single word for the synonym when possible.

Regular vocabulary items are case-insensitive by default. If you need to create a case-sensitive vocabulary item, use a pattern vocabulary item. For more information, see [Create a pattern vocabulary item](create-pattern-vocabulary-item.md).

**Note:** Choose a synonym that is a commonly-occurring word in the same language as your model.

In this example scenario, you are adding a vocabulary item for the word credentials. Say that your users may use credentials to refer to their password. By creating a vocabulary item, you can make sure that the system correctly predicts the intent for an utterance such as reset my credentials.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab corresponding to your model's application, then select the name of your model.

3.  On the Model details tab of the model overview, select the **Vocabulary** card.

4.  In the Vocabulary tab, select **Add a vocabulary**.

    ![Add a vocabulary button in the Vocabulary tab of the Manage your model content phase.](../images/create-regular-vocabulary-item4.png)

5.  In the **Add a vocabulary** window, select **Regular** as the Type.

6.  Add a vocabulary word or phrase that your users might use, and then add the synonym that the model should use for intent prediction.

    In this example procedure, add credentials as the vocabulary and password as the synonym.

    ![Add a vocabulary window for a regular vocabulary item.](../images/create-reg-vocabT2.png)

7.  Select **Save**.


## What to do next

To deploy your new vocabulary item, train and publish your model again.

Add more vocabulary items to improve model coverage and accuracy.

**Parent Topic:**[NLU vocabulary](../concept/using-nlu-vocabulary.md)

