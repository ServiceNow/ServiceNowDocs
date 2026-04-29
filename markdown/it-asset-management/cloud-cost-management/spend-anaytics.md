---
title: Spend analytics
description: The Spend analytics page helps you gain visibility to your cloud costs by displaying your cloud, Kubernetes, and shared resources spend over a time range or a cost type that you specify.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Cloud Cost Management overview, Cloud Cost Management Workspace, Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Spend analytics

The Spend analytics page helps you gain visibility to your cloud costs by displaying your cloud, Kubernetes, and shared resources spend over a time range or a cost type that you specify.

**Important:** If you have the insights\_owner role, only the accounts that are assigned to you appear in the filters and data.

Use the Spend analytics page to view the following:

-   Cloud spend analytics
-   Kubernetes spend analytics
-   Shared cost analytics

**Note:** You can't view the spend of your resources for nested tag values. For example, **\{"name":"test","created-by":"xyz","prod":"false","shared\_resource":"false"\}**.

## Cloud spend analytics

Select the **Cloud spend analytics** tab to do the following tasks:

-   Understand how you currently spend on cloud resources for a period that you can select in the **Time range** field.
-   Group the cloud spend analytics by using either of the following values:
    -   Provider
    -   Purchase option
    -   Region
    -   Service account
    -   Service category
    -   Cloud service
    -   Resource group
    -   Tag category
-   Sort your cloud spend results by the current month or select a time range such as 3, 6, 9, or 12 months.
-   Get a better picture of your results by searching and selecting values through the following filters:
    -   Provider
    -   Master Service Account
    -   Service account
    -   Region
    -   Service category
    -   Cloud service
    -   Purchase option
    -   Resource group
    -   Tag category

        **Note:** For more information about tag categories and the list of default tag categories, see [Tags and tag categories](../reference/tags-overview.md) and [List of default tag categories](../reference/default-tag-categories.md).

    -   Tag values
    -   Tag categories selected

![Cloud spend analytics page displaying the spend on various cloud resources grouped by various parameters.](../image/spend-analytic.png)

## Kubernetes spend analytics

Select the **Kubernetes spend analytics** tab to do the following tasks:

-   Understand how you spend on Kubernetes on the cloud for a period that you can select in the **Time range** field.
-   Group the Kubernetes spend analytics by using either of the following values:
    -   Kubernetes cluster
    -   Kubernetes namespace
    -   Tag category
-   Select the cost type as Actual cost or Amortized cost.
    -   Actual cost: Each billing period, your organization pays for direct cloud services.
    -   Amortized cost: Your organization pays the effective cost of the upfront and monthly reservation fees spread across the billing period. The amortized cost type is described in detail on the provider site.
-   Sort your Kubernetes spend results by the current month or select a time range such as 3, 6, 9, or 12 months.
-   Get a better picture of your results by searching and selecting values through the following filters:
    -   Provider
    -   Master Service Account
    -   Service account
    -   Region
    -   Kubernetes cluster
    -   Kubernetes namespace
    -   Purchase option
    -   Resource group
    -   Tag category

        **Note:** For more information about tag categories and the list of default tag categories, see [Tags and tag categories](../reference/tags-overview.md) and [List of default tag categories](../reference/default-tag-categories.md).

    -   Tag value
    -   Tag categories selected
-   View details of cost per Kubernetes cluster and cost per Kubernetes namespace.

![Kubernetes spend analytcis displaying the spend on Kubernetes on the cloud.](../image/ccm-kubernetes-spend-analytics.png)

## Shared cost analytics

Select the **Shared cost analytics** tab to do the following tasks:

-   Understand how you currently spend on shared cloud resources for a period that you can select in the **Time range** field.
-   Group the Shared cost analytics by using either of the following values:
    -   Provider
    -   Purchase option
    -   Region
    -   Service account
    -   Service category
    -   Cloud service
    -   Resource group
    -   Tag category
-   Select **Cost type** as Actual cost or Amortized cost.
    -   Actual cost: Each billing period, your organization pays for direct cloud services.
    -   Amortized cost: Your organization pays the effective cost of the upfront and monthly reservation fees spread across the billing period. The amortized cost type is described in detail on the provider site.
-   Sort your shared resources cost results by the current month or select a time range such as 3, 6, 9, or 12 months.
-   Get a better picture of your results by searching and selecting values through the following filters:
    -   Provider
    -   Master Service Account
    -   Service account
    -   Region
    -   Service category
    -   Cloud service
    -   Purchase option
    -   Resource group
    -   Tag category

        **Note:** For more information about tag categories and the list of default tag categories, see [Tags and tag categories](../reference/tags-overview.md) and [List of default tag categories](../reference/default-tag-categories.md).

    -   Tag value
    -   Tag categories selected
-   View details of the direct cost and shared cost of your cloud resources.

![Shared cost analytics displaying the spend on shared cloud resources.](../image/ccm-shared-cost-analytics.png)

**Related topics**  


[Cloud service categories in Cloud Cost Management](cloud-ser-categories.md)

[Tags and tag categories](../reference/tags-overview.md)

[Create and update a tag category](../task/tag-category-crud-cloudin.md)

[Create or update a shared cost allocation policy](../task/create-shared-cost-policy.md)

