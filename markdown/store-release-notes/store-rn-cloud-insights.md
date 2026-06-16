---
title: Cloud Cost Management release notes
description: Version history for the ITAM Cloud Cost Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-cloud-insights.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - IT Asset Management release notes, ServiceNow Store release notes]
---

# Cloud Cost Management release notes

Version history for the ITAM Cloud Cost Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.0.2 - June 2026**
    -   Performance-related defect fixes.
    -   Stability-related defect fixes.
-   **Version 10.0.1 - March 2026**
    -   Cloud Cost Management highlights for the 10.0 release
        -   Manage your Azure cloud cost data with support for FinOps Open Cost and Usage Specification \(FOCUS\), the industry standard for cost and usage data.
        -   Gain financial clarity and reporting flexibility by choosing to view your cloud cost data in your preferred currency.
        -   Get centralized visibility into the Microsoft Partner Agreement \(MPA\) account spend when operating under a Managed Service Provider \(MSP\).
        -   The Multi-currency setup operation is available on the Cloud Cost Management Workspace Operations view to enable setting up display currency options for cloud cost and usage data.
        -   The Currency preference operation is available on the Cloud Cost Management Workspace Operations view to enable selecting preferred currency options for cloud cost and usage data.
        -   Use the instance operator role to perform routine operational tasks without requiring the full admin role for basic operations. By using limited privileges in the instance operator role, you can help reduce security risks across your organization.
-   **Version 9.0.3 - February 2026**
    -   This release addresses both functional and performance issues. Updates include:
        -   Support for multi-MID server configurations for customers using multiple AWS Organizations.
        -   Improved license calculation with correct handling of ephemeral resources.
        -   Faster load times for the CCM landing page.
        -   Business Hours recommendations now cover EC2 instances that are detached from Auto Scaling groups.
        -   More precise Azure forecast calculations for subscription-based billing, considering only the relevant service account.
        -   Budget configurations now remain intact and are not deleted automatically.
        -   Corrected GCP Business Hours actions for improved cost optimization.
        -   Expanded spend visibility with support for additional Azure and AWS service lists.
-   **Version 9.0.2 - January 2026**
    -   This release addresses both functional and performance issues. Updates include:
        -   Support for multi-MID server configurations for customers using multiple AWS Organizations.
        -   Improved license calculation with correct handling of ephemeral resources.
        -   Faster load times for the CCM landing page.
        -   Business Hours recommendations now cover EC2 instances that are detached from Auto Scaling groups.
        -   More precise Azure forecast calculations for subscription-based billing, considering only the relevant service account.
        -   Budget configurations now remain intact and are not deleted automatically.
        -   Corrected GCP Business Hours actions for improved cost optimization.
        -   Expanded spend visibility with support for additional Azure and AWS service lists.
-   **Version 9.0.1 - October 2025**
    -   Functional and performance issues are fixed in this release. This includes:
        -   Forecast display on spend dashboard.
        -   Better formatting for amounts.
        -   Improved search and filtering capabilities for reports.
        -   Better error handing for Azure billing download, price sheet, and test connections.
        -   Custom properties to filter out unwanted tags.
        -   Better forecasting for future budgets.
-   **Version 9.0.0 - August 2025**
    -   This version includes several improvements:
        -   The cost and usage data retrieval from Azure is now faster through the Azure Export method.
        -   The Azure Microsoft Customer Agreement \(MCA\) is used to improve spend reporting and offer recommendations for potential savings.
        -   The support for Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA has been added.
-   **Version 8.2.1 - April 2025**

    A few functional issues have been fixed.

-   **Version 8.2.0 - February 2025**

    As part of Cloud Cost Management 8.2 release, Security Directives and Defect fixes have been merged.

-   **Version 8.1.0 - November 2024**

    New architecture with improved performance and scalability.

-   **Version 8.0.0 - August 2024**

    New: Spend breakdown for AI Services for Amazon Web Services \(AWS\), Microsoft Azure, and Google Cloud Platform \(GCP\) providers.

-   **Version 6.0.1 - April 2024**
    -   Fixed:
        -   Unassigned count fix
        -   Duplicate notification fix for budget forecast failure
        -   AWS billing download failure while executing post-import billing data
        -   AWS right sizing metrics fix
-   **Version 6.0.0 - February 2024**
    -   New Features:
        -   Container Spend Management for
            -   AWS: Amazon Elastic Kubernetes Services \(Amazon EKS\)
            -   Azure: Azure Kubernetes Services \(AKS\)
            -   GCP: Google Kubernetes Engine \(GKE\)
        -   Shared Cost Allocation
            -   Compare Direct and Shared Costs across providers, service accounts, service categories, cloud services, regions, and so on.
            -   Shared costs for both Actual and Amortised Costs.
-   **Version 5.0.3 - January 2024**
    -   This is a patch release with fixes for the following providers:
    -   AWS:
        -   CI placement issue fix for resources with the same object or resource ID.
        -   AWS billing download fix for AWSGlue resource ID.
        -   Pricesheet download timeout fix.
    -   Azure:
        -   Azure Rightsizing fixes for core subflow execution.
        -   Regulated market URL fix.
        -   Nested tags with incorrect format fix.
    -   Google:
        -   Missing Rightsizing recommendations fix.
        -   Business Hours Insights executions flow fix.
        -   Spend mismatch issue fix.
-   **Version 3.1.3 - January 2024**

    In this release, Empty ACLs are fixed.

