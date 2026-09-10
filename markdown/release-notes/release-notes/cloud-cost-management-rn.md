---
title: Cloud Cost Management release notes
description: The ServiceNow Cloud Cost Management application \(formerly known as ServiceNow Cloud Insights\) helps you to analyze the cloud resource costs so that you can identify and act on opportunities to save money and optimize the operations of your organization. Cloud Cost Management was enhanced and updated in the Zurich release.The Version 11.0.0 release introduces AI-powered summarization of cloud spend, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation, and reusable saved views.The Version 10.0.0 release introduces support for the FinOpsOpen Cost and Usage Specification \(FOCUS\) billing standard, the flexibility to view your cloud cost data in your preferred local currency, and centralized visibility into Azure Cloud Solution Provider \(CSP\) spend.The ServiceNow Cloud Cost Management application \(formerly known as ServiceNow Cloud Insights\) helps you to analyze the cloud resource costs so that you can identify and act on opportunities to save money and optimize the operations of your organization. Cloud Cost Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# Cloud Cost Management release notes

The ServiceNow® Cloud Cost Management application \(formerly known as ServiceNow Cloud Insights\) helps you to analyze the cloud resource costs so that you can identify and act on opportunities to save money and optimize the operations of your organization. Cloud Cost Management was enhanced and updated in the Zurich release.

## About Cloud Cost Management

-   Retrieve cost and usage data faster from the Azure billing download by using the Azure Export method.
-   Leverage Azure Microsoft Customer Agreement \(MCA\) to optimize spend reporting and recommendations for potential savings.

