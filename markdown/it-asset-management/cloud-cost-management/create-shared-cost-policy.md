---
title: Create or update a shared cost allocation policy
description: Create a shared cost allocation policy with  different allocation types to split the cost of shared cloud resources among various business lines.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Create or update a shared cost allocation policy

Create a shared cost allocation policy with  different allocation types to split the cost of shared cloud resources among various business lines.

## Before you begin

-   A cloud account \(parent account\) that has at least one service account and associated datacenters is required.
-   A Billing Download job must be created and the billing data must be pulled.
-   For Kubernetes, you must enable the cost allocation tag on your provider console for each Kubernetes cluster before you execute the Billing Download job.

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\] or insights\_owner \[sn\_clin\_core.insights\_owner\] for owned service accounts.

## About this task

-   You must select one of the Cloud Cost Management application scopes to create or update a shared cost allocation policy.
-   You can create as many policies as needed.
-   If Kubernetes Service is selected as Service Category, you can't edit the Service Category, Resource Type, Kubernetes Cluster fields while editing a policy.
-   When you deactivate a shared cost allocation policy, allocations get updated with the latest policy match.

## Procedure

1.  Navigate to **Workspaces** &gt; **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration**.

2.  Select **Shared cost allocation policies**.

3.  Select **New/Edit**.

4.  On the Shared Cost Allocation Policy Creation form, fill in the fields.

    For a description of the field values, see [List of Shared cost allocation policy fields](../reference/shared-cost-allocation-policy-fields.md).

5.  Select **Submit**.


## Result

After you create or modify a shared cost allocation policy, the policy gets displayed on the **Shared Cost Allocation Policies** page. Find the details of the policy such as the name, allocation type, business unit, and cloud service.

When the Discovery and Billing Download job executions finish, the system applies active policies to identify matching resources and then performs the policy actions on the resources.

## What to do next

After you create or update a shared cost allocation policy, select **Reapply policies** to apply the created policy to a resource.

**Parent Topic:**[Using Cloud Cost Management](../concept/using-cloud-insights.md)

