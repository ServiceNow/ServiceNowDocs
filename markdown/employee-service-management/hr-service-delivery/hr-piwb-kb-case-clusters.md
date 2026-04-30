---
title: HR PIWB template: Predict knowledge case clusters and demand insights
description: Use the classic setup template to configure and train your Cluster solution template with machine learning model to predict the case clusters that do not have knowledge, identify knowledge demand, and improve the knowledge articles.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [HR Predictive Intelligence Workbench implementation, HR Predictive Intelligence Workbench, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# HR PIWB template: Predict knowledge case clusters and demand insights

Use the classic setup template to configure and train your Cluster solution template with machine learning model to predict the case clusters that do not have knowledge, identify knowledge demand, and improve the knowledge articles.

## Before you begin

Role required: sn\_piwb\_hr\_content.admin

## About this task

This template helps customizing a use case model to configure the Knowledge Demand Insights feature to identify which topics are missing knowledge articles and create actionable knowledge gaps for missing topics. Review the information from [Configure Knowledge Demand Insights](https://www.servicenow.com/docs/access?context=configure-demand-insights&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence Workbench** &gt; **Use Cases** &gt; **Create New from Templates**.

2.  From the templates list, go to **Knowledge demand for HR case clusters** template and click **Start**.

    A pop-up with model name appears. This use case is handled in the classic Predictive Intelligence. You will be taken there to complete setup. You can perform the following steps:

    1.  Ensure you click **View product documentation for setting up this use case** to review the instructions on how to configure the solution definition.

        **Note:** Ensure you review and understand the documentation for creating the solution definition.

    2.  Click **Take me there** to get started with the solution definition.
    Machine Learning Solutions landing page appears.

    ![List of ML usecases for HR PIWB](../image/piwb-hr-ml-list.png "HR ML use cases")

3.  Review the information from [Configure Knowledge Demand Insights](https://www.servicenow.com/docs/access?context=configure-demand-insights&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

4.  Go to **Clustering** &gt; **Knowledge demand for HR case clusters** from the available Solution Definitions, click **Configure**.

    The solution definition appears.

5.  On the form, verify the default field values and customize the solution as required.


## Result

You can use a demand insights for knowledge gap analysis and create actionable knowledge articles for missing topics.

Review the corresponding use case information from [Machine learning solutions for HR Service Delivery](../concept/predictive-intelligence-for-hr-service-delivery-1.md).

## What to do next

You can verify the integration status from **HR Administration** &gt; **HR AI Configurations** &gt; **Solution definition**. The use case is now mapped to the selected solution definition.

**Parent Topic:**[HR Predictive Intelligence Workbench implementation](../concept/hr-piwb-implementation-guidance.md)

**Related topics**  


[Create and train a similarity solution](https://www.servicenow.com/docs/access?context=create-similarity-solution&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

[Create and train a clustering solution](https://www.servicenow.com/docs/access?context=create-clustering-solution&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

