---
title: Train the classification solution to predict the assignment group for Ethics Complaint
description: Train the legal request classification solution definition to identify and predict an group assignment using the description and subcategory for an Ethics Complaint.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Predictive intelligence for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Train the classification solution to predict the assignment group for Ethics Complaint

Train the legal request classification solution definition to identify and predict an group assignment using the description and subcategory for an Ethics Complaint.

## Before you begin

Role required: sn\_lg\_pi.admin and platlform\_ml\_read

Ensure that you have installed Predictive Intelligence \(com.glide.platform\_ml\) and Predictive Intelligence for Legal Service Delivery \(sn\_lg\_pi\) plugins.

**Note:** A minimum of ten thousand records are needed to train the classifications.

## Procedure

1.  Navigate to **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  In the Classification Definitions list, search for and select the Ethics Complaints Assignment \(ml\_x\_snc\_sn\_lg\_pi\_global\_ethics\_complaints\_assignment\) solution.

3.  On the form, verify the default field values and customize the solution as required.

    For more information about the Classification Definition form fields, see [Create and train classification solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/create-solution-definition.md).


**Parent Topic:**[Configure Predictive Intelligence for Legal Service Delivery](lsd-PI-configure-landing.md)

