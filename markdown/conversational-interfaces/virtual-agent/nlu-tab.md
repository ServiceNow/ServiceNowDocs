---
title: Legacy - Natural Language Understanding of Virtual Agent responses
description: Virtual Agent \(VA\) uses the Natural Language Understanding \(NLU\) service to understand user input. Use the NLU Prediction tab to see how well NLU predicts intents, and to improve the intents so NLU makes better predictions.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Natural Language Understanding of Virtual Agent responses

Virtual Agent \(VA\) uses the Natural Language Understanding \(NLU\) service to understand user input. Use the **NLU Prediction** tab to see how well NLU predicts intents, and to improve the intents so NLU makes better predictions.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

The **NLU Prediction** tab on the Conversational Analytics Dashboard shows how well NLU is understanding user input in chat conversations. Virtual Agent comes with NLU models, but you can use the [Activate the NLU Workbench](https://www.servicenow.com/docs/access?context=activate-nlu-workbench&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to modify or create new models.

![NLU Predictions page.](../images/dashboard-NLU-entire.png)

To use the NLU Prediction tab, you must have the Chat Analytics Viewer \(chat\_analytics\_viewer\) role.

## NLU Prediction graph

The graph shows the daily performance of NLU predictions. The graph can show up to three lines, which represent:

-   **Correct Predictions**—NLU predicted multiple intents and showed them to users. They selected one.
-   **Incorrect Predictions**—NLU predicted multiple intents and showed them to users. They indicated that none of them were what they were looking for.
-   **Auto Selected Predictions**—NLU predicted a single intent based on chat input from the user. Sometimes, NLU returns multiple topics, each from a separate intent, and the user selects one.

The example graph only shows Auto Selected Predictions. On 2021-01-27, one intent was auto-selected, and on 2021-01-31, two intents were auto-selected.

**Note:** The vertical axis can have duplicate values because the axis has 10 increments. If the number of intents is less than 10, some values on the vertical axis appear more than once. For example, in the previous image, the maximum number of intents of all the days in the date range is 5. So, on the vertical axis there are two 1s, two 2s, two 3s, and so forth.

How are these values determined? The dashboard collects the following data:

1.  Did the NLU prediction model determine an intent?
2.  Did the predicted intent match the topic bound in the model to the intent?
3.  What's the prediction score and did the dashboard show multiple options to the end user to specify the correct intent, or did the dashboard just display the topic associated with one intent.
4.  After showing the user multiple intents, did the user select one?

The Conversational Dashboard uses the following algorithms on the data to populate the intent lists:

-   Correct Predictions—1, 2, 3, and 4 are true.
-   Incorrect Predictions—4 was false.
-   Auto Selected Predictions—3 was auto-selected, and there was no 4.

It's possible for intents to appear in several categories. For example, the Activate Account \(Ben\) intent appears in the **Correct Predictions** and the **Auto Selected Predictions** columns because NLU correctly predicted the intent and only presented a single response to the user.

## Improving NLU predictions

Clicking anywhere on the graph opens the Model Performance page. It shows a summary of intents predicted or not predicted over the date range specified on the graph.

![NLU Model Performance page.](../images/dashboard-model-performance.png)

See [Activate the NLU Workbench](https://www.servicenow.com/docs/access?context=activate-nlu-workbench&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to see how to use the NLU Workbench to improve NLU predictions.

-   **[Legacy - Modify models](../task/modify-model.md)**  
Test and modify the Virtual Agent models so they more accurately predict user intents.

**Parent Topic:**[Legacy - Using the Conversational Analytics Dashboard](use-the-dashboard-overview.md)

