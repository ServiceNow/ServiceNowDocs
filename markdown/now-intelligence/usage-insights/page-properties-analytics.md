---
title: Page properties analytics
description: Page properties are metadata attributes that describe a page, such as the page name, owning team, language, or category. By enriching pages with properties, you can segment usage data by attributes that are meaningful to your organization instead of by page identifier alone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/usage-insights/page-properties-analytics.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: concept
last_updated: "2026-08-25"
reading_time_minutes: 3
keywords: [page properties]
breadcrumb: [Viewing session analytics, Using Usage Insights, Usage Insights, Platform Analytics]
---

# Page properties analytics

Page properties are metadata attributes that describe a page, such as the page name, owning team, language, or category. By enriching pages with properties, you can segment usage data by attributes that are meaningful to your organization instead of by page identifier alone.

## Pages and events

A page property is a named, filterable attribute captured from the URL parameters or record metadata of a page on every page view. Page properties let you distinguish pages that share a single page identifier, so that you can analyze usage by the resource a person actually viewed. Usage Insights represents user activity as pages and events:

-   A page is a view that a user opens.
-   An event is an interaction that a user performs on that page, such as adding a comment, selecting a link, or liking an article.

Opening a page generates page data. Every subsequent interaction on that page generates events. Because events occur on a page, every event now carries page properties alongside its own event properties. This is why page properties are available even when a filter condition is built on an event: the combination answers questions such as which pages a given event is being raised from.

## The problem page properties solve

Many pages share one page identifier. Every knowledge article opens in the same article view, every catalog item in the same catalog view, and every dashboard in the same dashboard view. Without page properties, a page view records only that identifier, so all of those visits are indistinguishable in analytics. So, anyone analyzing the data must perform a separate lookup to learn what the article is.

Page properties record the attributes that differentiate one visit from another, such as the article title, the page category, or the page owner. With those attributes available as filters, you can analyse:

-   How many password reset requests were submitted by people who visited the password reset catalog page?
-   How many comments were added to the knowledge article titled `Usage Insights MCP`?
-   Which dashboards did people visit last quarter, listed by name?

**Important:** Support for event properties has been available since the initial release of Usage Insights. Page properties extend the same capability to pages. Minimum version required is Brazil patch 0 and Australia patch 6.

## Where page properties are available

-   **Filter bar**

    A **Page** filter has been added. Select a page, and then filter by that page's properties alongside events.

-   **Properties section**

    The value distribution for each page property renders as a chart, below the event property distributions and in the same format.

-   **Sessions**

    Page properties are available as filter fields, including when the condition is built on an event. This combination answers questions such as which pages a particular event is being raised from.

-   **Events**

    Page properties are available as filter fields, so that you can identify the pages that generated a given set of events.

-   **Pages menu**

    A dedicated page properties view shows the distributions for a single page and lets you filter that page by an individual property.

-   **Advanced filters**

    Select a page, and then choose its properties from the field list to build a condition.

-   **Conversion funnels**

    When a funnel step is set to a page, that page's properties is set to available for the step, so that drop-off is calculated for the filtered subset. For example, a step can be limited to visits where the article title is `Password reset`.


## How to read a page property distribution

Each chart represents one property. The segments show the distinct values recorded for that property, and the legend shows the count and percentage for each value. The center of the chart shows the total number of occurrences in the selected date range.

## Default and custom properties

Usage Insights captures a set of properties for each page by default, including the page identifier and selected system parameters. You can customise additional properties to retrieve more relevant data.

-   **[Using page properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/using-page-properties.md)**  
Filter a page detail page by one or more page properties to see how usage differs across page attributes such as owner, category, or load time.

**Parent Topic:**[Viewing session analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/viewing-sessions.md)

