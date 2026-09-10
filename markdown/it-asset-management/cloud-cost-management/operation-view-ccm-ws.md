---
title: Operations view
description: Use the Operations view in the Cloud Cost Management Workspace to view and manage your preferences, cost usage tags, and administration-related operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/operation-view-ccm-ws.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Cloud Cost Management Workspace, Explore, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Operations view

Use the Operations view in the Cloud Cost Management Workspace to view and manage your preferences, cost usage tags, and administration-related operations.

**Important:** If you have the insights\_owner role, only the accounts that are assigned to you appear in the filters and data.

Access the Operations view by navigating to **Workspaces** &gt; **Cloud Cost Management Workspace** &gt; **Operations**.

\[Omitted image "operations-view.png"\] Alt text: Operations view in Cloud Cost Management Workspace

The Operations view includes the following categories of tasks:

-   **My preferences** - **Currency preference**: Set up your preferred display currency for the dashboard widgets, recommendations \(rightsizing, business hours, unused resources, reservation, and savings plan\), budgets, and billing data. For more information, see [Choose preferred currency for cost and usage data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/choose-pref-currency.md).

    **Note:** The option to set up your preferred currency is available with Cloud Cost Management 10.0.0 or later.

-   **Cost usage tags**: Associate resource usage with particular business entities. For more information, see [Cost usage tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/tags-overview.md).
    -   **Tag categories**: Create and update tag categories. For more information, see [Create and update a tag category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/tag-category-crud-cloudin.md).
    -   **Tag names**: Create tag names for the tag categories.
    -   **Tag category source**: Tag category source setting controls how the Cloud Cost Management application maps cloud resource tags to business entities for cost attribution and reporting. Available tag category source options are cloud provider tags, CMDB-driven cloud mapping, and ServiceNow-managed dimensions. For more information, see [Select a tag category source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/select-tag-category-source.md).
-   **Administration**
    -   **Service accounts**: Create service accounts for AWS, Azure, and Google to store the credentials and access information for your account.
        -   [Add an AWS service account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-service-acct-add-cloudin.md)
        -   [Add a Microsoft Azure government service account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/azure-gov-service-acct-add-cloudin.md)
        -   [Add a Google Cloud service account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/add-gcp-serv-acc.md)
    -   **Credentials**: Create credentials for accessing AWS, Azure, and Google accounts.
        -   [Set up access to AWS billing and usage data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-billing-usage-data.md)
        -   [Set up access to Microsoft Azure billing and usage data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/azure-billing-usage-data.md)
        -   [Set up access to Google Cloud billing and usage data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/google-cloud-billing-data.md)
    -   **Billing download jobs**: View, manage, and schedule the jobs that download billing data for AWS, Azure, and Google.
        -   [Schedule and manage the jobs that download AWS billing data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-bill-dwnld-job-cloudin.md)
        -   [Schedule and manage the jobs that download Azure billing data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/schedule-azure-billing-job.md)
        -   [Schedule and manage the jobs that download Google Cloud billing data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/gcp-bill-dwnld-job-cloudin.md)
    -   **Price sheet download jobs**: View, manage, and schedule the jobs that download the price sheet for AWS, Azure, and Google.
        -   [Schedule and manage the Cloud Cost Management jobs that download AWS price sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/aws-pricesht-sched-dwnld-cloudin.md)
        -   [Schedule and manage the Cloud Cost Management jobs that download Microsoft Azure price sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/azure-pricesht-sched-dwnld-cloudin.md)
        -   [Schedule and manage the Cloud Cost Management jobs that download Google Cloud price sheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/gcp-pricesht-sched-dwnld-cloudin.md)
    -   **Business hours schedules**: Create a schedule for business hours. For more information, see [Create Business hours schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/create-bh-schedule.md).
    -   **Unassigned resources**: View list of unassigned resources and details of the resources such as provider, region, CMDB CI, service account and category, and SyS ID.
    -   **Global exclusions**: Exclude resources for ensuring that cost data for a particular resource doesn’t appear in a report. For more information, see [Exclude a resource from all Cloud Cost Management reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/exclusion-list-add-to-cloudin.md).
    -   **Job executions**: View the job execution details of the following:
        -   Billing download
        -   Price sheet download
        -   Spend
        -   Budget
        -   Rightsizing/Unused
        -   Business hour
        -   Unassigned
        -   Commitments
    -   **Account to owner mappings**: Set up or update ownership of service accounts. For more information, see [Assign service accounts to an insights\_owner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/insights-owner-new-cloudin.md) and [Update or reassign insights\_owner privileges](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/insights-owner-update-cloudin.md).
    -   **View insights owners**: View the list of insights owner and also create a cloud service account. For more information, see [View the service accounts owned by an insights\_owner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/insights-owners-view-list-cloudin.md).
    -   **AWS price discounts**: View and specify the provider discount rate for each service account. For more information, see [Specify rate discounts to enable accurate pricing for Rightsizing recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/discounts-specify-cloudin.md).
    -   **AWS Gov account mappings**: Create mapping of AWS Gov account to a linked service account. For more information, see [Create AWS Gov accounts mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/map-aws-gov-acc.md).
    -   **Upload business data**: Upload your revenue and unit count data to populate the Unit economics dashboard in the Business insights view. For more information, see [Upload business data for unit economics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/upload-business-data.md).
    -   **Shared cost allocation policies**: Create, update, and view shared cost allocation policies with  different allocation types to split the cost of shared cloud resources among various business lines. For more information, see [Create or update a shared cost allocation policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/create-shared-cost-policy.md).
    -   **Multi-currency setup**: Set up or update the currency options for Cloud Cost Management users to view their cloud cost and usage data in their preferred currency. For more information, see [Set up or update preferred currency options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/setup-update-currency.md).

        **Note:** The multi-currency setup option is available with Cloud Cost Management version 10.0.0 or later.


