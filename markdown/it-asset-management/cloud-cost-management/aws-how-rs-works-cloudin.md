---
title: Rightsizing analysis for AWS
description: Cloud Cost Management uses a process that is optimized for each provider. For AWS, Cloud Cost Management compares the calculated potential costs to actual billed costs and then generates recommendations.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Rightsizing resources, Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Rightsizing analysis for AWS

Cloud Cost Management uses a process that is optimized for each provider. For AWS, Cloud Cost Management compares the calculated potential costs to actual billed costs and then generates recommendations.

## How Rightsizing resources analysis works for AWS

To generate accurate Rightsizing resources recommendations, Cloud Cost Management follows this procedure every time billing data is updated:

-   Obtain costs from the updated billing data tables.
-   Collect the CPU and memory usage data for each resource for the preceding 14 days.

    **Important:**

    -   To enable Rightsizing, you must define memory metrics to obtain memory usage data. For more information, see [Define a metric threshold](../task/define-metric-threshold.md).
    -   Recommendations are generated only for CPU usage data.
-   Obtain rates for resource types and sizes from the price sheet data tables.
-   If available, obtain percentage discount rates from the discount tables and apply the appropriate discounts to the rates on the price sheet.
-   Compare the calculated potential costs to the actual billed costs and then generate recommendations.
    -   If the average top 20% of CPU usage is less than 1%, then the resource is recommended for Unused resources processes.
    -   If the average top 20% of CPU usage is greater than 1% but less than 40%, then the resource is recommended for Rightsizing processes. The recommended memory size is calculated so that the peak usage during the analysis period would be no more than 80% of the recommended size. For example, a resource currently has 16 GB and the available sizes are 4 GB, 8 GB, and 16 GB. If the resource used a peak of 3.99 GB over the analysis period, then the recommendation would be 8 GB.

**Important:** If you have installed the Cloud Cost Management Infra Stack application, for AWS Rightsizing recommendations to work accurately, you must use the **GetCostAndUsageWithResources** API to retrieve the cost and usage metrics with resources for your account from your provider \(through AWS Portal\). For more information, see GetCostAndUsageWithResources API Reference topic in the AWS Billing and Cost Management Documentation.

## Resources that aren't considered

Resources with the following AWS attributes aren't considered for Rightsizing recommendations:

-   Members of an Auto Scaling group \(ASG\)
-   Burstable
-   Not in a VPC
-   Not backed by an EBS root volume
-   Don't have enhanced network support
-   Virtualization type isn't HVM
-   Spot instance

