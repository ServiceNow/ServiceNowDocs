---
title: Train the similarity solution for similar closed Universal Requests
description: Train the Similar Closed Universal Request solution definition to identify and predict similar Universal Requests that are closed based on the short description, description, and the assignment group of the Universal Request created. When an agent opens a universal request, similar closed universal requests can be searched in the Related Search section of the Universal Request record.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Predictive Intelligence for Universal Request, Configuring Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Train the similarity solution for similar closed Universal Requests

Train the Similar Closed Universal Request solution definition to identify and predict similar Universal Requests that are closed based on the short description, description, and the assignment group of the Universal Request created. When an agent opens a universal request, similar closed universal requests can be searched in the Related Search section of the Universal Request record.

## Before you begin

Role required: admin or sn\_un\_req.ur\_admin

Ensure that you have installed Predictive Intelligence \(com.glide.platform\_ml\) and Predictive Intelligence for \(com.snc.universal\_request.ml\) plugins are activated.

This solution is available only if you enable the **Enable to view similar closed Universal Request recommendations** \(sn\_uni\_req.similar\_closed\_universal\_request\) property. For more information on this property, see [Universal Request properties](../reference/ur-properties.md).

**Note:** A minimum of ten thousand records are needed to train the classifications.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  In the Similarity Definitions list, search for and select the Similar Closed Universal Request \(ml\_x\_snc\_sn\_uni\_req\_global\_similar\_closed\_universal\_request\) solution.

3.  On the form, verify the default field values and customize the solution as required.

    For more information about the Similarity Definition form fields, see [Create and train a similarity solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/create-similarity-solution.md).


**Parent Topic:**[Predictive Intelligence for Universal Request](../concept/predictive-intelligence-ur.md)

