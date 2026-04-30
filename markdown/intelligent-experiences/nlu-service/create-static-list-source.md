---
title: Create a list vocabulary source
description: Create a list of words or phrases to act as a vocabulary source. The values in the list source are replaced by the synonym if they are detected in a user utterance.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [NLU vocabulary, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create a list vocabulary source

Create a list of words or phrases to act as a vocabulary source. The values in the list source are replaced by the synonym if they are detected in a user utterance.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Role required: admin, nlu\_admin, or nlu\_editor

## About this task

Creating a list vocabulary source enables your models to interpret all the alternate and actual values of the list if they appear in a user utterance. The model interprets those values as the synonym you provide when predicting an intent.

**Note:** During intent prediction, the synonym you provide replaces the value. During entity prediction, the actual value is used as the entity if the actual value or one of the alternate values are detected in the utterance.

In this example procedure, you're creating a list vocabulary source for your company's meeting rooms. You add the names of the rooms and alternatives your users might call them. Once you create the list, you add it to an utterance in an intent for the model. The model interprets the intent \(for example, \#BookMeetingRoom\) and uses the name the user entered as an entity \(for example, Everest\).

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Vocabulary Sources**.

2.  Click the **My lists** tab.

3.  Click **Create new list**.

    ![My lists tab of the Vocabulary sources page.](../images/create-vocab-list1.png)

4.  In the **Create a new list to refer to** window, configure the fields.

    |Field|Description|
    |-----|-----------|
    |Handle|Name for the vocabulary source. Used to refer to in an utterance.|
    |Language|Language of the vocabulary source. Synonym must be in the same language.|
    |Synonym|Word or phrase the model uses during intent prediction. Choose a commonly-occurring word in the same language as your model.|
    |Enable Fuzzy Matching|Check this box if you want the items on the list to match when a user utterance has slight misspellings.|
    |Make case sensitive|Check this box to make the values in the list case sensitive. Utterances with wrong cases won't match.|

    For this example, use the following configurations:

    -   **Handle**: `@meetingroom`
    -   **Language**: `English - en`
    -   **Synonym**: `meeting room`
    -   **Enable Fuzzy Matching**: Select the box.
    -   **Make case sensitive**: Leave the box clear.
    ![Create a new list to refer to window for the meeting room example.](../images/create-static-listT1.png)

5.  Click **Create**.

    Your list vocabulary source draft appears in the My lists section of the Vocabulary sources screen.

6.  Click the name of the list vocabulary source.

7.  Click **Add list item**.

8.  Enter a value for the list and click the green check mark.

    ![Add list item button in the values tab of the vocabulary list.](../images/create-static-listT2.png)

    In this example, you enter `Everest`.

9.  Double-click the area under **Alternate values** to add alternatives separated by a comma.

    ![Alternate values in a vocabulary list item.](../images/create-static-listT3.png)

10. Train the model to make the list vocabulary source available.


## What to do next

Add the rest of the break room names and alternatives.

You must retrain the model after updating a list vocabulary source. For more information, see [Train and try your NLU model](test-train-nlu-model.md).

Then you can use the list vocabulary source when annotating a training utterance. Use the @ symbol with the handle to refer to this vocabulary source.

**Parent Topic:**[NLU vocabulary](../concept/using-nlu-vocabulary.md)

