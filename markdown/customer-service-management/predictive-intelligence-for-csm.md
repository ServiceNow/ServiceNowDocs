---
title: Predictive Intelligence for CSM solution definitions
description: Use your instance records to build Customer Service Management specific solutions.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Predictive Intelligence for CSM solution definitions

Use your instance records to build Customer Service Management specific solutions.

## Solution definitions

These solution definitions are available as templates on instances where both Predictive Intelligence and Customer Service Management are active. Create your own solution definition records to customize the behavior.

<table id="table_bdh_nzs_kbb"><thead><tr><th>

Solution Definition

</th><th>

Solution Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CSM Case Assignment

</td><td>

Classification

</td><td>

Predicts the **Assignment group** field from the **Short description**.

</td></tr><tr><td>

CSM Case Categorization

</td><td>

Classification

</td><td>

Predicts the **Category** field from the **Short description**.

</td></tr><tr><td>

CSM Case Prioritization

</td><td>

Classification

</td><td>

Predicts the **Priority** field from the **Short description**.

</td></tr><tr><td>

Grouping of Cases into Topics

</td><td>

Clustering

</td><td>

Clusters similar cases into topics based on the **Short description**.

</td></tr><tr><td>

All Similar Cases

</td><td>

Similarity

</td><td>

Recommends similar cases based on the **Short description** that can help customer service agents with case investigation and resolution processes.

</td></tr><tr><td>

Recommended Open Cases

</td><td>

Similarity

</td><td>

Recommends similar open cases based on the **Short description**.

</td></tr><tr><td>

Recommended Resolved Cases

</td><td>

Similarity

</td><td>

Recommends similar resolved cases based on the **Short description**.

</td></tr><tr><td>

Major Issue Detector

</td><td>

Similarity

</td><td>

Provides recommendations for major issues based on the **Short description**. -   Recommends one or more major cases, if available.
-   Otherwise, recommends similar cases that are not linked as child cases to a major case.

</td></tr><tr><td>

Similar Knowledge Articles

</td><td>

Similarity

</td><td>

Recommends similar knowledge articles by comparing the **Text**, **Short description**, and **Description** fields of knowledge articles to the **Short description** of the customer service case.

</td></tr><tr><td>

Similar Knowledge Articles All

</td><td>

Similarity

</td><td>

Recommends similar knowledge articles by comparing fields in the Knowledge View database view \[sn\_customerservice\_knowledge\_view\] with the **Short description** of the customer service case. **Note:** This solution definition is used in the Auto-Responder feature. For more information, see [Train the similarity solution for finding Auto-Responder notification content](../task/train-sol-defn-auto-responder.md).

</td></tr></tbody>
</table>## Business rules for classification solutions

These business rules apply only to the CSM Case Assignment, CSM Case Categorization, and CSM Case Prioritization solution definitions. The rules are available only on instances where both Predictive Intelligence and Customer Service Management are active. Create your own business rules on the Case \[sn\_customerservice\_case\] table to customize prediction and reporting behaviors.

|Business rule|Table|Description|
|-------------|-----|-----------|
|Default Case Based Prediction|Case \[sn\_customerservice\_case\]|Generates prediction results from the active Customer Service Management solutions. Runs when a case record is inserted.|
|Update Prediction Results|Case \[sn\_customerservice\_case\]|Updates the solution precision and coverage statistics. Runs when a case record is closed.|

**Upgrade Information**

If your instance is running on the Kingston release and you are upgrading to the Zurich release:

-   Use the Default Case Based Prediction business rule template to create a new business rule. This rule includes a Solution variable that gets all active solutions retrieved by the findActiveSolution\(solutionName\) method.
-   In a global domain environment, use the solutionNames array variable which requires that you explicitly provide the solutions that are called by the business rule.
-   In a domain-separated environment, such as an MSP environment, refer to the commented code in the business rule template for easy customization.
-   The business rule template calls the applyPredictionForSolution\(\) method to predict regardless of any changes to the default value.

**Maintaining prediction accuracy**

You can manage prediction drift by retraining, modifying, or creating solutions to reflect changes in your business conditions. Test and modify your business rule over time to verify it works as desired across multiple consumption points and user personas.

**Related topics**  


[Similar case/recommendation](customer-service-similar-cases.md)

