---
title: Predictive Intelligence for Knowledge Management
description: The Predictive Intelligence for Knowledge Management capability uses machine-learning algorithms to provide various Knowledge Management capabilities, such as similar articles and knowledge demand insights.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Machine learning solutions for Knowledge Management, Exploring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Predictive Intelligence for Knowledge Management

The Predictive Intelligence for Knowledge Management capability uses machine-learning algorithms to provide various Knowledge Management capabilities, such as similar articles and knowledge demand insights.

## Solution definitions for Predictive Intelligence for Knowledge Management

The solution definitions for Predictive Intelligence for Knowledge Management capability are available in the Predictive Intelligence for Knowledge Management plugin \(com.snc.knowledge\_ml\). For more information about the plugin, see [Additional plugins for Knowledge Management](../reference/additional-plugins-km.md).

<table id="table_bdh_nzs_kbc"><thead><tr><th>

Solution Definition

</th><th>

Solution Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge Similar Articles**Note:** This solution definition is available as a template on instances where both the Predictive Intelligence for Contextual Search plugin \(com.snc.contextual\_search\_ml\) and Predictive Intelligence for Knowledge Management plugin \(com.snc.knowledge\_ml\) are activated.

</td><td>

Similarity

</td><td>

Suggests related articles based on the short description of articles. You can see the results in the following places:-   The Knowledge results section on the Knowledge form when creating an article in the Knowledge Management Service Portal.

If the Knowledge results section isn't displayed on the Knowledge form, you may need to configure the form, to add the **Contextual Search Results** field. For more information, see [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   The Related Articles section on the knowledge article view page in the Knowledge Management Service Portal and Now Mobile applications.
-   The Agent assist in Agent Workspace when the **Similar Articles \(ML\)** option is selected.

</td></tr><tr><td>

Demand Insights: Case Clusters Need Knowledge

</td><td>

Clustering

</td><td>

Populates collections of closed and resolved customer service cases on the Demand Insights for Cases dashboard.

</td></tr><tr><td>

Demand Insights: Incident Clusters Need Knowledge

</td><td>

Clustering

</td><td>

Populates collections of closed and resolved incidents on the Demand Insights for Incidents dashboard.

</td></tr><tr><td>

Demand Insights: Similar Cases and Knowledge

</td><td>

Similarity

</td><td>

Compares similarity of incidents with knowledge bases and identifies similar closed and resolved customer service cases as candidate knowledge gaps.

</td></tr><tr><td>

Demand Insights: Similar Incidents and Knowledge

</td><td>

Similarity

</td><td>

Compares similarity of incidents with knowledge bases and identifies similar closed and resolved incidents as candidate knowledge gaps.

</td></tr></tbody>
</table>**Parent Topic:**[Machine learning solutions for Knowledge Management](machine-learning-km.md)

**Related topics**  


[Train the similarity solution for Knowledge Management to find related articles](../task/train-similarity-solution-km.md)

[Create a knowledge article in Agent Workspace](../task/create-article-workspace.md)

[Knowledge demand insights](knowledge-demand-insights.md)

[Demand Insights for Cases dashboard](demand-insights-cases-dashboard.md)

