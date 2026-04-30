---
title: Alert similarity
description: Finding alerts that are similar to the alert that you are currently investigating can help save troubleshooting time by seeing how similar alerts were resolved.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Alert similarity

Finding alerts that are similar to the alert that you are currently investigating can help save troubleshooting time by seeing how similar alerts were resolved.

## Finding similar alerts

Alert similarity applies natural language processing \(NLP\) based on ServiceNow AI Platform machine learning \(ML\) as implemented in [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

ML logic filters out irrelevant information and provides further information to help you understand the cause of alerts. You can view solutions used to resolve similar alerts and the probable root cause.

ML helps find similar alerts based on text found in these alert record fields:

-   Configuration item.Class
-   Metric name
-   Description

## Additional alert information

In the Alert Workspace, select the required alert and click **Insight** to view additional information about the alert.

In the Alerts list, select the required alert and use the Alert Insight tabs on the right side of the alert record to view additional information about the alert. For example, you can view the top recent alerts for the current CI and similar CIs to find the most suitable solution towards resolving the alert.

The alert insight tabs are:

-   Impacted Services
-   Flapping
-   History
-   Activities
-   More Information
-   Repeated Alerts
-   Similar Alerts
-   CI Incidents
-   CI Change Requests
-   CI Problems
-   Related Incidents
-   Related Change Requests
-   Related Problems

For more information about the alert insight tabs, see [Alert insight information](alert-insight-information.md).

-   **[Find similar alerts](../task/find-similar-alerts.md)**  
You can find alerts similar to the alert currently being investigated. Save troubleshooting time by reviewing similar alerts to see how they were resolved.
-   **[Similarity solutions](word-collection-similarity-solution.md)**  
Similarity solutions enable you to use Machine Learning \(ML\) to compare the text in a resolved alert record to an open alert record to reuse its resolution approach.
-   **[Create an Event Management similarity solution](../task/create-solution-similarity.md)**  
Create and train a solution that applies machine learning to a collection of words to target and suggest similar alerts in your instance dataset. For example, you can compare the text in a resolved alert record to an open alert record to reuse its resolution approach.
-   **[View Event Management solution training progress](../task/view-solution-training-progress.md)**  
View solution training progress or statistics to determine whether a solution is available or how long the next training cycle might take to complete.
-   **[Review Event Management similarity examples](../task/view-similarity-examples.md)**  
Review the similarity examples and scores that the system provides during solution training to see how the selected alert record compares to existing alert records. For example, you can modify the similarity score threshold to increase the accuracy of your similarity recommendations.
-   **[Activate Event Management solution version](../task/solution-version-activated.md)**  
The system activates the most recent version of the solution, but you can activate any previously trained Event Management solution version if it is more appropriate.

**Parent Topic:**[Manage and monitor alerts](c_EMAlert.md)

