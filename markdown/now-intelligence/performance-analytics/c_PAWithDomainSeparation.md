---
title: Domain separation and Performance Analytics
description: Domain separation is supported for Performance Analytics. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. Performance Analytics supports collecting scores from multiple domains and can be configured to enable domain-specific administration. Extended domain configuration functionality is available for customers with complex domains.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Domain separation and Performance Analytics

Domain separation is supported for Performance Analytics. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. Performance Analytics supports collecting scores from multiple domains and can be configured to enable domain-specific administration. Extended domain configuration functionality is available for customers with complex domains.

## Support level: Enhanced

-   Includes all aspects of **Basic** and **Standard** levels of support.
-   Data-driven process enables service provider customers to modify business logic that is based on defined use cases. These configurations are UI-based and fail-safe so that configurations by one customer cannot affect another.
-   Tenants of the instance must be able to configure minimum viable product \(MVP\) business logic and data parameters for themselves. This logic and parameters would be expected for the application's normal function.

Sample use case: Tenant-customers of a shared environment must be able to modify the impact, urgency, or priority matrix to set priority within their domain.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Requirements

-   A fully enabled, subscription version of Performance Analytics. See [Activating your Performance Analytics subscription](c_PremiumPerformanceAnalytics.md#).
-   The Domain Support — Domain Extension Installer plugin.

**Warning:** Instances with a large number of domains, as is typical for multiple service providers \(MSPs\), can experience performance degradation when retrieving Performance Analytics scores. For a potential solution, see [KB1516963](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1516963). Access to Now Support is required.

## Approaches to domain separation

There are three approaches to domain separation in Performance Analytics:

-   **Global**

    The Performance Analytics records, such as indicators and breakdowns, are all in the global domain. Data collection jobs respect the domains of facts table records, such as incidents, when they collect indicator scores. Users see scores only from domains they have visibility into. Platform Analytics Solutions use this approach. It is the most suitable approach in most cases.

-   **Domain-specific**

    The Performance Analytics records themselves are domain-separated. Each domain has users with pa\_admin and other roles for managing Performance Analytics.

-   **Hybrid**

    Low-level Performance Analytics records, such as indicator sources, are global. High-level Performance Analytics records, such as widgets, are domain-separated. The pa\_admin users manage the low-level, global records. Each domain has users with roles like pa\_power\_user to manage high-level records. This approach is advanced.


For more information, see:

-   [Approaches to Performance Analytics with domain separation](pa-domain-configurations.md)
-   [Performance Analytics for Managed Service Providers](https://community.servicenow.com/community?id=community_blog&sys_id=e59bf10adbb7d4d04aa5d9d96896197d)
-   [SPM Project Portfolio Management, Domain Separation and Managed Service Providers](https://community.servicenow.com/community?id=community_article&sys_id=616d706edbb318d066f1d9d9689619c1)

## Extended functionality for complex domains

You can extend the domain separation support for Performance Analytics with the following features, designed especially for customers with complex domains to manage:

-   **Hierarchical multi-domain configurations**

    Group domains together, based on their visibility to a user group or on other conditions. Collect scores on some, all, or none of the child domains of these domains. Decide whether to roll up child domain scores to the parent domain, and whether for all children or only those explicitly in the configuration.

-   **Collect aggregate scores**

    Combine scores from the multiple domains in a domain configuration to create an aggregate score.

-   **Dashboard filtering by domain**

    Filter dashboards to show scores by domain or domain aggregate, as you would by breakdown.


The extended functionality is available in the Performance Analytics — Domain Separation Support plugin. The general requirements for domain separation in Performance Analytics also apply.

Extended functionality supports only the global approach to domain separation.

For more information about this extended functionality, see: [Grouping domains in Performance Analytics domain configurations](pa-domain-separation-msp.md)

-   **[Approaches to Performance Analytics with domain separation](pa-domain-configurations.md)**  
When using Performance Analytics with domain separation, you can collect domain-specific scores. You can use global or domain-specific Performance Analytics table records or even a combination of both.
-   **[Grouping domains in Performance Analytics domain configurations](pa-domain-separation-msp.md)**  
Instead of configuring Performance Analytics for the domains of a specific user, create a reusable domain configuration. Select domains that are visible to a group of users, or filter domains directly. Domain configurations let you define hierarchical relationships and aggregate scores across multiple domains.
-   **[PADomainUtils - Global](../../../app-store/dev_portal/API_reference/PADomainUtils/concept/c_PADomainUtils.md)**  
The PADomainUtils API enables you to copy Performance Analytics records between different domains on the same instance.

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

