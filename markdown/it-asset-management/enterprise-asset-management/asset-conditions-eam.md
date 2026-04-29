---
title: Asset conditions in Enterprise Asset Management
description: Assessing the condition of assets in your organization aids in effective maintenance planning, resource allocation, and managing the asset life cycle.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Asset conditions in Enterprise Asset Management

Assessing the condition of assets in your organization aids in effective maintenance planning, resource allocation, and managing the asset life cycle.

## Overview of asset conditions

You need to evaluate assets based on specific conditions to ensure reliability. Asset health helps your organization in various ways:

-   Maximizes asset life.
-   Reduces unplanned downtime.
-   Improves operational effectiveness and safety.
-   Helps to comply with regulations and industry standards.

## Roles for asset conditions

The following are the two new roles added for the asset conditions feature:

-   Asset technician \(sn\_smart\_asmt.actor\) role added to the Enterprise technician \(sn\_eam.asset\_technician\) role
-   Asset manager \(sn\_smart\_asmt.template\_manager\) role added to the Enterprise asset manager \(sn\_eam.asset\_manager\) role

## Asset condition workflow

The asset condition workflow comprises of the following stages:

-   **Create condition templates**

    Create condition templates and associate condition attributes that you have defined to a condition template. Create questions and enable scoring in the templates to indicate whether the condition attributes for a model or asset passed or failed. For more details, see [Create condition templates for condition attributes](../task/create-condition-template-eam.md).

-   **Define condition attributes**

    Enterprise asset managers define condition attributes for evaluating models and assets. For more details, see [Define condition attributes on enterprise models and assets](../task/create-condition-attribute-eam.md).

-   **Schedule condition evaluations**

    The Enterprise asset manager schedules evaluations via maintenance plans or work orders. For more details, see [Schedule condition evaluations for enterprise models or assets](../task/schedule-condtion-evaluations.md).

-   **Perform condition evaluations**

    The technician performs the evaluation via the web interface or through the mobile application. Once the evaluation is complete, a score and a result are calculated. The Enterprise asset manager either accepts or rejects the evaluation. For more details, see [Perform condition evaluation from the Enterprise Asset Workspace](../task/perform-condition-assessment-webui.md) and [Perform condition evaluation from the Mobile Agent application](../task/perform-condition-assessment-mobileapp.md).

-   **View the evaluation reports**

    The Enterprise asset manager views the report for the evaluation. For more details, see [Review the asset condition results](../task/review-service-event-conditions.md).


## Plugin dependencies for asset conditions

The following are the plugin dependencies that are required to use asset conditions:

|Plugin Name|Plugin ID|
|-----------|---------|
|app-smart-assessment-core|com.sn\_smart\_asmt|
|sn-smart-assessment-connected|com.sn\_smart\_assessment\_connected|
|sn-smart-assessment-designer|com.sn\_smart\_assessment\_designer|
|app-smart-assessment-scoring|com.sn\_smart\_scoring|
|app-smart-assessment-mobile|com.snc.smart\_assessment\_mobile|
|mobile scripted screen|com.glide.sg.scriptedscreen|

## Domain separation supported

The asset conditions feature supports domain separation.

-   **[Create condition templates for condition attributes](../task/create-condition-template-eam.md)**  
Create a condition template and associate the template to condition attributes for enterprise models and assets.
-   **[Define condition attributes on enterprise models and assets](../task/create-condition-attribute-eam.md)**  
Define the conditions to be inspected on enterprise models and assets throughout their life cycle.

**Parent Topic:**[Create and manage enterprise assets](create-manage-enterprise-assets.md)

