---
title: Train the classification solution to predict the assignment group
description: Train the Universal Request classification solution definition to identify and predict an assignment group using the short description and create service level tickets that are associated with the universal request.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Predictive Intelligence for Universal Request, Configuring Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Train the classification solution to predict the assignment group

Train the Universal Request classification solution definition to identify and predict an assignment group using the short description and create service level tickets that are associated with the universal request.

## Before you begin

Role required: admin

Ensure that you have installed Predictive Intelligence \(com.glide.platform\_ml\) and Predictive Intelligence for Universal Request \(com.snc.universal\_request.ml\) plugins.

Set the **Enable universal request auto categorization** property to true by navigating to **Universal Request** &gt; **Administration** &gt; **Properties**. Enabling this property enables the application to use the **Universal Request Classification solution** for UR.

![Enable universal request auto categorization property](../images/ur-enable-categorization-property.png)

**Note:** A minimum of ten thousand records are needed to train the classifications.

## Procedure

1.  Navigate to **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  In the Classification Definitions list, search for and select the Universal Request Categorization \(ml\_universal\_request\_categorization\) solution.

3.  On the form, verify the default field values and customize the solution as required.

    For more information about the Classification Definition form fields, see [Create and train classification solution](https://www.servicenow.com/docs/access?context=create-solution-definition&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


**Parent Topic:**[Predictive Intelligence for Universal Request](../concept/predictive-intelligence-ur.md)

