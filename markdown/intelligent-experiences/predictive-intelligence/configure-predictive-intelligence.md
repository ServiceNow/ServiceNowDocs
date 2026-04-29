---
title: Configure Predictive Intelligence
description: Configure solution definitions for Predictive Intelligence to train, test, and monitor solution definitions
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Predictive Intelligence, Enable AI experiences]
---

# Configure Predictive Intelligence

Configure solution definitions for Predictive Intelligence to train, test, and monitor solution definitions

## Configuration

Use the following links to guide you as you set up your solution definition.

-   **[Database View support for Predictive Intelligence](../concept/database-view-support-predictive-intelligence.md)**  
Use database views to join two or more tables as input for your Machine Learning \(ML\) solution.
-   **[Configuration tips for Predictive Intelligence](../reference/troubleshooting-predictive-intelligence.md)**  
If you encounter issues during your solution training and solution prediction, follow these suggested resolutions.
-   **[Create a custom stopwords list](create-custom-stopwords-list.md)**  
Exclude common words you want the system to ignore during training and prediction.
-   **[Create a word corpus](create-word-corpus.md)**  
Build a collection of words and phrases that functions as the vocabulary the system uses to compare your instance records based on their textual similarity. You can think of the word corpus as a dictionary that you want your machine-learning system to understand.
-   **[Quick start tests for Predictive Intelligence](../../atf-quick-start-tests/reference/quick-start-tests-ai.md)**  
Validate that Predictive Intelligence still works after you make any configuration change such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
-   **[Activate a solution version](activate-solution-version.md)**  
Predictive Intelligence activates the most recent version of the solution when it completes training a solution. However, you can activate any previously trained solution version. Only one solution version can be active at a time, and only the active version is used when making predictions.
-   **[Export trained solutions to production](implement-iterative-solution-updates.md)**  
Refine and test your ML solutions iteratively on a non-production instance, and then use update sets to export the changes to your production instance. This practice mitigates the risk of retraining solutions on your live production instance.
-   **[Configuring advanced settings for your ML solutions](../concept/configuring-advanced-settings-ml-solutions.md)**  
Learn about advanced settings for your Predictive Intelligence machine learning \(ML\) solutions. Apply optional technology and algorithms for classification, clustering, similarity, and regression capabilities.

**Parent Topic:**[Predictive Intelligence](../concept/predictive-intelligence-landing.md)

