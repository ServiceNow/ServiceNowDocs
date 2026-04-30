---
title: Create a pattern entity
description: Create a pattern entity from a word or phrase with repeatable patterns, such as email addresses and phone numbers. These patterns help the system to recognize similar utterances based on the patterns.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [NLU entities, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create a pattern entity

Create a pattern entity from a word or phrase with repeatable patterns, such as email addresses and phone numbers. These patterns help the system to recognize similar utterances based on the patterns.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Create or use an existing NLU model for Virtual Agent or AI Search.
-   Create or use an existing intent.
-   Role required: nlu\_editor, nlu\_admin, or admin. The nlu\_editor must be assigned to the model.

## About this task

Pattern entities help your model identify, contextualize, and govern similar types of content. Inputs such as phone numbers and email address follow the same pattern. By creating a pattern entity, you can train the model to recognize all variations of those inputs.

**Note:** Pattern entities use regular expressions \(regex\). The regex field value is a Java regular expression. For more information on how to use regex, see [Using regular expressions in entities](../concept/using-regular-expressions-nlu.md).

In this example scenario, you've created an intent that's titled \#CheckITTicketStatus. In this example procedure, you're creating a pattern entity for incident record numbers.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab for your model's application, then the name of the model.

3.  On the model details page, select **Intents**.

4.  Select the name of an intent.

    In this example scenario, you select **\#CheckITTicketStatus**.

5.  Select one of the words of an utterance.

    In this scenario, you click **INC1234567**.

    ![Entity window in the Utterances tab of the intent details page.](../images/create-pattern-entity1.png)

6.  Select **Create New Entity**.

7.  In the Create a new entity window, configure the fields.

    For this example procedure, use these configurations:

    -   **Entity Name**: Enter `incidentnumber`
    -   **Type**: Select **Pattern**
    -   **Model Availability**: Select this box if you want this entity to be included in all intents in your model
    -   **Regex**: Enter `INC\d{7}`
    ![Create a new entity window for a pattern entity.](../images/create-pattern-entity2.png)

8.  Click **Save**.

    The pattern entity saves and appears in the **Associated Entities** tab. The model can use the pattern entity to interpret variations of the annotated utterance. For example, the model can match the \#CheckITTicketStatus intent if a user enters any incident record number.


**Parent Topic:**[NLU entities](../concept/entities.md)

**Related topics**  


[Create a simple entity](create-nlu-entities.md)

[Create a mapped entity](create-mapped-entity-lookup-source.md)

[Create a system-derived entity](create-system-derived-entity.md)

[Create an open-ended entity](create-open-ended-entity.md)

[Import entities](import-common-entities-nlu.md)

[Using regular expressions in entities](../concept/using-regular-expressions-nlu.md)

