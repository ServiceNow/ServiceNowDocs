---
title: Navigating breakdown elements with breakdown relations
description: Breakdown relations open a new navigation path for viewing breakdown scores, by moving from one breakdown element to another element of the same breakdown. The elements should be in an hierarchical relationship.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/breakdown-relations.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Navigating breakdown elements with breakdown relations

Breakdown relations open a new navigation path for viewing breakdown scores, by moving from one breakdown element to another element of the same breakdown. The elements should be in an hierarchical relationship.

**Important:** Platform Analytics features other than indicator scorecardsdo not support breakdown relations.

You can use breakdown relations to navigate between the elements of a single breakdown that are in a hierarchical relationship. For example, the Location breakdown has a hierarchy of 'parent' and 'child' elements, where a country can be the parent of cities. Breakdown relations let an Analytics Hub viewer navigate from a country down into a city, from a city to the country, or between cities in the same country.

In Platform Analytics, breakdown relations can be applied only on indicator scorecards. The latest version of the Data Visualizations application from the ServiceNow® Store is required. In the Core UI, breakdown relations affect navigation on the Analytics Hub and in breakdown widgets.

## Breakdown relations on Next Experience dashboards

An indicator scorecard on a Next Experience dashboard can show hierarchical or breakdown-to-breakdown relations. You must pair the indicator scorecard with a filter on the dashboard. The filter source is the table that is the breakdown source, and the filter applies to indicators with that breakdown. The filter acts as the source, and the scorecard breakdown acts as the target. The relation record defines how these two are connected. Within that connection, the breakdown elements from the filter are mapped to fields on the target scorecard's breakdown elements. That mapping is what the breakdown relation record defines. In short: filter → breakdown relation → scorecard breakdown, with element-level field mappings in between.

For a hierarchy of elements on the same breakdown, the filter source must be the same as the breakdown source. For example, if the indicator scorecard shows indicators with the Assignment Group breakdown, the dashboard filter must filter on the Group table. It also must filter indicators with the Assignment Group breakdown.

\[Omitted image "bkdwn-relations-ind-scorecard.gif"\] Alt text: Dashboard using an Assignment Group filter and an Indicator scorecard with the Assignment group breakdown to show the difference when breakdown relations are followed and between sibling and parent relations.

Breakdown-to-breakdown relations define different primary and related breakdowns. To show such a relation on a Platform Analytics dashboard, the indicator scorecard uses the related breakdown. The filter is based on the primary breakdown, so is identical to what you create for a hierarchical relation. For example, you can filter on the Hardware assignment group and configure the indicator scorecard to use the Assigned To breakdown. As a result, the indicator scorecard shows the members of the Hardware group.

\[Omitted image "bkdown2bkdown-relation.png"\] Alt text: Dashboard using an assignment group filter to show the members of an assignment group in an indicator scorecard with the Assigned To breakdown.

## Breakdown relations in Core UI breakdown widgets

A Core UI breakdown widget can show the parent, child, or sibling elements of the element that was chosen for the breakdown dashboard. For more information about using breakdown relations on breakdown dashboards, see [Showing breakdown relations on dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_ShowBkdwnRltnsWdgts.md).

\[Omitted image "Breakdown\_relations\_widget.png"\] Alt text: A breakdown dashboard with a breakdown widget showing the child elements of the EMEA element

-   **[Create relations between elements of a breakdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-relation-btwn-bkdn-elements.md)**  
Use a breakdown relation to set up navigation between a hierarchy of elements within the same breakdown. A field in the breakdown records must identify the hierarchical relationship of one record to another.
-   **[Create a breakdown-to-breakdown relation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_CreateABreakdownRelation.md)**  
To set up navigation in a visualization between the elements of two breakdowns at the same level, create a breakdown relation between the breakdowns. A table must exist with fields that reference the records for both breakdowns.

**Parent Topic:**[Indicator breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_CreatingBreakdowns.md)

**Related topics**  


[Create an Indicator Scorecard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-dv-indicator-scorecard.md)

[Create or add a filter on an inline dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/select-workspace-filter-type.md)

[Breakdown widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/breakdown-widgets.md)

