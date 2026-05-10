---
title: Natural Language Understanding of Virtual Agent responses
description: Use the NLU Prediction tab to see how well NLU predicts intents, and to improve the intents so NLU makes better predictions.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using the Conversational Analytics Dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyze VA performance, Virtual Agent, Conversational Interfaces]
---

# Natural Language Understanding of Virtual Agent responses

Use the **NLU Prediction** tab to see how well NLU predicts intents, and to improve the intents so NLU makes better predictions.

Virtual Agent \(VA\) uses the Natural Language Understanding \(NLU\) service to understand user input. **NLU Prediction** tab on the Conversational Analytics dashboard shows how well NLU is understanding user input in VA conversations. Virtual Agent comes with NLU models, but you can use the [Activate the NLU Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nlu-service/activate-nlu-workbench.md) to modify or create new models.

![NLU Predictions page.](../images/dashboard-NLU-entire-pae.png)

To use the NLU Prediction tab, you must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role.

## NLU Prediction indicator

The NLU Prediction indicator shows the daily performance of NLU predictions mapped against the user intent.

-   **Intent Unsupported**—NLU did not recognize user intent.
-   **Intent Auto Selected**—NLU predicted a single intent based and the user selected the same. Sometimes, NLU returns multiple topics, each from a separate intent, and the user selects one.
-   **Intent Correctly Predicted**—NLU predicted multiple intents and the user selected one of them.
-   **Intent Incorrectly Predicted**—NLU predicted multiple intents and the user indicated that none of them were what they were looking for.

**Note:** The vertical axis can have duplicate values because the axis has 10 increments. If the number of intents is less than 10, some values on the vertical axis appear more than once.

The dashboard collects the following data points to arrive at the indicators.

1.  Did the NLU prediction model determine an intent?
2.  Did the predicted intent match the topic bound in the model to the intent?
3.  What's the prediction score and did the dashboard show multiple options to the end user to specify the correct intent, or did the dashboard just display the topic associated with one intent.
4.  After showing the user multiple intents, did the user select one?

It's possible for intents to appear in several categories. For example, an intent can appear in the **Intent Correctly Detected** and **Intent Auto Selected** because NLU correctly predicted the intent and only presented a single response, which the user accepted.

## Improving NLU predictions

Clicking anywhere on the NLU Prediction indicator opens the Model Performance page. It shows a summary of intents predicted or not predicted over the date range specified on the graph.

![NLU Model Performance page.](../images/dashboard-model-performance.png)

See [Activate the NLU Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nlu-service/activate-nlu-workbench.md) for information on how to use NLU Workbench to improve NLU predictions.

-   **[Modify models](../task/modify-model-pae.md)**  
Test and modify the Virtual Agent models so they more accurately predict user intents.

**Parent Topic:**[Using the Conversational Analytics Dashboard](use-the-dashboard-overview-pae.md)

