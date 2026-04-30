---
title: Domain separation and Predictive Intelligence Workbench
description: Domain separation is supported in the Predictive Intelligence Workbench application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Predictive Intelligence Workbench
classification: predictive-intelligence-workbench
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ITSM Predictive Intelligence Workbench administration, ITSM Predictive Intelligence Workbench, IT Service Management]
---

# Domain separation and Predictive Intelligence Workbench

Domain separation is supported in the Predictive Intelligence Workbench application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Important:**

Starting with the Xanadu release, ITSM Predictive Intelligence Workbench is being prepared for future deprecation. It will be completed deprecated and will no longer be supported from the **Yokohama** release. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\) plugin. For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md)

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Standard Support level

-   Includes **Basic** level support.
-   Business logic: Processes can be created or modified per customer by the service provider \(SP\). The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The owner of the instance needs to be able to configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

## Domain separation in Predictive Intelligence Workbench - overview

Predictive Intelligence Workbench enables the creation of machine learning models using historic datasets. A machine learning model can be configured in Predictive Intelligence Workbench per domain, which ensures that the data used by the solution is domain-specific data. After a model is trained for a domain, the model calls for a prediction to be made for resolution, depending on what that domain belongs to. For example, the model predicts an incident or case.

## How domain separation works in Predictive Intelligence Workbench

An instance owner can train a machine learning model for each domain by creating a model definition for each domain and training those models. In this way each model uses data specific to the corresponding domain.

-   Data can be domain separated
-   Domain column is present for base system application tables
-   Domain-specific configuration is managed by instance owner
-   Tenant domains can manage their own application data

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

