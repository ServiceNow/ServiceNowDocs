---
title: Predictive Intelligence frameworks
description: Predictive Intelligence provides three different model frameworks in the Yokohama release: classification, similarity, and clustering. Each framework specializes in different types of predictions.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Explore Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Predictive Intelligence frameworks

Predictive Intelligence provides three different model frameworks in the Yokohama release: classification, similarity, and clustering. Each framework specializes in different types of predictions.

## Predictive Intelligence classification framework

The Predictive Intelligence classification framework enables you to use machine-learning algorithms to set categorical field values during record creation. For example, you can use the model to set the incident category based on the short description. You can train predictive models so they act as an agent to categorize and route work automatically based on your past record-handling experience.

Enable Predictive Intelligence to handle volumes of incoming requests at lower costs. Automate the categorization and assignment of requests to reduce:

-   Task resolution times.
-   The number of interactions required to resolve tasks.
-   The error rates of categorizing and assigning work.

For more information, see [Create and train a classification solution](../task/create-solution-definition.md).

## Predictive Intelligence similarity framework

The Predictive Intelligence similarity framework identifies existing records that have similar values to a new record. For example, you can train a subset of your incident records to recommend a resolution based on the information of a similar incident record. By borrowing from similar closed incidents that have a proven resolution, you can help agents and fulfillers quickly provide the best resolution for an incoming incident.

The similarity framework doesn't need an exact match of keywords for its text comparisons because its algorithms identify similar words and synonyms based on similar contexts. For example, the phrases printer not working and printer broken are both recognized as similar. The framework also collects, learns, and applies your industry-specific context. For example, the phrase unable to join network has a different context in a computer networking company than it does in a healthcare insurance company.

The similarity framework uses a workflow similarity solution. For more information, see [Create and train a similarity solution](../task/create-similarity-solution.md).

## Predictive Intelligence clustering framework

Clustering divides data into groups that can then be used to identify patterns. You can then address records collectively or find gaps in existing data. For example, you can group similar new incidents to identify a major outage.

The clustering framework uses a workflow clustering solution. For more information, see [Create and train a clustering solution](../task/create-clustering-solution.md).

## Deprecated in the Washington DC release: Predictive Intelligence regression framework

**Important:** Support for creating new regression solutions was removed in the Washington DC release. You can train and edit existing solutions, but you can't create new ones. This information is provided for legacy context.

Regression is a machine-learning framework that uses historic data to predict numeric outputs, such as a temperature or a stock price.

For more information, see [Create and train a regression solution](../task/create-regression-solution.md).

**Parent Topic:**[Explore Predictive Intelligence](predictive-intelligence.md)

**Related topics**  


[ServiceNow apps and features that use Predictive Intelligence](servicenow-apps-features-use-predictive-intelligence.md)

