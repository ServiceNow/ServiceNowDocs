---
title: Solution definitions and business rules for Predictive Intelligence for Legal Service Delivery
description: Solution definitions and business rules are defined to train, test, and monitor the predictive intelligence solution.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Predictive intelligence for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Solution definitions and business rules for Predictive Intelligence for Legal Service Delivery

Solution definitions and business rules are defined to train, test, and monitor the predictive intelligence solution.

## Solution definitions

The solution definition for Predictive Intelligence for Legal Service Delivery is available when you activate Predictive Intelligence plugin \(com.glide.platform\_ml\) and Predictive Intelligence for Legal Service Delivery \(sn\_lg\_pi\) plugin. You can customize the solution definition to meet your business requirements.

You can also create and train machine-learning solutions as per your requirement. For more information, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

The following solution definitions are available in the base system. You can access the solution definition by navigating to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

**Note:** The solutions definitions in the base system are not trained. You need to train them on your instance before using them.

|Solution Type|Solution Definition|Description|
|-------------|-------------------|-----------|
|Classification|Legal Request Sub-categorization|Predicts the subcategory for general legal request based on short description and description.|
|Classification|Ethics Complaints Sub-categorization|Predicts the subcategory for ethic complaints based on description.|
|Classification|Legal Request Assignment|Predicts the assignment group for general legal request based on short description, description, and subcategory.|
|Classification|Ethics Complaints Assignment|Predicts the assignment group for ethic complaints based on description and subcategory.|

## Use cases

The following use cases are available in the base system. You can access use cases by navigating to **All** &gt; **Legal Administration** &gt; **Legal AI Configurations**.

|Use case|Description|
|--------|-----------|
|Legal Request Assignment|Predicts the assignment group for general legal request based on short description, description, and subcategory.|
|Legal Request Sub-categorization|Predicts the subcategory for general legal request based on short description and description.|
|Ethics Complaints Assignment|Predicts the assignment group for ethic complaints based on description and subcategory.|
|Ethics Complaints Sub-categorization|Predicts the subcategory for ethic complaints based on description.|

## Business rules

The business rule triggers the predictive intelligence to predict the assignment group and sub categorization. The following business rules are available in the base system. To complete the solution definition and use cases available in the base system, create a business rule for Ethics Complaints.

You can create your own solution for any fields based on your requirement. For any solution definition defined, create a corresponding business rule.

|Solution Definition|Description|
|-------------------|-----------|
|Predict legal request assignment group|Predicts the assignment group for general legal request based on short description, description, and subcategory.|
|Predict legal request subcategory|Predicts the subcategory for general legal request based on short description and description.|

