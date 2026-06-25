---
title: List reports
description: List reports display data in the form of an expandable list. You can configure whether lists appear expanded or collapsed. Lists are often used for enumerations such as the number of incidents or changes. They contain columns that show more detailed information, such as a short description, category, or state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/reporting/list-reports.html
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Report types, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# List reports

List reports display data in the form of an expandable list. You can configure whether lists appear expanded or collapsed. Lists are often used for enumerations such as the number of incidents or changes. They contain columns that show more detailed information, such as a short description, category, or state.

**Note:**

-   This topic refers to Reporting in the Core UI. If your instance is migrated to Platform Analytics experience, see [Create a list visualization in the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-dv-analytics-list.md).
-   List reports display in List v2, even if List v3 is enabled.
-   The record count and pagination buttons appear only at the bottom of the list.

This example list report displays incidents sorted by caller.

\[Omitted image "List.png"\] Alt text: List report — change requests by category including assigned to, short description, planned start date, and planned end date

## Types of list reports

There are three types of list reports.

-   **[Basic list reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/t_CreateAListReport.md)**

    List reports with no additional features

-   **[List reports with variable columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/create-list-rep-with-var-col.md)**

    List reports based on a data source or table that has variables associated with it, for example, Service Catalog data sources. Variables are often variations in products such as amounts of storage in a computer.

-   **[List reports with question columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/create-list-rep-with-question-col.md)**

    List reports based on a data source or table that has questions associated with it. For example, if a form prompts a user to select the specific nature of a problem, you can create a list report with columns for their responses.


Basic list reports can use a table, a data source, an imported Excel spreadsheet, or a MetricBase table for their report sources. List reports with variable and question columns use only tables and data sources.

There are extra steps to configure the question and variable columns.

