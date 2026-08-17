---
title: Monitoring AI plan execution in AI Control Tower
description: Monitor the delivery status of AI-related projects and epics from a single page in AI Control Tower, with widgets and lists that update dynamically when you apply filters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-plan-execute.html
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 2
breadcrumb: [Use, Plan AI strategy, prioritize, and execute, Plan your AI strategy, AI Control Tower, Enable AI experiences]
---

# Monitoring AI plan execution in AI Control Tower

Monitor the delivery status of AI-related projects and epics from a single page in AI Control Tower, with widgets and lists that update dynamically when you apply filters.

## Execute page overview

The Execute page shows AI-related projects and epics in one view. Portfolio managers and AI COE leads use this page to track delivery status across the AI portfolio without switching to separate project management applications.

The page has three components that work together:

-   Two donut widgets summarizing project and epic counts by a grouping parameter such as state or priority.
-   Header filters that narrow all widgets and lists simultaneously.
-   Project and Epic lists showing individual records with key details.

## Widgets

The Execute page has two donut widgets: one for Projects and one for Epics. Each widget shows the total count of AI-related records broken down by the selected grouping parameter. The default grouping is by state.

Use the **Group by** control on each widget to change the grouping parameter. Each widget's grouping can be changed independently. Available grouping options include the following:

-   Project: State, Status, Priority, Project Manager, Department, Product
-   Epic: State, Status, Owner, Department, Product

Clicking a segment in a widget show the list of corresponding records.

## Filters

Three filters are available in the page header. Selecting a filter value updates the widgets and lists simultaneously.

|Filter|Description|
|------|-----------|
|Strategic Priority|Filters by the strategic priority associated with the records.|
|AI System|Filters by the AI system linked to the records.|
|Department|Filters by the department associated with the records.|

## Project and Epic lists

The Project and Epic lists show individual AI-related records from their source tables. These lists are displayed based on the Default view of the project and epic. Each list has a toolbar with the following actions:

-   Search: Find records by keyword.
-   Filter: Open the filter panel to build conditions using field and operator combinations, sort records, or group them within the list. These are separate from the page-level header filters.
-   Refresh: Reload the list to show the latest data.
-   Personalize columns: Choose which columns are displayed and in what order. Search from available columns, add or remove them, and drag to reorder. Select **Reset to Default** to restore the original column set.
-   New: Create a record directly from the Execute page.

|List name|Source table|Records displayed|
|---------|------------|-----------------|
|Project|pm\_project|Records where the investment type is Artificial Intelligence, or where the linked product belongs to the cmdb\_ai\_system\_component\_product\_model table \(includes generative AI, agentic AI, and other subclasses\).|
|Epic|sn\_align\_core\_scrum\_epic|Records where the investment type is Artificial Intelligence, or where the linked product belongs to the cmdb\_ai\_system\_component\_product\_model table \(includes generative AI, agentic AI, and other subclasses\).|

**Related topics**  


[AI Plan configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-plan-configuring.md)

[Planning and tracking AI work in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-plan-using.md)

[AI Control Tower plan reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-plan-reference.md)

