---
title: Cloud Cost Management release notes
description: The ServiceNow Cloud Cost Management application \(formerly known as ServiceNow Cloud Insights\) helps you to analyze the cloud resource costs so that you can identify and act on opportunities to save money and optimize the operations of your organization. Cloud Cost Management was enhanced and updated in the Australia release.The Version 11.0.0 release introduces AI-powered summarization of cloud spend, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation, and reusable saved views.The Version 10.0.0 release introduces support for the FinOpsOpen Cost and Usage Specification \(FOCUS\) billing standard, the flexibility to view your cloud cost data in your preferred local currency, and centralized visibility into Azure Cloud Solution Provider \(CSP\) spend.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Cloud Cost Management release notes

The ServiceNow® Cloud Cost Management application \(formerly known as ServiceNow Cloud Insights\) helps you to analyze the cloud resource costs so that you can identify and act on opportunities to save money and optimize the operations of your organization. Cloud Cost Management was enhanced and updated in the Australia release.

## About Cloud Cost Management

-   Gain visibility by discovering cloud resources from all service providers across your environment.
-   Achieve resource optimization with analysis of cloud costs by cost center, business service, and custom entity.
-   Optimize cloud costs using recommendations to reduce unnecessary spending.

See [Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-insights-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Cloud Cost Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    The Cloud Cost Management platform support is available beginning with the Xanadu release. For instructions on upgrading Cloud Cost Management to Australia, see [Upgrade Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/upgrade-cloud-insights-to-version-3-0.md).


**Parent Topic:**[Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-asset-management-rn-landing.md)

## Version 11.0.0

The Version 11.0.0 release introduces AI-powered summarization of cloud spend, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation, and reusable saved views.

### What's new

-   **Make smarter cloud cost decisions with AI-powered summarization of cloud spend**

    Get an AI-generated summary of your cloud spend trends, top cost drivers, and budget alignment with your selected filters and groupings. The **Summarize** button enables you to view month-over-month changes, commitments coverage, and the top five recommendations to reduce costs. Use these insights to make more informed decisions about your cloud spend.

-   **Get complete cost visibility with TCO and unit economics**

    Enhance total spend analysis with TCO insights for your business applications by combining cloud costs with non-cloud costs such as hardware, software licensing, and labor. Upload business data to track revenue, units, and margins alongside your cloud costs using the Unit Economics view. Use the new Business Insights view to analyze spending trends by application owner, business application, department, business unit, and cost center.

-   **Get complete cost visibility with TCO and unit economics**

    Enhance total spend analysis with TCO insights for your business applications by combining cloud costs with non-cloud costs such as hardware, software licensing, and labor. Upload business data to track revenue, units, and margins alongside your cloud costs using the Unit Economics view. Use the new Business Insights view to analyze spending trends by application owner, business application, department, business unit, and cost center.

-   **Manage cloud spend attribution with the tag category source selection capability**

    Align cloud spend attribution with your organization's enterprise architecture \(EA\) by selecting a tag category source. Instead of manually tagging resources in each cloud provider, derive business context automatically from existing CMDB relationships. This feature eliminates duplicate tagging effort and ensures that cost reports reflect the same taxonomy already maintained in your ServiceNow instance.

-   **Streamline spend analysis with saved, shared, and reusable report views**

    Eliminate repetitive setup using Spend analytics filters, time ranges, groupings, and cost types and apply your saved views instantly without manual reconfiguration. Set a default view to load your preferred configuration automatically every time you open the Spend Analytics page. Mark frequently used views as favorites or set a default view to streamline your daily workflow.

-   **[Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/ci-workspace.md)**

    Navigate cloud cost data more efficiently with a reorganized structure within the Cloud Cost Management Workspace. Drill down from any home page widget directly into detailed spend analytics.

    This enhancement provides the Insights User \(insights\_user\) role read-only access to Optimization and Budget pages so they can review recommendations, unused resources, rightsizing suggestions, and budget data.


### What's changed

-   **Optimization view on the Cloud Cost Management Workspace**

    The Recommendations have been moved from the Operations view to the newly added Optimization view in the Cloud Cost Management Workspace. The Optimization view shows savings opportunities and recommendations for you across Unused resources, Rightsizing, Business hours, and Commitments.


### Plugin information

-   **New plugins**

    ServiceNow Otto for Cloud Cost Management \(com.sn\_now\_assist\_ccm\): Enables cloud resource admins and users to use the capabilities of generative AI skills in Cloud Cost Management.

-   **Plugins planned for deprecation**

    Cloud Cost Management \(sn\_clin\): Planned for deprecation in a future release. Planned for deprecation in a future release. Use the Cloud Cost Management Infra Stack application that includes related ServiceNow® Store applications and plugins if they aren’t already installed.


## Version 10.0.0

The Version 10.0.0 release introduces support for the FinOpsOpen Cost and Usage Specification \(FOCUS\) billing standard, the flexibility to view your cloud cost data in your preferred local currency, and centralized visibility into Azure Cloud Solution Provider \(CSP\) spend.

### What's new

-   **[Gain insights from your billing data with the FOCUS standard for Microsoft Azure billing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/schedule-azure-billing-job.md)**

    Enhance your ability to manage cloud costs using the FOCUS billing standard that enables better insights. This feature helps you make more informed decisions. Additionally, you experience seamless processing of billing data across multiple Azure billing models such as:

    -   Enterprise Agreement \(EA\)
    -   Microsoft Customer Agreement \(MCA\)
    -   Microsoft Partner Agreement \(MPA\)
-   **[View cloud cost data in your preferred currency for multiple cloud service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/operation-view-ccm-ws.md)**

    View your cloud cost data in your preferred local currency for better clarity and reporting flexibility. This capability enables you to view cost and usage details from multiple cloud service providers, including AWS, Azure, and GCP, in your selected currency.

-   **[Get support for your Azure MPA model when operating under an MSP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/azure-pricesht-sched-dwnld-cloudin.md)**

    Gain full visibility into your cloud costs and actionable insights for your Azure cloud spend when operating under an MSP. Additionally, the feature provides a centralized view to monitor cloud spend and manage budgets.


### What's changed

-   **[Multi-currency setup on the Operations view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/operation-view-ccm-ws.md)**

    The **Multi-currency setup** operation is available on the Cloud Cost Management Workspace Operations view to enable setting up display currency options for cloud cost and usage data.

-   **[Currency preference option on the Operations view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/operation-view-ccm-ws.md)**

    The **Currency preference** operation is available on the Cloud Cost Management Workspace Operations view to enable selecting preferred currency options for cloud cost and usage data.


-   **[Granular instance operator role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-insights-roles.md)**

    Use the instance operator role to perform routine operational tasks without requiring the full admin role for basic operations. By using limited privileges in the instance operator role, you can help reduce security risks across your organization.


