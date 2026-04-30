---
title: Operations view
description: Use the Operations view in the Cloud Cost Management Workspace to view and manage recommendations, cost usage tags, and administration-related operations.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Cloud Cost Management Workspace, Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Operations view

Use the Operations view in the Cloud Cost Management Workspace to view and manage recommendations, cost usage tags, and administration-related operations.

**Important:** If you have the insights\_owner role, only the accounts that are assigned to you appear in the filters and data.

You can access the Operations view by navigating to **Cloud Cost Management Workspace** &gt; **Operations**.

![Operations view in Cloud Cost Management Workspace](../image/operations-view.png)

The Operations view lets you do the following tasks by expanding each category in the **Lists** tab:

-   **Overview**: View your total savings by recommendation type and the number of recommendations to review, which are grouped by their state.
-   **Recommendations**: View the savings of your cloud assets by recommendation type such as Rightsizing, Unused resources, Reservation/Saving plans, and Business hours. Select the recommendation type to view detailed reports and act accordingly:
    -   **Rightsizing**: View the total potential savings by service category, total potential savings by change group, number of resources that are scheduled, completed, declined, failed, and excluded for rightsizing. You can also exclude or schedule resources for rightsizing resources, configure the rightsize settings, and create service category metrics. For more information, see [Resize resources with Rightsizing](resize-res-ci.md).
    -   **Unused resources**: View the total potential savings by service category, total potential savings by change group, number of unused resources that are scheduled, completed, declined, failed, and excluded. You can also exclude or schedule unused resources to identify resources that are wasting money because they aren’t used, configure the unused settings, and create unused recommendations. For more information, see [Manage unused resources](manage-unused-mac.md).
    -   **Reservation/Saving plans**: View upfront cost to reserve, overall RI utilization percentage, potential savings by service category. You can accept or decline the recommendations for reserved instances. For more information, see [Reduce resource cost with Reservation Plans](reserve-plan-using.md#)
    -   **Business hours**: View the total potential savings by service category, total potential savings by change group, business hour against non-business hour spend, and number of resources that are scheduled, completed, declined, failed, and excluded from business hour policies. You can also exclude resources from the policies. For more information, see [Improve resource usage with Business hours](improve-res-use-business.md).
-   **Cost usage tags**: Associate resource usage with particular business entities. For more information, see [Tags and tag categories](../reference/tags-overview.md).

    -   **Tag categories**: Create and update tag categories.
    -   **Tag names**: Create tag names for the tag categories.
    For more information, see [Create and update a tag category](../task/tag-category-crud-cloudin.md).

-   **Administration**
    -   **Service accounts**: Create service accounts for AWS, Azure, and Google to store the credentials and access information for your account.
        -   [Add an AWS service account](../task/aws-service-acct-add-cloudin.md)
        -   [Add a Microsoft Azure government service account](../task/azure-gov-service-acct-add-cloudin.md)
        -   [Add a Google Cloud service account](../task/add-gcp-serv-acc.md)
    -   **Credentials**: Create credentials for accessing AWS, Azure, and Google accounts.
        -   [Set up access to AWS billing and usage data](aws-billing-usage-data.md)
        -   [Set up access to Microsoft Azure billing and usage data](azure-billing-usage-data.md)
        -   [Set up access to Google Cloud billing and usage data](google-cloud-billing-data.md)
    -   **Billing download jobs**: View, manage, and schedule the jobs that download billing data for AWS, Azure, and Google.
        -   [Schedule and manage the jobs that download AWS billing data](../task/aws-bill-dwnld-job-cloudin.md)
        -   [Schedule and manage the jobs that download Azure billing data](../task/schedule-azure-billing-job.md)
        -   [Schedule and manage the jobs that download Google Cloud billing data](../task/gcp-bill-dwnld-job-cloudin.md)
    -   **Price sheet download jobs**: View, manage, and schedule the jobs that download the price sheet for AWS, Azure, and Google.
        -   [Schedule and manage the Cloud Cost Management jobs that download AWS price sheets](../task/aws-pricesht-sched-dwnld-cloudin.md)
        -   [Schedule and manage the Cloud Cost Management jobs that download Microsoft Azure price sheets](../task/azure-pricesht-sched-dwnld-cloudin.md)
        -   [Schedule and manage the Cloud Cost Management jobs that download Google Cloud price sheets](../task/gcp-pricesht-sched-dwnld-cloudin.md)
    -   **Business hours schedules**: Create a schedule for business hours. For more information, see [Create Business hours schedule](../task/create-bh-schedule.md).
    -   **Unassigned resources**: View list of unassigned resources and details of the resources such as provider, region, CMDB CI, service account and category, and SyS ID.
    -   **Global exclusions**: Exclude resources for ensuring that cost data for a particular resource doesn’t appear in a report. For more information, see [Exclude a resource from all Cloud Cost Management reports](../task/exclusion-list-add-to-cloudin.md).
    -   **Job executions**: View the job execution details of the following:
        -   Billing download
        -   Price sheet download
        -   Spend
        -   Budget
        -   Rightsizing/Unused
        -   Business hour
        -   Unassigned
        -   Reservation plan
    -   **Account to owner mappings**: Set up or update ownership of service accounts. For more information, see [Assign service accounts to an insights\_owner](../task/insights-owner-new-cloudin.md) and [Update or reassign insights\_owner privileges](../task/insights-owner-update-cloudin.md).
    -   **View insights owners**: View the list of insights owner and also create a cloud service account. For more information, see [View the service accounts owned by an insights\_owner](../task/insights-owners-view-list-cloudin.md).
    -   **AWS price discounts**: View and specify the provider discount rate for each service account. For more information, see [Specify rate discounts to enable accurate pricing for Rightsizing recommendations](../task/discounts-specify-cloudin.md).
    -   **AWS Gov account mappings**: Create mapping of AWS Gov account to a linked service account. For more information, see [Create AWS Gov accounts mapping](../task/map-aws-gov-acc.md).
    -   **Shared cost allocation policies**: Create, update, and view shared cost allocation policies with  different allocation types to split the cost of shared cloud resources among various business lines. For more information, see [Create or update a shared cost allocation policy](../task/create-shared-cost-policy.md).
-   **Tools**- **Compare MetricBase with Spend data**: Compare MetricBase \(Clotho\) data with your Spend data for Amazon Web Services \(AWS\), Azure, and Google Cloud Platform \(GCP\) and easily diagnose and troubleshoot Cloud Cost Management billing issues. For more information see, [Compare MetricBase data with spend data](../task/compare-metricbase-spend.md).

    **Note:** This option is available with Cloud Cost Management 8.0.0 version or later.


