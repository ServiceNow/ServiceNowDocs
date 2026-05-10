---
title: HR PIWB template: Recommend similar cases by employee profile
description: Use the classic setup template to configure and train your Similarity solution template with machine learning model to recommend top relevant articles and catalog items based on a similar employee profile for content discovery and personalized experience.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HR Predictive Intelligence Workbench implementation, HR Predictive Intelligence Workbench, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# HR PIWB template: Recommend similar cases by employee profile

Use the classic setup template to configure and train your Similarity solution template with machine learning model to recommend top relevant articles and catalog items based on a similar employee profile for content discovery and personalized experience.

## Before you begin

Role required: sn\_piwb\_hr\_content.admin

## About this task

Discover all the users who have a similar profile as the employee. Identify the top viewed knowledge articles and top submitted catalog items by those users.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence Workbench** &gt; **Use Cases** &gt; **Create New from Templates**.

2.  From the templates list, go to **Employee profile based recommendation** template and click **Start**.

    A pop-up with model name appears. This use case is handled in the classic Predictive Intelligence. You will be taken there to complete setup. You can perform the following steps:

    1.  Ensure you click **View product documentation for setting up this use case** to review the instructions on how to configure the solution definition.

        **Note:** Ensure you review and understand the documentation for creating the solution definition.

    2.  Click **Take me there** to get started with the solution definition.
    Machine Learning Solutions landing page appears.

    ![List of ML usecases for HR PIWB](../image/piwb-hr-ml-list.png "HR ML use cases")

3.  Go to **Similarity** and click **Configure**.

    The solution definition section appears.

4.  On the form, verify the default field values and customize the solution as required.

    For more information about the Clustering solution definition form fields, see [Create and train a clustering solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/create-clustering-solution.md) and [Test a classification solution prediction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/test-solution-prediction.md).

    **Note:** For details regarding trained use case integration implementation, see Predictive Intelligence Workbench integration and customization.


## Result

When the configuration is complete, the solution displays the top three knowledge articles and top three catalog items to the employee based on a similar employee profile. For more information, see [Discovering knowledge articles and catalog items for employees](../concept/user-profile-based-recommendations.md).

## What to do next

You can verify the integration status from **HR Administration** &gt; **HR AI Configurations** &gt; **Solution definition**. The use case is now mapped to the selected solution definition.

**Parent Topic:**[HR Predictive Intelligence Workbench implementation](../concept/hr-piwb-implementation-guidance.md)

**Related topics**  


[Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/predictive-intelligence.md)

[Get started with Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/install-predictive-intelligence.md)