See [Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/cloud-insights-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Cloud Cost Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    The Cloud Cost Management platform support is available beginning with the Xanadu release. For instructions on upgrading Cloud Cost Management to Zurich, see [Upgrade Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/upgrade-cloud-insights-to-version-3-0.md).


## Accessibility and localization

-   **Accessibility information**
    -   **Dark theme**

        The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[IT Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-asset-management-rn-landing.md)

## Version 11.0.0

The Version 11.0.0 release introduces AI-powered summarization of cloud spend, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation, and reusable saved views.

### What's new

-   **Get complete cost visibility with TCO and unit economics**

    Enhance total spend analysis with TCO insights for your business applications by combining cloud costs with non-cloud costs such as hardware, software licensing, and labor. Upload business data to track revenue, units, and margins alongside your cloud costs using the Unit Economics view. Use the new Business Insights view to analyze spending trends by application owner, business application, department, business unit, and cost center.

-   **Get complete cost visibility with TCO and unit economics**

    Enhance total spend analysis with TCO insights for your business applications by combining cloud costs with non-cloud costs such as hardware, software licensing, and labor. Upload business data to track revenue, units, and margins alongside your cloud costs using the Unit Economics view. Use the new Business Insights view to analyze spending trends by application owner, business application, department, business unit, and cost center.

-   **Manage cloud spend attribution with the tag category source selection capability**

    Align cloud spend attribution with your organization's enterprise architecture \(EA\) by selecting a tag category source. Instead of manually tagging resources in each cloud provider, derive business context automatically from existing CMDB relationships. This feature eliminates duplicate tagging effort and ensures that cost reports reflect the same taxonomy already maintained in your ServiceNow instance.

-   **Streamline spend analysis with saved, shared, and reusable report views**

    Eliminate repetitive setup using Spend analytics filters, time ranges, groupings, and cost types and apply your saved views instantly without manual reconfiguration. Set a default view to load your preferred configuration automatically every time you open the Spend Analytics page. Mark frequently used views as favorites or set a default view to streamline your daily workflow.

-   **[Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/ci-workspace.md)**

    Navigate cloud cost data more efficiently with a reorganized structure within the Cloud Cost Management Workspace. Drill down from any home page widget directly into detailed spend analytics.

    This enhancement provides the Insights User \(insights\_user\) role read-only access to Optimization and Budget pages so they can review recommendations, unused resources, rightsizing suggestions, and budget data.


### What's changed

-   **Optimization view on the Cloud Cost Management Workspace**

    The Recommendations have been moved from the Operations view to the newly added Optimization view in the Cloud Cost Management Workspace. The Optimization view shows savings opportunities and recommendations for you across Unused resources, Rightsizing, Business hours, and Commitments.


### Plugin information

-   **Plugins planned for deprecation**

    Cloud Cost Management \(sn\_clin\): Planned for deprecation in a future release. Use the Cloud Cost Management Infra Stack application that includes related ServiceNow® Store applications and plugins if they aren’t already installed.


## Version 10.0.0

The Version 10.0.0 release introduces support for the FinOpsOpen Cost and Usage Specification \(FOCUS\) billing standard, the flexibility to view your cloud cost data in your preferred local currency, and centralized visibility into Azure Cloud Solution Provider \(CSP\) spend.

### What's new

-   **[Gain insights from your billing data with the FOCUS standard for Microsoft Azure billing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/schedule-azure-billing-job.md)**

    Enhance your ability to manage cloud costs using the FOCUS billing standard that enables better insights. This feature helps you make more informed decisions. Additionally, you experience seamless processing of billing data across multiple Azure billing models such as:

    -   Enterprise Agreement \(EA\)
    -   Microsoft Customer Agreement \(MCA\)
    -   Microsoft Partner Agreement \(MPA\)
-   **[View cloud cost data in your preferred currency for multiple cloud service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/operation-view-ccm-ws.md)**

    View your cloud cost data in your preferred local currency for better clarity and reporting flexibility. This capability enables you to view cost and usage details from multiple cloud service providers, including AWS, Azure, and GCP, in your selected currency.

-   **[Get support for your Azure MPA model when operating under an MSP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/azure-pricesht-sched-dwnld-cloudin.md)**

    Gain full visibility into your cloud costs and actionable insights for your Azure cloud spend when operating under an MSP. Additionally, the feature provides a centralized view to monitor cloud spend and manage budgets.


### What's changed

-   **[Granular instance operator role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/cloud-insights-roles.md)**

    Use the instance operator role to perform routine operational tasks without requiring the full admin role for basic operations. By using limited privileges in the instance operator role, you can help reduce security risks across your organization.


## Version 9.0.0

The ServiceNow® Cloud Cost Management application \(formerly known as ServiceNow Cloud Insights\) helps you to analyze the cloud resource costs so that you can identify and act on opportunities to save money and optimize the operations of your organization. Cloud Cost Management was enhanced and updated in the Zurich release.

### What's new

-   **[Achieve better efficiency with faster retrieval of cost and usage data with the Azure Export method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/schedule-azure-billing-job.md)**

    Manage cost and usage datasets in Azure billing downloads efficiently by using the Azure Export method. With this feature, you can retrieve larger cost datasets faster.

-   **[Manage MCA contracts with the enhanced support for Microsoft Azure MCA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/create-ms-azure-service-principal.md)**

    Gain access to the spend reporting and recommendations for Azure based MCA contracts. This feature helps you to visualize cost and usage data from Azure MCA accounts and optimize your cloud spend with recommendations for potential savings.


### What's changed

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Use Exports option on the Azure Billing Download Job form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/schedule-azure-billing-job.md)**

    The **Use Exports** option is selected by default. This option is used for the Azure Export method.

-   **[New fields on the Azure Billing Download Job form when the Use Exports option is selected](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/schedule-azure-billing-job.md)**

    Three new fields, **Billing Account Id Type**, **Actual Cost Export Name**, and **Amortized Cost Export Name**, have been added to the Azure Billing Download Job form. These fields appear when the **Use Exports** option is selected.


### What's deprecated or removed

The current mechanism for the Azure billing download is planned for deprecation. With this deprecation, the Export option remains the default method for the Azure billing download.

