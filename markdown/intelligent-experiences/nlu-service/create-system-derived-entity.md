---
title: Create a system-derived entity
description: Create a custom entity that's derived from a default system entity such as date, time, duration, or location.
locale: en-US
release: yokohama
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [NLU entities, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create a system-derived entity

Create a custom entity that's derived from a default system entity such as date, time, duration, or location.

## Before you begin

-   Make sure that the [NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.](activate-nlu-workbench.md)
-   [Create or use](../concept/creating-models.md) an existing NLU model for Virtual Agent or AI Search.
-   [Create or use an existing intent.](create-nlu-intent.md)
-   Role required: nlu\_editor, nlu\_admin, or admin. The nlu\_editor must be assigned to the model.

## About this task

System entities are pre-built in your ServiceNow instance by default, and appear on the Entities section of the Model screen. These entities, such as DATE, TIME, and DATE\_TIME, are enabled by default. You can disable and re-enable them if needed by clicking **Enable**.

System-derived entities extend your system entities, providing more context. For example, your model already understands date formats thanks to the system entity DATE. However, you can create system-derived entities, such as startdate and enddate, to extract more information from user utterances regarding dates.

For the following example scenario, you're creating a model for booking flights, cars, hotels, and events. You want your intent \#FlightBooking to interpret utterances with your users flight requests. Your model contains the system entity LOCATION, but flight plans usually involve two locations.

In this example procedure, you create two system-derived entities to gather the departure and arrival locations of the flight.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab for your model's application, then the name of your model.

3.  In the model details page, select **Intents**.

4.  Select the name of the intent.

    For this example, you select the **\#FlightBooking** intent.

5.  On the **Utterances** tab, select a word or phrase from one of the utterances.

    In this example scenario, you have an example utterances `book a flight from San Diego to San Francisco`. For this step, click **from San Diego**.

    ![Entity window on the Utterances tab of the Intent details page.](../images/create-derived1.png)

6.  Select **Create New Entity**.

7.  In the Create a new entity screen, configure the fields.

    For this example, use these configurations.

    -   **Entity Name**: Enter `FromLocation`
    -   **Type**: Select **System-derived**
    -   **Model Availability**: Select this check box if you want this entity to be included in all intents in your model
    -   Parent Entity: Select **LOCATION**
    ![Create a new entity window for a system-derived entity.](../images/create-derived2.png)

8.  Select **Save**.

9.  On the same utterance, select another word or phrase.

    In this example scenario, you click **to San Francisco**.

    ![Entity window on the Utterances tab of the Intent details page. Make sure to select the correct part of the utterance.](../images/create-derived3.png)

10. Select **Create New Entity**.

    For this example, use these configurations.

    -   **Entity Name**: Enter `ToLocation`
    -   **Type**: Select **System-derived**
    -   **Model Availability**: Select this check box if you want this entity to be included in all intents in your model
    -   **Parent Entity**: Select **LOCATION**
    ![Create a new entity window for a system-derived entity.](../images/create-derived4.png)

11. Select **Save**.

    **Result:** Your two system-derived entities appear in the entity window.

    ![Entity window for system-derived entities.](../images/create-derived5.png)


## What to do next

Train your model to save the entities. You can try your model to see if it recognizes and interprets variations of the entities that you created.

For this example, you can test your model with a different departure and arrival location.

1.  Select **Try model**.
2.  Enter `book a flight from Dallas to San Jose`.
3.  Select **Go**.

![Intents details page with the test panel open. Train and try your model to assess your new entities.](../images/create-derived6.png "Intents details page with the test panel")

The model predicts the intent, showing the entities it used to determine the values. Notice how it uses both the system entity and system-derived entity when predicting.

**Parent Topic:**[NLU entities](../concept/entities.md)

**Related topics**  


[Create a simple entity](create-nlu-entities.md)

[Create a mapped entity](create-mapped-entity-lookup-source.md)

[Create a pattern entity](create-pattern-entity.md)

[Create an open-ended entity](create-open-ended-entity.md)

[Import entities](import-common-entities-nlu.md)

[Using regular expressions in entities](../concept/using-regular-expressions-nlu.md)

