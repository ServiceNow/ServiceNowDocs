---
title: Defining indicators and reports
description: On the KPI Composer Data Definition tab, you further specify the artifacts you defined during analysis and link them to indicator and report definitions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/performance-analytics/designing-indicators.html
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Design your indicator solution, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Defining indicators and reports

On the KPI Composer Data Definition tab, you further specify the artifacts you defined during analysis and link them to indicator and report definitions.

After you open the Data Definition tab, you see the same KPI tree that you defined in the Analysis tab. The header with personas and breakdown definitions and the footer with new artifacts are gone.

Each artifact that is associated with a Performance Analytics widget on the Dashboard Visualization should reference an indicator definition. Each artifact that is associated with a Reporting widget should reference a report definition. An artifact can be associated with both an indicator and a report definition. If a definition is missing, a clickable plus sign + appears with a message to create the definition. If the artifact is linked to any definitions, there is a hyperlink to open each definition.You can quickly get an overview of which artifacts are missing definitions by filtering on **Create definition**. \[Omitted image "kpi-composer-filter-create-def.png"\] Alt text: The filtering menus with Create Definition selected

The following illustration shows a measurement artifact that needs both a report and an indicator definition. An artifact definition named "% changes closed within SLA" is linked. The artifact still needs a report definition.

\[Omitted image "kpi-composer-data-def-artifact-tile.png"\] Alt text:

Before you create a new definition, see if a suitable definition already exists. Click on an artifact to open its properties. You see a read-only view of the properties you set on the Analysis tab, with one addition: You can link the artifact to an existing indicator and/or report definition. Start typing to populate the list of matching definitions. Linking existing definitions is simpler in the properties dialog than in the indicator or report definition records.

\[Omitted image "kpi-composer-data-def-measurement-props.png"\] Alt text: Properties of a measurement artifact in the data definition tab.

## Filtering

The following filter options are available on the Data Definition tab:

-   Filter by name, for filtering by one or more words that appear in the artifact name
-   Filter by task
-   Create definition, for filtering by whether an indicator or report definition is needed
-   Link PA Indicator, for filtering by artifacts with indicator definitions that are not linked to Performance Analytics indicators

\[Omitted image "kpi-composer-data-def-filters.png"\] Alt text: Filters on the Data Definition tab

## Indicator definitions

An indicator definition contains the description of how to develop a specific Performance Analytics indicator. The indicator definition itself is not a Performance Analytics indicator. The indicator definition bridges the function-oriented artifact in the KPI tree and the technical implementation of the indicator in Performance Analytics.

If a suitable indicator definition does not exist, click the **create indicator definition** link in the artifact tile. Specify the required properties of the indicator. Also write any development instructions in the field provided for them. If you are defining an [automated indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md), specify the facts table for the indicator source. Also describe any conditions, either on the indicator itself or on the indicator source. You can describe the conditions qualitatively, not following condition builder format. If you are defining a formula indicator, add definitions of its [contributing indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/performance-analytics-glossary.md).

When a suitable Performance Analytics indicator exists, you can add a link to it in the indicator definition. You can see the technical details of the linked indicator. Reproduce the Performance Analytics indicator exactly or specify a modified version.

\[Omitted image "kpi-composer-indicator-definition.png"\] Alt text: Indicator definition record

## Report definitions

A report definition contains the description to create a report. The key information is the facts table or the report source, along with any conditions. You do not have to follow a technical format when writing the conditions.

\[Omitted image "kpi-composer-report-definition.png"\] Alt text: Report definition record

-   **[Create an indicator definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/create-indicator-definition.md)**  
You can create a new KPI Composer indicator definition directly from the relevant artifact in the Data Definition tab. Fill the indicator definition with the necessary information for creating a Performance Analytics indicator.
-   **[Create a report definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/create-report-definition.md)**  
You can create a new KPI Composer report definition directly from the relevant artifact in the Data Definition tab. Fill the report definition with the necessary information for creating a report.

**Parent Topic:**[Design your Performance Analytics solution with KPI Composer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/designing-pa-solution.md)

