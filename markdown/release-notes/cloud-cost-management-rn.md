---
title: Cloud Cost Management release notes
description: The ServiceNow Cloud Cost Management application helps you to analyze cloud costs across your organization. It helps you to identify and act on opportunities to save costs and optimize operations. See the following sections for release notes by version.The Version 11.0.0 release introduces AI-powered summarization of cloud spend, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation, and reusable saved views.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/cloud-cost-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Asset Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Cloud Cost Management release notes

The ServiceNow® Cloud Cost Management application helps you to analyze cloud costs across your organization. It helps you to identify and act on opportunities to save costs and optimize operations. See the following sections for release notes by version.

## About Cloud Cost Management

-   Gain visibility by discovering cloud resources from all service providers across your environment.
-   Achieve resource optimization with analysis of cloud costs by cost center, business service, and custom entity.
-   Optimize cloud costs using recommendations to reduce unnecessary spending.

See [Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/cloud-insights-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Cloud Cost Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**
    -   The Cloud Cost Management platform support is available beginning with the Xanadu release. For instructions on upgrading Cloud Cost Management to Brazil, see [Upgrade Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/upgrade-cloud-insights-to-version-3-0.md).
    -   After upgrading to the Brazil release, review and reassess any ACL roles you have customized or deleted to confirm they reflect your expected access settings.
    -   Starting with the Brazil release, the sn\_change\_write role for Insights admin \(insights\_admin\) and Insights owner \(insights\_owner\) has been replaced with the sn\_change\_read role.

## Accessibility and localization

-   **Accessibility information**

    Accessibility improvements were completed across the Cloud Cost Management Workspace, including the homepage, Spend, Optimization, Operations, Admin, and Budget pages. Updates include corrected heading structure and improved drag-and-drop interaction support. These updates benefit screen reader users, keyboard-only users, and low-vision users navigating the Cloud Cost Management Workspace.


**Parent Topic:**[Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-asset-management-rn-landing.md)

## Version 11.0.0

The Version 11.0.0 release introduces AI-powered summarization of cloud spend, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation, and reusable saved views.

### What's new

-   **[Make smarter cloud cost decisions with AI-powered summarization of cloud spend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/spend-summary-otto-ccm.md)**

    Get an AI-generated summary of your cloud spend trends, top cost drivers, and budget alignment with your selected filters and groupings. The **Summarize** button enables you to view month-over-month changes, commitments coverage, and the top five recommendations to reduce costs. Use these insights to make more informed decisions about your cloud spend.

-   **[Get complete cost visibility with TCO and unit economics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/business-insights-ccm-ws.md)**

    Enhance total spend analysis with TCO insights for your business applications by combining cloud costs with non-cloud costs such as hardware, software licensing, and labor. Upload business data to track revenue, units, and margins alongside your cloud costs using the Unit Economics view. Use the new Business Insights view to analyze spending trends by application owner, business application, department, business unit, and cost center.

-   **[Manage cloud spend attribution with the tag category source selection capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/tag-category-source.md)**

    Align cloud spend attribution with your organization's enterprise architecture \(EA\) by selecting a tag category source. Instead of manually tagging resources in each cloud provider, derive business context automatically from existing CMDB relationships. This feature eliminates duplicate tagging effort and ensures that cost reports reflect the same taxonomy already maintained in your ServiceNow instance.

-   **[Streamline spend analysis with saved, shared, and reusable report views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/spend-anaytics.md)**

    Eliminate repetitive setup using Spend analytics filters, time ranges, groupings, and cost types and apply your saved views instantly without manual reconfiguration. Set a default view to load your preferred configuration automatically every time you open the Spend Analytics page. Mark frequently used views as favorites or set a default view to streamline your daily workflow.

-   **[Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/ci-workspace.md)**

    Navigate cloud cost data more efficiently with a reorganized structure within the Cloud Cost Management Workspace. Drill down from any home page widget directly into detailed spend analytics.

    This enhancement provides the Insights User \(insights\_user\) role read-only access to Optimization and Budget pages so they can review recommendations, unused resources, rightsizing suggestions, and budget data.


### What's changed

-   **[Optimization view on the Cloud Cost Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/optimization-view-ccm-ws.md)**

    The Recommendations have been moved from the Operations view to the newly added Optimization view in the Cloud Cost Management Workspace. The Optimization view shows savings opportunities and recommendations for you across Unused resources, Rightsizing, Business hours, and Commitments.


### Plugin information

-   **New plugins**

    ServiceNow Otto for Cloud Cost Management \(com.sn\_now\_assist\_ccm\): Enables cloud resource admins and users to use the capabilities of generative AI skills in Cloud Cost Management.

-   **Plugins planned for deprecation**

    Cloud Cost Management \(sn\_clin\): Planned for deprecation in a future release. Use the Cloud Cost Management Infra Stack application that includes related ServiceNow® Store applications and plugins if they aren’t already installed.


