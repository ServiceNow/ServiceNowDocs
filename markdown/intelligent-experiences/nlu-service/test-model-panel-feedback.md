---
title: Test panel feedback
description: When testing your NLU model on the Try model section of the test panel, use this feature to provide feedback on the model's intent predictions.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Test panel feedback

When testing your NLU model on the Try model section of the test panel, use this feature to provide feedback on the model's intent predictions.

## Summary context

When a model is trained and tested for an utterance and the model returns an intent prediction, you can provide a thumbs up or thumbs down rating on the predicted intent it returns. Marking a different intent prediction as correct adds the utterance to the corrected intent. All other feedback is captured for continual learning. The system then incorporates your feedback to optimize the model predictions. This feature requires the nlu\_admin role to access and test the model. NLU editors can also access the test panel if an NLU admin assigns them to it.

## Providing prediction feedback

The ratings you provide help the system to match an intent to an utterance. These ratings are essential for the system to continuously learn, evolve, and improve the accuracy of the intent predictions based on user input. They also enable you to notify the system if the intent prediction is correct or not.

The following scenarios below show examples of how to interact with your model test panel and provide prediction feedback to the system. In all scenarios, you use these four steps:

1.  In the **Build and train your model** phase of your model, select **Try model** to open the test panel.
2.  In the test panel's **Enter an utterance to test** field, enter a brief utterance that's similar to a training utterance in one of the intents.
3.  Click **GO**.

    Result: The system returns its predictions for your test utterance in the **Top Predictions\(s\)** section of the test panel.

4.  Click the **Thumbs Up** icon or the **Thumbs Down** icon.

    If you want the system to know it has predicted the correct intent for your utterance, select the **Thumbs Up** icon.

    In all other cases, select the **Thumbs Down** icon, which opens the **Provide feedback to improve this prediction** section. Here you can choose an intent other than the top predicted intent.


**Scenario 1**: On the Try model section of the test panel, you enter `help with hr` as the utterance. When the top prediction results appear, you're confident that the predicted intent is the correct match to your utterance. So in this case, you click the **Thumbs Up** icon.

Results:

-   The system predicted the correct intent, which in this case is **\#CreateHRGeneralInquiryCase**.
-   Your feedback notifies the system that it has matched the correct intent to your test utterance.

![How to use the Try model panel to test for the top intent prediction results](../images/test-panel-feedback001.png)

**Scenario 2**: In a separate model on a separate instance, a different user enters the same `help with hr` utterance. The system responds with the top prediction results for the intent, but the user isn't sure if it's the correct intent or not. So this user clicks the **Thumbs Down** icon, as shown in the image below.

![Here you select Thumbs Down to invoke the feedback option](../images/test-panel_feedback002.png)

Result: The panel expands to show the **Provide feedback to improve this prediction** section where users can submit feedback that may help to improve the intent prediction.

There are two options here:

-   If users click the **Its correct intent should be:** button, a list appears where they can choose a more appropriate intent for the test utterance. In this example scenario, a user selects the **Retrieve Work Location** intent, as shown in the image below.

    ![Here the user can choose a different intent in the model than the one the system predicted](../images/test-panel-feedback2.png)

-   If you click the **I'm not sure what the correct intent is** prompt, instead of returning a top prediction, the system shows the next best intent predictions available.

**Scenario 3**: In a separate model on a separate instance, another user submits an utterance that uses gibberish, or uses a language that's different from the language the model uses. For example, a user mistakenly submits an utterance comprised of both non-English and English languages, as shown in the image below.

![A user mistakenly submits an utterance that has more than one language, so the user provides feedback](../images/test-panel-feedback3.png)

Result: The system doesn't return a prediction because the utterance uses two different languages together. Since no intent was predicted, the user clicks the **Give feedback** option which expands the Try model section to show other intent alternatives.

![Since no prediction was made, you choose the 'No intent should be predicted 'option](../images/test-panel-feedback4.png)

So instead of choosing an intent from the prompt, this user selects the **No intent should be predicted** option.![The user doesn't choose any of the intents because they know the utterance was not a valid entry and the system didn't return a prediction](../images/test-panel-feedback5.png)

**Note:** When you choose and save **No intent should be predicted**, the utterance is removed from all intents which it is a part of.

**Scenario 4**: Along with choosing from a list of your model's intents for a prediction, you can also directly notify the system that the utterance is irrelevant to the model. To do this, you click the **Exclude this model's predictions for this utterance** button, then click **Save changes**.

![The user saves the changes, choosing not to have a prediction for the utterance you submitted](../images/test-panel-feedback6.png)

Result: A banner appears at the top of the screen confirming the user feedback for the prediction is saved, as shown in the image below.

![The banner confirms the feedback is saved](../images/test-panel-feedback7.png)

## Accessing your feedback records

Your feedback data is stored in the **ml\_labeled\_data** table, which is also used by other ServiceNow products. This table can also house multiple sources, such as Virtual Agent chat logs that can be used for future predictions.

**Parent Topic:**[Build and train your model](managing-model-content.md)

