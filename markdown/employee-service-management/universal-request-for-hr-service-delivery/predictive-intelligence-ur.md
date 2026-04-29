---
title: Predictive Intelligence for Universal Request
description: The Predictive Intelligence for Universal Request uses machine-learning algorithms for the auto-assignment of universal requests and to find similar knowledge articles and closed universal requests.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Predictive Intelligence for Universal Request

The Predictive Intelligence for Universal Request uses machine-learning algorithms for the auto-assignment of universal requests and to find similar knowledge articles and closed universal requests.

Predictive Intelligence for Universal Request has the following benefits:

-   Use of machine learning algorithms to predict the assignment group across various departments based on the data provided by the requester in the short description and description fields of the request.
-   Use of machine learning similarity solution to provide recommendations for similar Knowledge Base articles and similar closed Universal Request. These recommendations are based on the data provided in the short description and description fields of the request, and help agents to resolve universal requests quickly.

## Solution definitions for Predictive Intelligence for Universal Request

The solution definition for Predictive Intelligence for Universal Request is available when you activate Predictive Intelligence plugin \(com.glide.platform\_ml\) and Predictive Intelligence for Universal Request \(com.snc.universal\_request.ml\) plugins. You can customize the solution definition to meet your business requirements.

<table id="table_crv_lcq_xlb"><thead><tr><th>

Solution definition

</th><th>

Solution type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Universal Request Categorization

</td><td>

Classification

</td><td>

-   Predicts the assignment group from the short description and description of a Universal Request.
-   Runs a business rule to create service level tickets using the prediction.

The service level tickets that are created will be associated with the universal request.


</td></tr><tr><td>

Similar Knowledge Articles for UR

</td><td>

Similarity

</td><td>

Predicts similar knowledge base articles based on the short description and description of a Universal Request.

</td></tr><tr><td>

Similar closed Universal Request

</td><td>

Similarity

</td><td>

Predicts closed Universal Request that have similar short description, description, and assignment group.

</td></tr><tr><td>

Identify sensitive information in UR

</td><td>

Classification

</td><td>

Identifies and predicts that the UR is sensitive based on the short description and description of the request. It also marks the request as restricted.

</td></tr></tbody>
</table>-   **[Train the classification solution to predict the assignment group](../task/train-ur-classification-soln.md)**  
Train the Universal Request classification solution definition to identify and predict an assignment group using the short description and create service level tickets that are associated with the universal request.
-   **[Train the similarity solution for similar knowledge articles](../task/train-similarity-for-articles-ur.md)**  
Train the Similar Knowledge articles for UR solution definition to identify and predict knowledge articles using the short description. When an agent opens a universal request, similar knowledge articles are displayed in the Related Search section of the Universal Request record.
-   **[Train the similarity solution for similar closed Universal Requests](../task/train-similarity-for-closed-ur.md)**  
Train the Similar Closed Universal Request solution definition to identify and predict similar Universal Requests that are closed based on the short description, description, and the assignment group of the Universal Request created. When an agent opens a universal request, similar closed universal requests can be searched in the Related Search section of the Universal Request record.
-   **[Train the classification solution to identify UR with sensitive information](../task/train-classification-identify-restrict-ur.md)**  
Train the Universal Request classification solution definition to identify and predict universal request with sensitive information using the short description and description. The solution identifies and marks the UR as restricted, allowing only agents with access or from the assignment group to work on the request.

**Parent Topic:**[Configuring Universal Request](configure-ur.md)

