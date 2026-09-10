---
title: Cloud Cost Management Infra Stack release notes
description: Version history for the Cloud Cost Management Infra Stack application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itam-cloud-cost-mgmt-infra-stack.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - IT Asset Management version history release notes, ServiceNow Store version history release notes]
---

# Cloud Cost Management Infra Stack release notes

Version history for the Cloud Cost Management Infra Stack application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.0.0 - September 2026**
    -   The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views.
    -   What's new
        -   Make smarter cloud cost decisions with AI-powered summarization of cloud spend
        -   Get complete cost visibility with TCO and unit economics
        -   Manage cloud spend attribution with the tag category source selection capability
        -   Streamline spend analysis with saved, shared, and reusable report views
        -   Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility
    -   What's changed
        -   The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers.
        -   The Business Insights view has been added to the Cloud Cost Management Workspace
        -   Saved views on the Cloud Cost Management Workspace
        -   Optimization view on the Cloud Cost Management Workspace
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
    -   Functional and performance issues are fixed in this release. This includes:
        -   Multi-MID server configuration support for customers with multiple AWS Organizations.
        -   Accurate license calculation with proper handling of ephemeral resources.
        -   Improved CCM landing page performance with faster load times
        -   Business Hours recommendations now include EC2 instances detached from Auto Scaling groups.
        -   Accurate Azure forecast calculation for subscription-based billing \(now considers only the relevant service account\).
        -   Budget configurations now retain correctly without automatic deletion.
        -   Fixed GCP Business Hours actions for proper cost optimization execution.
        -   Enhanced spend visibility with support for additional Azure and AWS service lists.
-   **Version 9.0.2 - January 2026**
    -   Functional and performance issues are fixed in this release. This includes:
        -   Multi-MID server configuration support for customers with multiple AWS Organizations.
        -   Accurate license calculation with proper handling of ephemeral resources.
        -   Improved CCM landing page performance with faster load times
        -   Business Hours recommendations now include EC2 instances detached from Auto Scaling groups.
        -   Accurate Azure forecast calculation for subscription-based billing \(now considers only the relevant service account\).
        -   Budget configurations now retain correctly without automatic deletion.
        -   Fixed GCP Business Hours actions for proper cost optimization execution.
        -   Enhanced spend visibility with support for additional Azure and AWS service lists.
-   **Version 9.0.1 - October 2025**

    Functional and performance issues are fixed in this release. This includes:

    -   Forecast display on spend dashboard.
    -   Better formatting for amounts.
    -   Improved search and filtering capabilities for reports.
    -   Better error handing for Azure billing download, price sheet, and test connections.
    -   Custom properties to filter out unwanted tags.
    -   Better forecasting for future budgets.
-   **Version 9.0.0 - August 2025**

    As part of 9.0, the following features are supported. Azure MCA contract support Azure billing download using export option.

-   **Version 8.2.2 - June 2025**

    Fixes for infra stack plug in.

-   **Version 8.2.1 - April 2025**

    A few functional and performance issues have been fixed.

-   **Version 8.2.0 - February 2025**

    Cloud Cost Management \(CCM\) Infra stack app cannot be installed without Cloud cost management parent app. This application installs additional shared services dependencies for the new architecture to improve the performance and scalability of CCM.

-   **Version 8.1.0 - November 2024**

    The Cloud Cost Management \(CCM\) Infra stack application deploys the shared services architecture to enhance the performance and scalability of CCM.It has a dependency on the parent Cloud Cost Management app.


