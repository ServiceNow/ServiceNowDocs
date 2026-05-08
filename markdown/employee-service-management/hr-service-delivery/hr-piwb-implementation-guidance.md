---
title: HR Predictive Intelligence Workbench implementation
description: You can use machine learning to optimize your business processes. You can train and implement HR Predictive Intelligence Workbench use cases to augment your existing application workflows.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [HR Predictive Intelligence Workbench, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# HR Predictive Intelligence Workbench implementation

You can use machine learning to optimize your business processes. You can train and implement HR Predictive Intelligence Workbench use cases to augment your existing application workflows.

## Explore common use case templates

With the sn\_piwb\_hr\_content.admin role, you can explore the use case templates and create predictive machine learning models. To create a machine learning model, you first select a pre-built use case template. You can use one of the following templates for setting up the use cases.

-   **Guided** templates include a comprehensive setup process to help you through implementation. Templates with available auto-trained models accelerate your setup process, by providing a pre-generated model based on your data.
-   **Classic** templates include a comprehensive setup information to help you through implementation. Leverage the existing templates to configure, test, and train the models based on your business requirements.

When a template indicates **Auto-trained model available**, this means you can go directly to the evaluation phase of the use case setup. If the auto-trained model is acceptable, you can directly integrate the model with your business processes. Otherwise, you can tune this model or create another model. You may change the name and description of the use case later.

## Solution definitions

These solution definitions are available as templates on instances where both Predictive Intelligence and HR are active. Create your own solution definition records to customize the behavior.

|Solution Type|Solution Definition|Description|Implementation|
|-------------|-------------------|-----------|--------------|
|Classification|Predict the HR service for incoming cases|Predicts the correct HR service for cases.|Guided|
|Classification|Predict the assignment group for incoming cases|Predicts the correct assignment group for cases.|Guided|
|Classification|Email Case Categorization|Auto-categorizes the HR service for the email cases for improved productivity by saving time and costs.|Guided|
|Similarity|Similar Closed HR Cases|Recommends similar cases closed in the past to assist an HR agent for faster and better resolution.|Classic|
|Similarity|User profile based recommendation|Recommends top 3 relevant articles and catalog items based on users with a similar profile for content discovery and personalized experience.|Classic|
|Similarity|Similar HR Cases and knowledge|Automates the discovery of knowledge gaps in your knowledge bases and recommends insights into improving knowledge that is driven by demand.|Classic|
|Similarity|Similar Knowledge Articles for HR Task|Displays related articles to assist employees in completing the HR or Content or Campaign to-dos.|Classic|
|Similarity|Similar Knowledge Articles for HR Case|Uses ML to identify the most relevant knowledge articles to assist an HR agent for faster and better resolution.|Classic|
|Regression|HR Case Resolution Time|Determines the resolution time expected a case by analyzing similar closed cases in past for better visibility and transparency.|Classic|
|Clustering|Demand Insights: HR Case Clusters Need Knowledge|Identifies the case clusters that do not have knowledge and helps with filling the knowledge gaps in your knowledge base.|Classic|

## Use case creation phases

Creating a predictive machine learning model involves several phases. After you create and train your model, evaluate and tune, test prediction results, and integrate the model with your business process. Use case model creation phases include:

-   **Create and train models:** Define parameters to create a model that you train based on your unique data. Create multiple models as you tune and refine your models by defining the right combination of coverage and precision to use.
-   **Test your models:** Get prediction results from your models to decide which one is best to integrate with your business process. To see if a model returns a correct result, you can use either the single or batch testing process.
-   **Integrate the best model:** Deploy the best model into your business process. After you determine which model returns the best, correct result, integrate it into production.

## Prediction accuracy maintenance

You can manage prediction drift by retraining, modifying, or creating new solutions to reflect changes in your business conditions. Test and modify your business rule over time to ensure it works as desired across multiple consumption points and user persona.

-   **[HR PIWB template: Auto-categorize email cases](../task/hr-piwb-email-categorization.md)**  
Use a guided template that walks you through setting up a machine learning model to categorize the email cases automatically for improved productivity and cost savings.
-   **[HR PIWB template: Predict the HR service for incoming cases](../task/hr-piwb-predict-hrservice.md)**  
Use a guided template that walks you through setting up a machine learning model to predict the correct HR service for cases.
-   **[HR PIWB template: Predict the assignment group for incoming cases](../task/hr-piwb-predict-ag.md)**  
Use a guided template that walks you through setting up a machine learning model to predict the correct assignment group for cases.
-   **[HR PIWB template: Predict knowledge case clusters and demand insights](../task/hr-piwb-kb-case-clusters.md)**  
Use the classic setup template to configure and train your Cluster solution template with machine learning model to predict the case clusters that do not have knowledge, identify knowledge demand, and improve the knowledge articles.
-   **[HR PIWB template: Predict knowledge gaps and insights](../task/hr-piwb-kb-gaps-insights.md)**  
Use the classic template that walks you through setting up a machine learning model to automate the discovery of knowledge gaps and recommend insights into improving knowledge by demand.
-   **[HR PIWB template: Predict knowledge for HR case resolution](../task/hr-piwb-similar-hrcases-agent.md)**  
Use the classic setup template to configure and train your Similarity solution template with machine learning model to recommend knowledge articles to assist an HR agent for faster case resolution.
-   **[HR PIWB template: Recommend similar cases by employee profile](../task/hr-piwb-similar-profile.md)**  
Use the classic setup template to configure and train your Similarity solution template with machine learning model to recommend top relevant articles and catalog items based on a similar employee profile for content discovery and personalized experience.
-   **[HR PIWB template: Predict knowledge for HR task completion](../task/hr-piwb-similar-hrtasks-employee.md)**  
Use the classic setup template to configure and train your Similarity solution template with machine learning model to recommend knowledge articles for employees to complete the HR tasks.
-   **[HR PIWB template: Recommend similar cases](../task/hr-piwb-similar-cases.md)**  
Use the classic setup template to configure and train your Similarity solution template with machine learning model to recommend similar closed HR cases.
-   **[HR PIWB template: Recommend estimated time to resolve](../task/hr-piwb-ettr.md)**  
Train your solution by using historical data to predict numeric outputs based on the historic data. Configure the solution definition to predict the estimated time to resolve a HR case.

**Parent Topic:**[HR Predictive Intelligence Workbench](hr-predictive-intelligence-wb.md)

**Related topics**  


[bundle-platai.predictive-intelligence]

[bundle-platai.get-started-predictive-intelligence]

