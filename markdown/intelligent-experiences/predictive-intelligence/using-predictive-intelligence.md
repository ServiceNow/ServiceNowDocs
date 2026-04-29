---
title: Using Predictive Intelligence
description: Train and use Predictive Intelligence solutions to accomplish various tasks and that integrate with other ServiceNow products, such as Document Intelligence and Task Intelligence.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Predictive Intelligence, Enable AI experiences]
---

# Using Predictive Intelligence

Train and use Predictive Intelligence solutions to accomplish various tasks and that integrate with other ServiceNow products, such as Document Intelligence and Task Intelligence.

## Overview of Predictive Intelligence

Predictive Intelligence is the interface by which you can train models on the ServiceNow AI Platform. These models enable you to predict, estimate, and identify patterns that can be used to route work, populate form fields, estimate wait times, and more.

-   Show suggestions for relevant articles.
-   Assign, categorize, and prioritize tasks.
-   Detect major incidents.
-   Recommend case resolutions.
-   Prevent duplicate articles and ideas.
-   Detect phishing attempts.

For more information about the different types of solutions available, see [Explore Predictive Intelligence](predictive-intelligence.md).

## Training your ML solutions

Predictive Intelligence enables you to train predictive models and machine-learning solutions that you can apply using data on your instances. The solutions you create use the frameworks to predict, recommend, and organize data. To get started, see [Creating and training solutions](training-ml-solutions.md).

You can also extend Predictive Intelligence to other processes and applications, such as:

-   Incident categorization: Predicts the incident category based on the short description. See [Predictive Intelligence for Incident Management](https://www.servicenow.com/docs/access?context=predictive-intelligence-for-incident&version=australia&pubname=australia-it-service-management&ft:locale=en-US).
-   CSM case assignment: Predicts the case record assignment group based on the short description. See [Predictive Intelligence for case management](https://www.servicenow.com/docs/access?context=agent-intelligence-case-mgmt&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

For more information, see [ServiceNow apps and features that use Predictive Intelligence](servicenow-apps-features-use-predictive-intelligence.md).

## Testing and monitoring predictions

After creating and training your solutions, call on the Predictive Intelligence API to make a solution prediction. Use the results to gauge the performance of the solution and make changes as needed.

You can track the coverage and precision of deployed predictive models using the Solution Statistics dashboard, which provides reporting on these prediction areas by default.

|Report|Description|
|------|-----------|
|Average Prediction Coverage \(last 30 days\)|The percentage of predictions that yielded an outcome out of the total number of predictions attempted. Click the coverage score to see a breakdown by class.|
|Daily Prediction Coverage|The percentage of records created on a given day in which the solution was able to predict an outcome.|
|Average Prediction Precision \(last 30 days\)|The percentage of predictions in which the predicted value was the same as the final value of the field when the record closed. Click the precision score to see a breakdown by class.|
|Daily Prediction Precision|The percentage of records closed on a given day in which the predicted field value was the same as the final value.|

For more information, see [Testing and monitoring predictions](testing-reviewing-ml-solutions.md).

## Preparing your instance

For you to get the most out of Predictive Intelligence, you will want to prepare. You don't need to write code or do calculations, but deciding what you hope to do with the solution definitions will make implementation easier.

-   Identify the problems that you want to solve with Predictive Intelligence.
-   Have 30,000–300,000 high-quality records from which Predictive Intelligence can learn.
-   Set your expectations.

**Note:** Inconsistencies or gaps in training data can cause incorrect or unreliable predictions.

## Implementation Process

Predictive Intelligence takes approximately 14 days to implement on a production instance.

-   Day 1: Clone production instance over to a non-production instance.
-   Days 2–10: Create a solution definition, train it on historical records, and validate that the solution works as desired on the non-production instance.
-   Days 11–13: Create import and update sets to move the solution to production, train and validate on the new instance, and set the retraining frequency.
-   Day 14 and on: Monitor the solution.

In general, non-production environments are where workflows can be tested and formatted before being moved over to the production instance to further train models and test predictions.

For more information about getting started with Predictive Intelligence, see [our guide on how to get started with Predictive Intelligence](../task/install-predictive-intelligence.md#).

