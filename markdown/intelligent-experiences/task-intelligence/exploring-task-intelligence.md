---
title: Exploring Task Intelligence
description: Learn more about Task Intelligence and how machine learning models can learn from your data to make predictions and achieve important outcomes.
locale: en-US
release: yokohama
product: Task Intelligence
classification: task-intelligence
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Task Intelligence, Enable AI experiences]
---

# Exploring Task Intelligence

Learn more about Task Intelligence and how machine learning models can learn from your data to make predictions and achieve important outcomes.

## Task Intelligence overview

With Task Intelligence, you can easily set up machine learning solutions that interact with your data. Then, track how the solutions are impacting creation, deflection, triage, remediation, and optimization moments. With automated task creation, triage, and investigation, agents spend less time receiving and preparing information, so tasks can proceed faster. These models can help you work more efficiently, helping to lower the mean time to resolve \(MTTR\) of tasks.

With Task Intelligence, agents:

-   Solve issues faster for better service and experiences
-   Focus  on  meaningful, high-value work
-   Reduce  error  rates  and  drive down  costs
-   Improve time to value with intuitive experiences

![GIF of the Admin Console.](../images/setup-screen.png)

The Admin Console supports the following model types:

<table id="table_bgj_1fc_f5b"><thead><tr><th>

Model

</th><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incident field prediction

</td><td>

[Task Intelligence for ITSM](https://www.servicenow.com/docs/access?context=c-itsm-task-intelligence&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)

</td><td>

[Create an incident field prediction model](https://www.servicenow.com/docs/access?context=create-incident-prediction-model&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)

</td></tr><tr><td>

Similarity model management

</td><td>

[Task Intelligence for ITSM](https://www.servicenow.com/docs/access?context=c-itsm-task-intelligence&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)

</td><td>

[Create a similar records prediction model in Task Intelligence for ITSM](https://www.servicenow.com/docs/access?context=create-a-similar-records-model-in-task-intelligence-for-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)

</td></tr><tr><td>

Case field prediction

</td><td>

[Task Intelligence for CSM](https://www.servicenow.com/docs/access?context=csm-task-intelligence&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)

</td><td>

Predicts output fields on case forms, including categorization.

 [Record categorization](https://www.servicenow.com/docs/access?context=case-categorization-overview&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)

</td></tr><tr><td>

Sentiment prediction

</td><td>

[Task Intelligence for CSM](https://www.servicenow.com/docs/access?context=csm-task-intelligence&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)

</td><td>

Predicts current and trending user sentiment.

 **Note:** Model is pre-trained but can be tested and edited. Only one sentiment model can be configured.

</td></tr><tr><td>

Language detection

</td><td>

[Task Intelligence for CSM](https://www.servicenow.com/docs/access?context=csm-task-intelligence&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)

</td><td>

Detects language which language is being used.

 **Note:** Model is pre-trained but can be tested and edited. Only one language detection model can be configured.

</td></tr></tbody>
</table>## Task Intelligence workflow

The Task Intelligence Admin Console uses machine learning models. The models are statistical and can predict future data by training with your past data.

With the Admin Console, create, configure, train, test, and deploy predictive models used for automation in other ServiceNow features and applications, such as Customer Service Management \(CSM\).

Training a machine learning model is when the model learns patterns in past data to make predictions for new data. Models are trained using a lot of data so that they can learn patterns and the large data set makes the learned patterns statistically significant. By answering questions about your information systems, business process, and service operations, the system actively learns from your responses.

## Task Intelligence benefits

The Task Intelligence Admin Console provides admins with a no-code experience for deploying Task Intelligence solutions. The seamless experience helps you automate and optimize task creation, deflection, triaging, and resolution.

Features are implemented by two applications: [Task Intelligence for Customer Service](https://www.servicenow.com/docs/access?context=csm-task-intelligence&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) and [Task Intelligence for ITSM](https://www.servicenow.com/docs/access?context=c-itsm-task-intelligence&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

|Benefit|Feature|Users|
|-------|-------|-----|
|Predict form field values to auto-populate or recommend as suggestions|Create a field prediction model|Admins, agents|
|Categorize emails and cases based on language and attachment content|[Record categorization](https://www.servicenow.com/docs/access?context=case-categorization-overview&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)|Agents|
|Predict incident category and priority based on previous incidents to lower time to resolution|Create an incident prediction model|Agents|
|Analyze initial and ongoing sentiment during customer service cases|[Sentiment Analysis](https://www.servicenow.com/docs/access?context=case-sentiment-analysis&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)|Agents|
|Identify the language used to create customer service cases|[Language detection](https://www.servicenow.com/docs/access?context=case-language-detection&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)|Agents|
|Analyze and assess the performance of models|Task Intelligence Analytics and Monitoring|Admins|

