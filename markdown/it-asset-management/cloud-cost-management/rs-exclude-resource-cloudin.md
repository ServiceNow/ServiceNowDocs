---
title: Exclude a resource from Rightsizing analysis
description: To ensure that a particular resource is not considered or recommended for Rightsizing, add the resource to the Excluded Resources list. The system continues to collect cost and usage data but does not consider the resource for Rightsizing.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Resize resources with Rightsizing, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Exclude a resource from Rightsizing analysis

To ensure that a particular resource is not considered or recommended for Rightsizing, add the resource to the Excluded Resources list. The system continues to collect cost and usage data but does not consider the resource for Rightsizing.

## Before you begin

Run Discovery on each service account.

Ensure that the Billing Download job has completed for each provider.

Ensure that the Price Sheet Download job has completed for each provider.

Role required: insights\_admin or insights\_owner

## About this task

When you change the resources that are included in a job, the app checks for the following conditions:

-   A resource in the job is owned by another user \(as when a insights\_admin updates a job that was created by an insights\_owner or an insights\_owner updates a job that was created by a different insights\_owner\).
-   The job was created by another user.

If either condition is met, the app sends an email notification to the owner of the resource or the creator of the job.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Recommendations** &gt; **Rightsizing**.

2.  On the New, Declined, or Failed tabs, select the resources that you want to exclude from rightsizing analysis.

3.  Select **Exclude**.

    The resources are added to the Excluded Resources list. To remove a resource from the list, select the resources from the **Excluded** tab and then select **Remove From Exclusion**.


**Parent Topic:**[Resize resources with Rightsizing](../concept/resize-res-ci.md)

**Related topics**  


[Exclude a resource from all Cloud Cost Management reports](exclusion-list-add-to-cloudin.md)

