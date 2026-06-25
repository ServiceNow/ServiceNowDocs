---
title: Create a domain filter
description: Create a domain filter so that you can filter data visualizations on domains in a domain-separated instance. Domain filters enable the user to see data associated with one or more domains.Domain filters based on Performance Analytics domain configurations behave differently than domain filters based on the list of platform domains.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/create-domain-filter.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Filters, Platform Analytics experience, Platform Analytics]
---

# Create a domain filter

Create a domain filter so that you can filter data visualizations on domains in a domain-separated instance. Domain filters enable the user to see data associated with one or more domains.

## Before you begin

Domain filters are available on instances with domain separation enabled. Domain filters are not automatically enabled by default. To enable them, install these two plug-ins:

-   com.glide.domain.msp\_extensions.installer
-   com.snc.pa.domain\_support

For more information, see [Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md). Domain filters are a different component than the Filter component.

Role required: ui\_builder\_admin or admin.

## About this task

Domain filters support both the instance's list of domains and Performance Analytics domain configurations. Filters based on the domain list provide different results than filters based on domain configurations. For more information, see [Differences between domain list and domain configuration filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-domain-filter.md).

The filter applies to all elements on the same dashboard or the same dashboard tab, depending on filter placement. Filters on dashboard tabs have higher priority than top-level filters.

## Procedure

1.  Open **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Locate the dashboard in the dashboard library and open it for editing, as described in [Edit Platform Analytics dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/edit-db-in-ac.md).

    **Note:** These instructions are for using the inline dashboard editor. If you’re editing a technical dashboard in the UI Builder, see the [Component reference](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/shared-components/sn-pa-domain-filter/overview) on the Developer Site.

3.  Create or open the dashboard that you want to add a domain filter to.

    For more information, see [Edit Platform Analytics dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/edit-db-in-ac.md).

4.  Select **Edit**.

5.  From the **Add new element** menu, select **Domain filter**.

    The domain filter is added to the dashboard layout in the first available space. This location may be below existing dashboard elements.

6.  Select the domain filter's three-dot menu and choose **Configure**.

    \[Omitted image "config-domain-filter-ie.png"\] Alt text: Domain filter container with More actions menu open and Configure option highlighted

7.  In the **Filter label** field, type a meaningful name for the filter.

    This name is the name that the user sees.

8.  To determine what data to display in your filter, configure the domain display and whether to include domain data.

    1.  Select the **Domain display**.

        You can filter on either a Performance Analytics domain configuration or a standard domain list.

        \[Omitted image "domain-filter-config.png"\] Alt text: Domain filter configuration panel with Domain display list expanded.

        |Options|Description|
        |-------|-----------|
        |Use the Performance Analytics domain configuration|Enables users to filter results based on a domain configuration. To learn more about domain configurations, see [Grouping domains in Performance Analytics domain configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-domain-separation-msp.md).|
        |Use the standard domain list|Enables users to filter results based on the list of domains. The list shows only active domains. Aggregations aren’t included.|

        For a more detailed description of how these properties affect the results of the filter, see [Differences between domain list and domain configuration filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-domain-filter.md).

    2.  Choose whether to **Include global domain data**.

        When selected, the filter includes values from records in the global domain. The global domain usually contains only configuration records.

9.  Select **Save**.


**Parent Topic:**[Filters in Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/interactive-filters-workspace.md)

**Related topics**  


[Create or add a filter on an inline dashboard]()

[Create a filter in the Filter Designer]()

[Create a filter group]()

[Create a filter on a technical dashboard in UI Builder]()

[Make a data visualization act as a filter]()

[Configure a Single/Multiple select or cascading filter]()

[Configure a True/False filter]()

[Configure a Date filter in the inline editor]()

[Edit a Platform Analytics filter on a dashboard]()

[Platform Analytics filter tables]()

## Differences between domain list and domain configuration filters

Domain filters based on Performance Analytics domain configurations behave differently than domain filters based on the list of platform domains.

### Overview of differences

The results of domain filtering differ based on the presence of child domains and the inclusion of the global domain. If you use domain configurations, results also depend on aggregation.

### Platform domain list

-   **Global domain included**
    -   **Visualizations based on indicator data**

        Show only the scores for the selected domain. Child domain and global domain scores are not included. The values can come from both [data collection jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md) and manual input.

    -   **Visualizations based on table data or [database views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md)**

        Combine the values of the global and selected domains, and any child or parent domains.

-   **Global domain not included**
    -   **Visualizations based on indicator data**

        Show only the score for the selected domain. Child domain and global domain scores are not included.

    -   **Visualizations based on table data or database views**

        Combine the values of the selected domain and the values of the child domains.


### Performance Analytics domain configurations

See [Grouping domains in Performance Analytics domain configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-domain-separation-msp.md) for a detailed discussion of domain configurations.

Once you group domains in a Performance Analytics domain configuration, there are two considerations when you filter on a domain in that configuration:

-   Does the domain have children or is it a standalone domain?
-   Is the data aggregated?

-   **Global domain included**
    -   **Visualizations based on indicator data**

        Show only the scores for the selected domain, and only if a data collection job collected indicator scores for that domain.

        Aggregated scores come from all domains in the domain configuration, but exclude child domains. The global domain is also excluded.

    -   **Visualizations based on table data or database views**

        Include values from the selected domain, any child domains of that domain, and the global domain.

        Aggregated results come from all domains in the configuration, including their child domains, plus the global domain.

-   **Global domain not included**
    -   **Visualizations based on indicator data**

        Show only the scores for the selected domain. Child domains and the global domain are excluded.

        Aggregated scores come from all domains in the domain configuration, but exclude child domains. The global domain is also excluded.

    -   **Visualizations based on table data or database views**

        Include the values of the selected domain and children of the selected domain, if present. Global domain values are not included.

        Aggregated results come from all domains in the domain configuration plus any children of domains in that configuration. Global domain values are not included.


**Related topics**  


[Approaches to Performance Analytics with domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-domain-configurations.md)

