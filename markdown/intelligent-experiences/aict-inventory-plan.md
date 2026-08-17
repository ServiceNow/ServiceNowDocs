---
title: Planning AI work from Inventory in AI Control Tower
description: View all planning data for a specific AI system in one location. The Plan tab automatically filters goals, intake items, and delivery records to show only those linked to your selected AI system across Strategize, Prioritize, and Execute workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-inventory-plan.html
release: zurich
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
keywords: [AI Plan, Inventory, AI system, product model]
breadcrumb: [Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Planning AI work from Inventory in AI Control Tower

View all planning data for a specific AI system in one location. The Plan tab automatically filters goals, intake items, and delivery records to show only those linked to your selected AI system across Strategize, Prioritize, and Execute workflows.

## Plan tab overview

The Plan tab appears on the record page of an AI system in AI Control Tower Inventory. It appears only for AI systems, not for other asset types such as AI prompts. The Plan tab provides a focused view of the goals, intake items, and delivery records associated specifically with the AI system you selected.

To navigate to the Plan tab of an AI system:

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Inventory**.
2.  Select **AI Systems** as the asset type.
3.  Select an AI System record to open it.
4.  Navigate to the Plan tab.

The Plan tab has three sub-tabs: Strategize, Prioritize, and Execute. The data on each sub-tab is filtered using the product model of the selected AI system. Records in tables such as goals, demands, and projects that carry a product model field are filtered to show only those linked to that product model. Because the data is already scoped to a single AI system, the Plan tab has no additional header-level filters.

Each list on the Plan tab has a toolbar with the following actions:

-   Search: Find records by keyword.
-   Filter: Open the filter panel to build conditions using field and operator combinations, sort records, or group them within the list.
-   Refresh: Reload the list to show the latest data.
-   Personalize columns: Choose which columns are displayed and in what order. Search from available columns, add or remove them, and drag to reorder.
-   New: Create a record directly from the Plan tab.

You can also edit a record inline by selecting the edit icon \(\[Omitted image "aict-plan-edit-icon.png"\] Alt text:\) in the record row.

**Note:** When you create a record from the Plan tab, confirm that the product model field on the new record is set to the product model of the AI system that you're viewing. If the product model is not set correctly, the new record is excluded from the filtered list after saving.

## Strategize

The Strategize sub-tab displays the Goal and Target lists, both filtered to show only records linked to the product model of the selected AI system. Unlike the Strategize page in the Plan menu, this view shows only the filtered lists without analytics widgets.

|List|Source table|Records displayed|
|----|------------|-----------------|
|Goal|sn\_gf\_goal|Goals where the product model matches the product model of the selected AI system.|
|Target|sn\_gf\_goal\_target|Targets where the product model matches the product model of the selected AI system.|

To edit a goal or target record, see [Edit a strategize record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-plan-edit-a-strategize-record.md).

## Prioritize

The Prioritize sub-tab displays the Demand, Feedback, and Product idea lists, all filtered to show only records linked to the product model of the selected AI system. Unlike the Prioritize page in the Plan menu, this view shows only the filtered lists without analytics tiles.

|List|Source table|Records displayed|
|----|------------|-----------------|
|Demand|dmn\_demand|Demands where the product model matches the product model of the selected AI system.|
|Feedback|sn\_align\_core\_feedback|Feedback records where the product model matches the product model of the selected AI system.|
|Product idea|sn\_align\_core\_product\_idea|Product ideas where the product model matches the product model of the selected AI system.|

To create an intake record, see [Create an intake record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-plan-create-intake-record.md). To edit an existing intake record, see [Manage intake records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-plan-edit-an-intake-record.md).

## Execute

The Execute sub-tab displays the Project and Epic lists, both filtered to show only records linked to the product model of the selected AI system. Unlike the Execute page in the Plan menu, this view shows only the filtered lists without donut widgets or header filters.

|List|Source table|Records displayed|
|----|------------|-----------------|
|Project|pm\_project|Projects where the product model matches the product model of the selected AI system.|
|Epic|sn\_align\_core\_scrum\_epic|Epics where the product model matches the product model of the selected AI system.|

To create a project or epic, see [Create a project or epic in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-plan-create-project-or-epic.md). To edit an existing project or epic, see [Edit a project or epic in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-plan-edit-project-or-epic.md).

**Parent Topic:**[Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-managing-ai-assets.md)

**Related topics**  


[Planning and tracking AI work in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-plan-using.md)