-   **Version 5.0.0 - August 2023**
    -   New:
        -   New UI \(Workspace\)
        -   Storage optimization
        -   Database optimization
        -   Admin centre and guided setup\(to help set up the app easily\)
        -   Service graph connector support \(azure and GCP in testing\)
        -   Cost reporting on data on a longer time range than before
    -   Changed: Legacy UI is set to deprecate in a couple of releases \('X' release\)
-   **Version 3.1.2 - June 2023**

    Fixes to address couple of customer issues.

-   **Version 3.1.1 - March 2023**

    This is a patch release which incorporates fixes.

-   **Version 3.1.0 - November 2022**

    This is a minor release which incorporates Azure API change and fixes.

-   **Version 3.0.0 - June 2022**

    New: Support for Google Cloud

-   **Version 2.2.0 - November 2021**

    New: Reserved instance \(RI\) support: Cloud service providers offer discount pricing for certain resources at a particular level of use for a fixed period. Providers use various names for this offering: “reserved instance plans”, “committed use plans”, or “savings plans”. Cloud Insights integrates with the provider recommendations for resources that would cost less under such plans.

-   **Version 2.1.0 - September 2021**
    -   New:
        -   Budgets
        -   Amortized spend
-   **Version 2.0.0 - May 2021**
    -   Fixed:
        -   Cost reports enable you to view data based on provider cost tags.
        -   Cloud Insights supports AWS billing data in both hourly and daily granularities. You can configure the AWS Time granularity setting as either Daily or Hourly.
        -   Cost Optimization feature - The Business Hours feature supports Daily AWS billing data.
        -   Spend analytics features support environments that do not use the ServiceNow Discovery application. You have the option to use a third-party discovery source.
        -   For any provider, you have the option to use only specified MID Servers when performing actions like downloading billing data, performing discovery, or performing actions that are recommended by Cloud Insights.
        -   Two Automatic Test Framework \(ATF\) tests now verify upgrades.
-   **Version 1.3.1 - December 2020**
    -   Fixed:
        -   Azure billing download for special characters.
        -   Azure Pricesheet and Azure Balance Summary API fix for double digit months.
        -   Code adjustments to absorb IntegrationHub and MetricBase changes to work with Paris and later.
-   **Version 1.3.0 - October 2020**
    -   New: Gov support for AWS and Azure
    -   Fixed:
        -   Multi-currency fix for Azure, AWS spend reports to include tax and fees
        -   Pivot key changes fix \(KB article\)
-   **Version 1.2.0 - June 2020**
    -   New:
        -   Cloud Insights v1.2.0 supports Microsoft Azure:

            All Cloud Insights features are supported on Microsoft Azure. Appropriate features include a Provider filter to enable you to specify Microsoft Azure.

        -   Azure property setting:

            You can specify the batch size for Azure actions like Stop, Start, Modify \(resize\), Terminate, and Describe.

        -   Assign service accounts to an Insights Owner:

            Assign responsibility for all resources in one or more service accounts to an Insights Owner. You can assign ownership of one or more service accounts and, optionally, the related CIs to users that have the Insights Owner role. An Insights Owner can define jobs and policies and can view data for owned service accounts.

        -   Unused Machines feature:

            The Unused Machines feature analyzes usage data to identify resources that are wasting money because they are not used. You schedule Unused Machines jobs to power-off or terminate the resources you specify.

    -   Changed:
        -   Policy Precedence setting:

            The Precedence setting determines the order in which groups of policies are applied — by policy type. Policy types reflect the role of the user who created the policy — Cloud Insights Admin or Insights Owner. If a resource matches a policy with precedence, no other policy is applied to the resource.

        -   Policy cards and the Policy list display provider and creator information.
        -   Use the Provider and Service Account filters to focus the data that appears in reports.
        -   Auto Scaling group resources are excluded from Cloud Insights operations:

            AWS Auto Scaling group \(ASG\) operations act to maintain minimum capacity for ASG-member resources. To avoid conflicts with ASG operations, the Cloud Insights app excludes all instances that are part of an Auto Scaling group from Rightsizing, Unused Machines, and Business Hours operations.

        -   Billing Download jobs run daily:

            Billing Download jobs are scheduled to run daily at the time of day that you specify.

        -   Policy view is organized by policy creator:

            Policies are divided into two sections based on the creator of the policy. On both the card view and list view, the top section includes all policies that were created by users with your role \(Cloud Insights Admin or Insights Owner\). The next section includes all other policies.

-   **Version 1.1.0 - January 2020**

    -   New: Rollback on failed Rightsizing attempts. If a Rightsizing action fails, the system immediately performs a rollback to return the resource to its original size, restarts the resource if needed, updates the change request with full details, and updates Rightsizing report data.
    -   Removed: For AWS accounts, only costs of the unblended type are supported. The Cost Type field no longer appears on the Billing Download Job form.
    **Important:** To upgrade Cloud Cost Management from version 1.0 to 1.1, follow the upgrade instructions in the product documentation.

-   **Version 1.0.0 - November 2019**
    -   The Cloud Insights application enables you to analyze the full range of costs associated with your cloud assets so you can identify and take action on opportunities to optimize operations and save money.
    -   Cloud Insights generates detailed and readily-understood cost analytics reports that you can filter as needed. You can make meaningful cost comparisons because Cloud Insights normalizes your organization’s entire cloud spend.
    -   Cloud Insights enables you to optimize cloud spend by identifying underused and over-provisioned assets and providing you the choice of automated or semiautomated rightsizing operations.
    -   To eliminate the uncertainty associated with ownerless assets, Cloud Insights uses your policies to assign ownership to cloud resources and auto-update the CMDB. Spend reports now include all assets in your cloud infrastructure.
    -   Each feature is fully integrated with ServiceNow’s change management system.

