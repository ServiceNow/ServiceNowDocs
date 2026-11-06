---
title: Predictive Intelligence for Incident Management
description: Use your instance records to build classification and similarity solutions for Incident Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/predictive-intelligence-for-incident.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Machine learning solutions for IT Service Management, IT Service Management]
---

# Predictive Intelligence for Incident Management

Use your instance records to build classification and similarity solutions for Incident Management.

## Solution definitions

These solution definitions are available as templates on instances where both Predictive Intelligence and Incident Management are active. Create your own solution definition records to customize the behavior.

<table id="table_bdh_nzs_kbb"><thead><tr><th>

Solution definition

</th><th>

Solution type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incident Assignment

</td><td>

Classification

</td><td>

Predicts the **Assignment group** field from the **Short description**.

</td></tr><tr><td>

Incident Categorization

</td><td>

Classification

</td><td>

Predicts the **Category** field from the **Short description**.

</td></tr><tr><td>

Incident Service

</td><td>

Classification

</td><td>

Predicts the **Service** field from the **Short description**.

</td></tr><tr><td>

Incident Configuration Item

</td><td>

Classification

</td><td>

Predicts the **Configuration item** field from the **Short description**.

</td></tr><tr><td>

Major Incident Detection

</td><td>

Similarity

</td><td>

Recommends similar active major incidents that the current incident can be linked to.

 Recommends similar incidents to propose a major incident.

</td></tr><tr><td>

Similar Incidents \(Major Incident Workbench\)

</td><td>

Similarity

</td><td>

Recommends similar incidents that are not linked as child incidents to a major incident.

</td></tr><tr><td>

Similar Incidents

</td><td>

Similarity

</td><td>

Recommends similar incidents based on the **Short description** and **Description** fields, to help with incident investigation and resolution processes.

</td></tr><tr><td>

Similar Open Incidents

</td><td>

Similarity

</td><td>

Recommends similar open incidents based on the **Short description** and **Description** fields, that the current incident can be linked to.

</td></tr><tr><td>

Similar Closed Incidents

</td><td>

Similarity

</td><td>

Recommends similar closed incidents based on the **Short description** and **Description** fields, to help with incident investigation and resolution processes.

</td></tr><tr><td>

Similar Resolved Incidents

</td><td>

Similarity

</td><td>

Recommends similar resolved incidents to help with incident investigation and resolution processes.

</td></tr></tbody>
</table>The following table lists the plugins that each solution definition requires.

<table id="table_ekm_dwq_hnb"><thead><tr><th>

Solution definition

</th><th>

Plugins

</th></tr></thead><tbody><tr><td>

-   Incident Assignment
-   Incident Categorization
-   Incident Service
-   Incident Configuration Item

</td><td>

The plugins com.glide.platform\_ml and com.snc.incident.ml\_solution must be active.

</td></tr><tr><td>

Similar Incidents \(MIM\)

</td><td>

The plugins com.glide.platform\_ml and com.snc.incident.mim.ml\_solution must be active.

</td></tr><tr><td>

Major Incident Recommendation

</td><td>

The plugins com.snc.contextual\_search\_ml and com.snc.incident.mim.ml\_solution must be active.

</td></tr><tr><td>

-   Similar Open Incidents
-   Similar Resolved Incidents
-   Similar Incidents
-   Similar Knowledge Articles

</td><td>

The plugins com.snc.contextual\_search\_ml and com.snc.incident.mim.ml\_solution must be active.

</td></tr></tbody>
</table>For more information about creating classification and similarity solutions, see [Create solution definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-solution-definition.md) and [Create similarity solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-similarity-solution.md).

## Business rule for classification solutions

This business rule applies only to the Incident Assignment and Incident Categorization solution definitions and is available only on instances where both Predictive Intelligence and Incident Management are active. Create your own business rules on the Incident \[incident\] table to customize prediction and reporting behaviors.

|Business rule|Table|Description|
|-------------|-----|-----------|
|Update Prediction Results|Incident|Updates the solution precision and coverage statistics. Runs when an incident record is closed.|

## Upgrade Information

If your instance is running on the Kingston release and you are upgrading to the Brazil release:

-   In a global domain environment, use the *solutionNames* array variable, which requires that you explicitly provide the solutions that are called by the business rule.
-   In a domain-separated environment, such as a managed service provider \(MSP\) environment, see the commented code in the business rule template to customize the business rule.
-   The business rule template calls the applyPredictionForSolution\(\) method to predict values regardless of any changes to the default value.

## Maintaining prediction accuracy

You can manage prediction drift by retraining, modifying, or creating new solutions to reflect changes in your business conditions. Test and modify your business rule over time to verify that it works as expected across multiple consumption points and user personas.

**Parent Topic:**[Machine learning solutions for IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/machine-learning-itsm.md)

