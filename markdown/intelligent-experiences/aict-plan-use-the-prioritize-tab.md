---
title: Prioritizing AI plan in AI Control Tower
description: View and manage AI-related intake items, demands, product ideas, and product feedback, through analytics tiles, contextual filters, and filterable lists in Prioritize tab. All three lists support creation of new records from this tab.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-plan-use-the-prioritize-tab.html
release: australia
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 2
breadcrumb: [Use, Plan AI strategy, prioritize, and execute, Plan your AI strategy, AI Control Tower, Enable AI experiences]
---

# Prioritizing AI plan in AI Control Tower

View and manage AI-related intake items, demands, product ideas, and product feedback, through analytics tiles, contextual filters, and filterable lists in Prioritize tab. All three lists support creation of new records from this tab.

## Prioritize tab overview

The Prioritize tab displays all AI-related intake records, demands, product ideas, and feedback, in a single view.\[Omitted image "aict-plan-prioritize-tab.png"\] Alt text: The Prioritize tab displays the intake lists with analytics and filters.

AI stewards use the Prioritize tab to:

-   Monitor incoming AI-related intake across all three record types.
-   Identify unowned items that are at risk of stalling.
-   Create records without leaving the planning context.

The page is divided into the following components:

-   Analytics summary cards - displays real-time counts of intake and ownership status.
-   Filters - helps narrow all tiles and lists by strategic priority, AI system, or department.
-   Intake lists - displays the full set of demand, product idea, and feedback records.

## Analytics summary cards

The four analytics tiles at the top of the page display counts based on the active filter state. All counts are updated when a filter is applied.

|Summary card|Functionality|Drill-down|
|------------|-------------|----------|
|Total Intake Items|Displays the combined count of all demands, product ideas, and feedback|Not applicable as all records are visible in the lists.|
|Ownerless Demands|Displays the count of demands where the owner field is empty.|Drills down to the list of ownerless demands.|
|Ownerless Ideas|Displays the count of product ideas where the owner field is empty.|Drills down to the list of ownerless product ideas.|
|Ownerless Feedback|Displays the count of feedback records where the owner field is empty.|Drills down to the list of ownerless feedback records.|

## Filters

Three filters are available in the page header. All filters apply simultaneously across all tiles and all three lists.

|Filter|Description|
|------|-----------|
|Strategic Priority|Filters by the strategic priority associated with the records.|
|AI System|Filters by the AI system linked to the records.|
|Department|Filters by the department associated with the records.|

## Intake lists

The Demand, Product idea, and Feedback lists display the AI-related intake records from their respective tables. All three lists share the same behaviour and functionalities. You can search, filter, refresh, and personalize the columns in these lists. Additionally, you can create records or edit existing records directly from the lists. The lists and forms displayed for the records in the Prioritize pages are in the default view.

<table id="table_tmn_45j_1jc"><thead><tr><th>

List name

</th><th>

Source table

</th><th>

Records displayed

</th></tr></thead><tbody><tr><td>

Demand

</td><td>

dmn\_demand

</td><td rowspan="3">

The following records are displayed:-   Investment type is Artificial Intelligence.

**Note:** This is applicable only for demands and ideas.

-   Linked product belongs to the cmdb\_ai\_system\_component\_product\_model table, which includes generative AI, agentic AI, and other subclasses.

</td></tr><tr><td>

Product idea

</td><td>

sn\_align\_core\_product\_idea

</td></tr><tr><td>

Feedback

</td><td>

sn\_align\_core\_feedback

</td></tr></tbody>
</table>The following list actions are available on all three intake lists:

|Action|Description|
|------|-----------|
|Search|Search within the intake list.|
|Filter|Apply additional filter conditions to the list.|
|Refresh|Reload the list with the latest data.|
|Personalize columns|Add, remove, or reorder list columns.|

**Related topics**  


[AI Plan configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-plan-configuring.md)

[Planning and tracking AI work in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-plan-using.md)

