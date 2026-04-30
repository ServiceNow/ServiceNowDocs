---
title: Model management
description: Manage your NLU model's life cycle in the NLU Workbench. Model management phases guide you through the iterative process of building, testing, and publishing your model.
locale: en-US
release: yokohama
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Natural Language Understanding, Enable AI experiences]
---

# Model management

Manage your NLU model's life cycle in the NLU Workbench. Model management phases guide you through the iterative process of building, testing, and publishing your model.

![Model management life-cycle.](../images/model-management-5.png)

Bringing your NLU model from creation to deployment requires multiple steps, separated into phases. You can return to earlier phases when you want to adjust and maintain your model.

The phases available for your model depend on the model's application. The system will display a phase, button, or function only when it applies to your model's application.

To use the model management phases, ensure you have all the necessary NLU plugins. For more information, see the following resources:

-   [Activate the NLU Workbench](../task/activate-nlu-workbench.md)
-   [Install NLU Workbench - Advanced Features](../task/install-nlu-workbench-adv-features.md)
-   [Install Intent Discovery](../task/install-intent-discovery.md)

**Note:** NLU Workbench - Advanced Features and Intent Discovery are available from the ServiceNow Store. NLU model testing and performance monitoring require NLU Workbench - Advanced Features.

## Create a model

To create a model for Virtual Agent or AI Search, navigate to **NLU Workbench** &gt; **Models**. The Virtual Agent tab opens by default. Select the appropriate tab for the model you want to create.

![In the NLU Workbench, Virtual Agent tab, the Create new model button is highlighted.](../images/model-management-phasesV1.png) You can choose different ways to create a model:

-   **Use prebuilt model**: Copy one of the included read-only models, and add content specific to your business.
-   **Import data from CSV**: Upload a CSV file that contains training utterances and matched intents.
-   **Start from blank**: Go through the process of setting up a new model from scratch.

To get started, see [Creating models](creating-models.md).

## Model management phases

After creating a model, access its management phases by navigating to **NLU Workbench** &gt; **Models**. Select the tab for your model's application, then the name of the model to open the **Model details** page on the model overview.

There are three phases on a Virtual Agent model's overview page: Build and train your model, Test and publish your model, and Tune your model. These phases guide you as you build and improve your model.

![Model management phases for a trained NLU model.](../images/model-managementT2.png)

## Build and train your model

Build the model by adding and managing content:

-   Intents: Add more intents to broaden the range of user requests that your model can understand.
-   Entities: Add more entities so that your model can extract more contextual details from your users' requests.
-   Vocabulary: Add vocabulary to enable the model to better understand words and phrases that are specific to your business, such as industry terms and acronyms.
-   Test set: Add test utterances and their expected intents to your model's default test set.

To learn more, see [Build and train your model](managing-model-content.md).

Train your model using utterances that the model is likely to encounter from your users. To learn more, see [Train and try your NLU model](../task/test-train-nlu-model.md).

## Test and publish your model

Test your model to gauge the performance and identify areas for improvement.

**Note:** Model testing requires the NLU Workbench - Advanced Features store application. For more information, see [NLU Workbench - Advanced Features](nlu-workbench-advanced-features.md).

For more information on testing and thresholds, see [Test and publish your model](testing-your-model.md).

When you're satisfied with the results of testing, publish your model to make it available for use by other applications. For more information, see [Publish your NLU model](../task/publish-nlu-model.md).

## Tune your model

If NLU Workbench - Advanced Features is installed, and your model is created for Virtual Agent, the **Tune your model** phase is enabled. With this phase, you can use **Expert Feedback Loop** to incorporate actual user utterances into your model.

For more information, see [Tune your model](nlu-tune-your-model.md).

If your model is created for Issue Auto Resolution, you will be taken to IAR Tuning by selecting the name of your model in the IAR tab of the NLU Workbench homepage. For more information, see [Issue Auto Resolution Tuning in NLU](issue-auto-resolution-tuning-nlu.md).

## Model settings

Use the **Settings** page of the model overview to change the name and description of the model. You can also modify the confidence threshold of the model. The confidence threshold determines how confident the model must be to predict an intent.

For more information, see [NLU model settings](nlu-model-settings.md).

-   **[Creating models](creating-models.md)**  
Creating models is the first step to taking advantage of Natural Language Understanding \(NLU\) in your instances. Create models for Virtual Agent and AI Search in the NLU Workbench.
-   **[Build and train your model](managing-model-content.md)**  
After creating a model, build the model's content by adding intents, entities, vocabulary, and test set utterances. Your NLU model content determines how the model responds to user inputs.
-   **[Test and publish your model](testing-your-model.md)**  
Assess the performance of your NLU model to identify areas for improvement. Then publish your model to make it available to other applications such as Virtual Agent.
-   **[Irrelevance detection in NLU](irrelevance-detection-nlu.md)**  
Keep Virtual Agent chats focused with Irrelevance detection. Use the Irrelevance detection feature to train your NLU model to avoid making predictions for utterances that are not relevant.
-   **[Tune your model](nlu-tune-your-model.md)**  
On your model's overview in NLU Workbench, open the **Tune your model** phase to review and incorporate user utterances from the Expert Feedback Loop.
-   **[NLU model settings](nlu-model-settings.md)**  
Change your NLU model's name, description, or confidence threshold on the **Settings** page of the model overview.

**Parent Topic:**[Natural Language Understanding](nlu-landing.md)

