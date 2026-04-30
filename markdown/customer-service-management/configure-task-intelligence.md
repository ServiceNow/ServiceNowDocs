---
title: Configure Task Intelligence for Customer Service
description: Install the Task Intelligence for Customer Service application and configure the different features: record categorization, language detection, Sentiment Analysis, and Document Intelligence for Customer Service.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Task Intelligence for Customer Service, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Configure Task Intelligence for Customer Service

Install the Task Intelligence for Customer Service application and configure the different features: record categorization, language detection, Sentiment Analysis, and Document Intelligence for Customer Service.

## Install and configure Task Intelligence features

Complete the following tasks to install Task Intelligence for Customer Service and configure the features.

|Task|Description|
|----|-----------|
|[Install the Task Intelligence for Customer Service application](../task/install-task-intelligence-cs-app.md)|You can install the Task Intelligence for Customer Service application \(com.snc.csm\_ml\_task\) if you have the admin role.|
|[Configure record categorization](case-categorization-configure.md)|Activate the required plugins and import training data. Then you can create and train a model to predict field values.|
|[Configure Sentiment Analysis](case-sentiment-analysis-configure.md)|Activate the required plugins, enable the sentiment analysis property, and assign roles. Then you can train a model to predict case sentiment.|
|[Configure language detection](case-language-detection-configure.md)|Activate the required plugins and the ServiceNow translator to use the language detection feature. Then you can set up a model to detect the case language.|
|[Configure Document Intelligence for Customer Service](csm-doc-intel-configuring-.md)|Enable Document Intelligence for Customer Service and create use cases to extract data.|

## Set up and deploy Task Intelligence models

Once you have completed the configuration tasks, you can use the Task Intelligence Admin Console to set up and deploy models for record categorization, sentiment analysis, and language detection. You can also use the Task Intelligence Admin Console to access the Document Intelligence Admin interface, which you can use to create document processing use cases.

<table id="table_ang_qtp_fvb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Create a model to predict record fields](csm-task-intel-create-cat-solution.md)

</td><td>

Create and train a model to predict fields for cases and interactions.

</td></tr><tr><td>

[Create a model to predict case sentiment](csm-task-intel-create-sentiment-solution.md)

</td><td>

Edit and test the pre-trained sentiment model to predict sentiment for customer service cases.

</td></tr><tr><td>

[Create a model to detect case language](csm-task-intel-create-language-solution.md)

</td><td>

Edit and test the pre-trained model to detect the language used to create customer service cases.

</td></tr><tr><td>

[Create a Document Intelligence use case](csm-task-intel-create-di-use-case.md)

</td><td>

Create a use case to identify the information to extract from email and case attachments.

</td></tr><tr><td>

[Create a model to predict similar cases](create-a-model-to-predict-similar-cases.md)

</td><td>

Test and edit the pre-trained similar cases model for predicting similarity in customer service cases and create a new model for custom cases.

</td></tr><tr><td>

[Edit a model](../task/edit-a-case-prediction-model.md)

</td><td>

Edit the case models that have already been trained and deployed. Change the model configurations, view the updated training results, and redeploy the model.

</td></tr><tr><td>

[Export a model](../task/export-a-task-intelligence-model.md)

</td><td>

Export a Task Intelligence model to another instance.

</td></tr><tr><td>

[Create a custom similar case model](create-a-custom-similar-case-model.md)

</td><td>

Set up a training model to help it recognize similarities between two types of tables by comparing their fields.

 The model looks at the prediction fields of a prediction table and the training fields of a training table. It uses the similarities in these fields to predict similar records.

</td></tr></tbody>
</table>**Related topics**  


[Task Intelligence for Customer Service](csm-task-intelligence.md)

[Use Task Intelligence for Customer Service](use-task-intelligence.md)

