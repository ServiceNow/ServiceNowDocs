---
title: Machine learning model setup and behavior
description: Set up models to predict field values and sentiment for customer service cases.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Task Intelligence Admin Console, Task Intelligence for Customer Service, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Machine learning model setup and behavior

Set up models to predict field values and sentiment for customer service cases.

## Training a model

Training a machine learning model is when the model learns patterns in past data to make predictions for new data. Models are trained using a lot of data so that they can learn patterns and the large data set makes the learned patterns statistically significant.

## Setting up a field prediction model

Users with the ml\_admin role can create and train a machine learning model to predict field values from the [Task Intelligence Admin Console](csm-task-intel-admin-center.md).

Using the field prediction model as a starting point, you can choose the training data set that the model learns from. The model can be trained using data from the following tables:

-   Email \[sys\_email\] table
-   Case \[sn\_customerservice\_case\] table
-   Tables that extend the Case table
-   Interaction \[interaction\] table

Models can also be trained using data from email or case attachments.

You then direct the model to learn a pattern between two types of fields from that data:

-   **Output fields** are the fields that you want your model to predict. For example, the Category and Priority fields for cases.
-   **Input fields** are the fields that the model uses as a basis for predictions. For example, text in the subject and body of an email.

You can use the recommended input fields or you can modify these fields and add your own preferences.

If the model is configured to use text from attachments, the system performs the following steps when a case or interaction is created:

-   The system checks the record for attachments with supported content types and file extensions. It ignores the attachments that have unsupported file extensions.
-   If the record has attachments in a supported format, the system parses the text and sends it as an input to the categorization model, along with text from the input fields.
-   If the record does not have attachments, or no attachments in a supported format, the system sends text from the input fields to the categorization model.

Supported content types and file extensions are stored in the **sn\_csm\_ml\_task.categorization.allowed\_content\_types** system property. For more information, see [Components installed with Task Intelligence for Customer Service](../reference/case-categorization-components.md#section_bqd_lqt_xrb).

## Supporting multiple languages

Categorization supports multiple languages including attachments, if the models are configured to include attachments. The categorization model returns the predicted language and stores it in the **Detected Language** field in the Predictor Result \[ml\_predictor\_results\] table.

## Setting up a case sentiment model

The case sentiment model is pre-trained with a large data set to learn communication patterns. This data comes from customer emails and case descriptions and comments and reflects typical communication between agents and customers.

-   **Email**: The model uses the text in the subject and body of the initial email to predict sentiment when the case is created. Text from the body of subsequent emails is used to update the prediction.
-   **Cases**: The model uses the text in the case short description and description to predict sentiment when the case is created. Comments added to the case are used to update the prediction.

The case sentiment model supports case types. When setting up a sentiment model, you select the table on which to run sentiment analysis. You can select:

-   The Case table
-   Tables that extend the Case table

**Note:** The sentiment analysis feature supports one level of custom extension from the Case table.

**Parent Topic:**[Task Intelligence Admin Console](csm-task-intel-admin-center.md)

