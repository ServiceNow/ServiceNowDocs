---
title: Predictive Intelligence for Change Management
description: The Predictive Intelligence for Change Management capability uses machine-learning algorithms to suggest standard templates, identify similar incidents, and enhance risk assessment for the change.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Predictive Intelligence for Change Management

The Predictive Intelligence for Change Management capability uses machine-learning algorithms to suggest standard templates, identify similar incidents, and enhance risk assessment for the change.

Predictive Intelligence for Change Management delivers the following benefits:

-   Enhanced change risk calculation using machine-learning algorithms to assess change risk.
-   Uses Predictive Intelligence clustering capability to identify and suggest Standard Change templates to create a change.

## Solution definitions for Predictive Intelligence for Change Management

The Solutions definitions for Predictive Intelligence for Change Management capability are available after you activate the following plugins:

-   Change Management - Risk Intelligence plugin \(com.snc.change\_management.ml.risk\)
-   Change Management - Standard Change Template Intelligence plugin \(com.snc.change\_management.ml.sctp\)

**Note:** Predictive intelligent for Change Management plugins can be requested through the Now Support Customer Service system.

For more information, see [Change Management plugins](change-plugins.md).

<table id="table_xt3_n4g_nlb"><thead><tr><th>

Solution definition

</th><th>

Solution type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk for proposed change

</td><td>

Similarity and Categorization

</td><td>

Provides insight into the potential risk of the change activity and facilitates intelligent approval decisions. The info message puts all the risk related information to easily compare the returned value.This prediction helps in reducing approval friction and time. For example, when risk = low, you can use Change Approval Policies to automatically approve this low risk activity.

</td></tr><tr><td>

Standard change candidates

</td><td>

Clustering

</td><td>

Analyzes and suggests opportunities for Standard Change proposal templates that can be used for automatically creating a change. This solution uses similarity and clustering solution type to identify the common fields in the records and make it a template.

</td></tr></tbody>
</table>-   **[Intelligent solutions system properties](../reference/change-mgmt-intelligentsoln-properties.md)**  
Administrators can configure the Change Management Intelligent solutions system properties to use predictive intelligence \(PI\) capabilities.
-   **[Train the Risk Intelligence solution](../task/train-risk-intelligence-solution.md)**  
Create Risk categorization or similarity solution definitions to use the predictive intelligence that helps in accessing change risk.
-   **[Train the clustering solution for standard change proposal](../task/train-std-chg-proposal-soln.md)**  
Train the Standard change proposal solution definition to use clustering capabilities to identify and suggest Standard Change templates to create a change.

**Parent Topic:**[Configuring Change Management](configure-change-management.md)

