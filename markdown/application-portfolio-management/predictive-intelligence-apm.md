---
title: Predictive Intelligence for Enterprise Architecture \(formerly Application Portfolio Management\)
description: The Predictive Intelligence for Enterprise Architecture uses machine-learning algorithms to predict, suggest, and drive the data outcome of the new application that is onboarded.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Predictive Intelligence for Enterprise Architecture \(formerly Application Portfolio Management\)

The Predictive Intelligence for Enterprise Architecture uses machine-learning algorithms to predict, suggest, and drive the data outcome of the new application that is onboarded.

The application similarity machine-learning solution predicts and suggests the category of the business application when you enter the name and the benefit of the business application in the Register a Business Application form.

Predictive Intelligence for Enterprise Architecture has the following benefits:

-   Uses the data in your instance and hence the suggestions of the machine-learning solution are more accurate.
-   Provides similarity definition for new applications based on the name and description of the existing applications in the Business Application table \[cmdb\_ci\_business\_app\].
-   Suggests categories for the application that you are onboarding to help you sort it into an appropriate category. It is important to categorize an application as it defines its purpose and key business function in the Enterprise Architecture inventory.
-   Enhances the **Register a Business Application** feature offered by [Business Application Lifecycle Management services](business-application-lifecycle-mangmt-svc-cat.md).

## Solution definitions for Predictive Intelligence of Enterprise Architecture

The solution definitions for the predictive intelligence of Enterprise Architecture are available in the Enterprise Architecture – Predictive Intelligence plugin \(com.snc.apm.predictive\_intelligence\). For more information, see [Activate Application Portfolio Management](../task/activate-apm.md).

|Solution Definition|Solution Type|Description|
|-------------------|-------------|-----------|
|Business Application Similarity|Similarity|Predicts the **Category of the business application** field from the **Name of the business application** field and the description provided in the **Benefit of the business application** field.|

## Maintaining prediction accuracy

If your business applications table has more diversified data, then the chances of the machine-learning solution to collect and compare your existing records with new similar records are more. Therefore, the prediction results of categorizing the business application from the name and the description entered by the requester may be more accurate.

You can manage prediction drift by retraining the similarity definition of a business application similarity model provided by the base system. Once your machine-learning solutions are trained, you can call on the Predictive Intelligence API to make a solution prediction.

