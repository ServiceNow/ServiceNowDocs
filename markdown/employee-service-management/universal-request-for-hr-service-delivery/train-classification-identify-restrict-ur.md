---
title: Train the classification solution to identify UR with sensitive information
description: Train the Universal Request classification solution definition to identify and predict universal request with sensitive information using the short description and description. The solution identifies and marks the UR as restricted, allowing only agents with access or from the assignment group to work on the request.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Predictive Intelligence for Universal Request, Configuring Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Train the classification solution to identify UR with sensitive information

Train the Universal Request classification solution definition to identify and predict universal request with sensitive information using the short description and description. The solution identifies and marks the UR as restricted, allowing only agents with access or from the assignment group to work on the request.

## Before you begin

Role required: admin

Ensure that you have installed Predictive Intelligence \(com.glide.platform\_ml\) and Predictive Intelligence for \(com.snc.universal\_request.ml\) plugins are activated.

Set the **Enable to auto-restrict requests with sensitive information** property to true by navigating to **Universal Request** &gt; **Administration** &gt; **Properties**. Enabling this property enables the application to use the **Universal Request Classification solution** for UR.

**Note:** A minimum of ten thousand records are needed to train the classifications.

## Procedure

1.  Navigate to **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  In the Similarity Definitions list, search for and select the UR Sensitive Classification \(ml\_sn\_sn\_uni\_req\_ml\_global\_ur\_sensitive\_classification\) solution.

3.  On the form, verify the default field values and customize the solution as required.

    For more information about the Classification Definition form fields, see [Create and train classification solution](https://www.servicenow.com/docs/access?context=create-solution-definition&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


**Parent Topic:**[Predictive Intelligence for Universal Request](../concept/predictive-intelligence-ur.md)

