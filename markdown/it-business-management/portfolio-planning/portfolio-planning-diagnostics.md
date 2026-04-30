---
title: Portfolio Planning diagnostics
description: Run diagnostic scans to identify and fix errors in the configuration and other common settings for Portfolio Planning before your planning managers prioritize and roadmap their projects and demands.
locale: en-US
release: xanadu
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Portfolio Planning diagnostics

Run diagnostic scans to identify and fix errors in the configuration and other common settings for Portfolio Planning before your planning managers prioritize and roadmap their projects and demands.

Portfolio Planning diagnostic scans help you find discrepancies by validating the configuration for the following:

-   Lens and lens structure
-   Form views, list views, related list views, and workspace view rules for planning items
-   Global ranking for planning items
-   Portfolio plans

The following are the default diagnostic scans available for Portfolio Planning.

## Portfolio Planning diagnostics

<table id="table_ppcorediag"><thead><tr><th>

Name of the scan

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Identify planning items without a global rank

</td><td>

Identifies the number of planning items on the Prioritization List page, for which the global rank is not populated.

 If this scan fails, the result shows the planning items that do not have a global rank. Click **Run Fix Script** to populate a global rank to items for which this field is empty.

</td></tr><tr><td>

Validate List views for planning items

</td><td>

Verifies that all the planning items that can be added to portfolio plans have the APW Prioritization and APW Default List views.

 If this scan fails, the result displays the List views that are missing for certain planning item tables.

 To learn how to fix these, see [Create list views for new planning item tables in Strategic Planning](../../alignment-planner-workspace/task/create-list-views-for-new-planning-item-tables-in-strategic-planning.md).

</td></tr><tr><td>

Validate Form section views for planning items

</td><td>

Verifies that all the planning items that can be added to portfolio plans have the APW Prioritization, APW Default, and APW New form views.

 If this scan fails, the result displays the Form section views that are missing for certain planning item tables.

 To learn how to fix these, see [Create form views for new planning item tables in Strategic Planning](../../alignment-planner-workspace/task/create-form-views-for-planning-item-tables-in-apw.md).

</td></tr><tr><td>

Validate Related list views for planning items

</td><td>

Verifies that all the planning items that are allowed on portfolio plans have the APW Default Related list view.

 If this scan fails, the result displays the Related list views that are missing for certain planning item tables.

 To learn how to fix these, see [Create related list views for new planning item types in Strategic Planning](../../alignment-planner-workspace/task/create-related-list-views-new-planning-item-types-strategic-planning.md).

</td></tr><tr><td>

Validate Workspace view rule for Default view of planning items

</td><td>

Verifies that all the planning items that are allowed on portfolio plans have the Default view's workspace view rule.

 If this scan fails, the result displays the Default view rule is missing for certain planning item tables.

 To learn how to fix these, see [Create workspace view rules for new planning item forms in Strategic Planning](../../alignment-planner-workspace/task/create-workspace-view-rules-for-planning-item-tables.md).

</td></tr><tr><td>

Validate Workspace view rule for APW Default view of planning items

</td><td>

Verifies that all the planning items that are allowed on portfolio plans have the APW Default view's workspace view rule.

 If this scan fails, the result displays the APW Default view rule is missing for certain planning item tables.

 To learn how to fix these, see [Create workspace view rules for new planning item forms in Strategic Planning](../../alignment-planner-workspace/task/create-workspace-view-rules-for-planning-item-tables.md).

</td></tr><tr><td>

Validate invalid fields in the Portfolio Plan configuration

</td><td>

Finds any invalid fields in the portfolio plan configuration records for all existing portfolio plans.If this scan fails, click **Run Fix Script** to remove the identified invalid fields.

</td></tr><tr><td>

Validate Portfolio Plan Configuration for all the portfolio plans

</td><td>

Verifies if each existing portfolio plan created in your instance has a valid portfolio plan configuration.

</td></tr></tbody>
</table>