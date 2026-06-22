---
title: Predictive Intelligence for case management
description: Assist agents with case creation by requiring a minimum of information, such as the short description, and predicting values for the category, priority, and assignment group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/agent-intelligence-case-mgmt.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Predictive Intelligence for case management

Assist agents with case creation by requiring a minimum of information, such as the short description, and predicting values for the category, priority, and assignment group.

From either Agent Workspace or the platform interface, agents can use this feature when creating cases by providing the short description. Based on the information entered in the **Short description** field, the [Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/predictive-intelligence/predictive-intelligence.md) feature predicts the category, priority, and assignment group, and routes the case to the correct queue.

## Plugin

The Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\) provides Predictive Intelligence capabilities for Customer Service Management. This plugin enables customers to leverage machine learning algorithms for searching related cases in CSM. This plugin requires:

-   Customer Service \(com.sn\_customerservice\)
-   Predictive Intelligence for Contextual Search \(com.snc.contextual\_search\_ml\)

The Predictive Intelligence for Customer Service Management plugin is activated automatically for new Orlando customers. Existing customers upgrading to the Orlando release must manually activate this plugin.

## Solution definitions

Predictive Intelligence includes the following solution definitions for case management:

-   CSM Case Categorization
-   CSM Case Assignment
-   CSM Case Prioritization

A solution definition predicts one or more output fields based on a configured input field. At least one solution definition must be active to use Predictive Intelligence with Customer Service Management.

For more information, see [Predictive Intelligence for CSM solution definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/predictive-intelligence-for-csm.md).

## Business rules

Predictive Intelligence also includes business rules for Customer Service Management:

-   Default Case Based Prediction
-   Update Prediction Results

For more information, see [Predictive Intelligence for CSM solution definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/predictive-intelligence-for-csm.md).

## Extension points

The Predictive Intelligence feature for Customer Service Management includes the **CSMPredictionService** extension point. This extension point contains a method that returns the following information:

-   The list of solution definitions that are used to predict field values during case creation.
-   The treatment of the predicted fields based on the values of the input fields.

The system administrator can use this extension point to customize the solution definitions.

