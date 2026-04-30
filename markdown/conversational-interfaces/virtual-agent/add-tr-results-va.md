---
title: Add recommended topics and intents to Virtual Agent
description: After you run and review a Topic Recommendations report, select the pre-built topics and suggested intents to add to Virtual Agent.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Add, topic recommendations, intents, Virtual Agent, NLU, Natural Language Understanding]
breadcrumb: [Using Virtual Agent Topic Recommendations, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Add recommended topics and intents to Virtual Agent

After you run and review a Topic Recommendations report, select the pre-built topics and suggested intents to add to Virtual Agent.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

When you add a recommended topic to Virtual Agent, the Topic Recommendations app automatically does the following:

-   Duplicates the pre-built topics that you selected.
-   Creates empty topics for the intents you selected.
-   If you're using ServiceNow NLU:
    -   Creates a new NLU model if it doesn't exist.
    -   Updates and trains the NLU model with the added intents.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Topic Recommendations**.

2.  Go to the analysis results for your data source.

3.  Select one or more topic and intent cards to be added to Virtual Agent, and then select **Add to VA**.

    Selected cards are highlighted in blue and display as **Selected**, as shown in the following example.

    ![When selected, the topic card is blue and displays "Selected" with a check mark.](../images/selected-topic-recommendation.png)

4.  If you're using ServiceNow NLU, select one of the following options in the **Model** list:

    -   **Create new model**

        Select this option to create a new model group. If other languages are enabled for your instance, select the languages to add as secondary models in the group. Select **make primary** for the primary language in the group.

        ![Select Create new model and enter a name. Specify which language should be the primary language for the model.](../images/tr-create-model-add-va.png "Adding selected recommendations to a new model group")

        For more information about model groups, see [Multilingual model management](https://www.servicenow.com/docs/access?context=multilingual-model-managent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

    -   An existing model name

        If other languages are enabled for your instance, select the languages to add as secondary models in the group.

        ![In the Model list, choose an existing model and select the languages you want to add as secondary models for the topic in the group.](../images/tr-intent-add-nlu.png "Adding selected recommendations to an existing model group")

5.  Select **Add to VA**.


## Result

For recommended pre-built topics, Virtual Agent duplicates the topic \(but removes the **Template** portion of the file name\). For recommended intents, Virtual Agent creates a new topic mapped to the intent. These topics are added to the **Recommended** category in the Virtual Agent Designer Topics page.

In the Topic recommendations page, the topic card shows the date it was added and its status \(**Active** or **Inactive**\). To open the new topic from the Topic Recommendations page, select the info icon to open the overlay card. Select the open link icon ![Open link icon.](../images/icon-open-link.png) to open the topic in Virtual Agent Designer.

![The pre-built topic card in Topic Recommendations page shows the date that it was added and its current state. The duplicated topic card displays in the Topics page.](../images/tr-vad-topic.png "Recommended topic cards for an added topic")

