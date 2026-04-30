---
title: Strategic Planning diagnostics
description: Run diagnostic scans to identify and fix errors in the configuration and other common settings for Strategic Planning before your planning managers prioritize and roadmap work for their portfolio plans.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Strategic Planning diagnostics

Run diagnostic scans to identify and fix errors in the configuration and other common settings for Strategic Planning before your planning managers prioritize and roadmap work for their portfolio plans.

Strategic Planning diagnostic scans help you find discrepancies by validating the configuration for the following:

-   Lens and lens structure
-   Form views, list views, related list views, and workspace view rules for planning items
-   Global ranking for planning items
-   Portfolio plans
-   Goals data
-   high-level planning entities

The following are the default diagnostic scans available for Strategic Planning.

![Portfolio Planning diagnostics.](../../it-business-management/image/SPW-diagnostics.png)

## Strategic Planning diagnostics for high-level planning

<table id="table_myz_3wj_cxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Validate Rank configuration for the high-level planning entities

</td><td>

Verifies that entities enabled for high-level planning have a Rank configuration.

 If this test fails, see [Create rank configuration for high-level planning](../task/create-rank-configuration-enable-high-level-planning.md) to fix failure.

</td></tr><tr><td>

Validate Form section views for high-level planning entities

</td><td>

Verifies that all the lens entities that are enabled for high-level planning have the required Form section views.

 If this scan fails, the result displays the Form section views that are missing for certain entities that are enabled for high-level planning.

 To learn how to fix these, see [Create form views for new planning item tables in Strategic Planning](../task/create-form-views-for-planning-item-tables-in-apw.md).

</td></tr><tr><td>

Validate Related list views for high-level planning entities

</td><td>

Verifies that all the lens entities that are enabled for high-level planning have the required Related list views.

 If this scan fails, the result displays the Related List views that are missing for certain entities that are enabled for high-level planning.

 To learn how to fix these, see [Create related list views for new planning item types in Strategic Planning](../task/create-related-list-views-new-planning-item-types-strategic-planning.md).

</td></tr><tr><td>

Validate List views for high-level planning entities

</td><td>

Verifies that all the lens entities that are enabled for high-level planning have the required List views.

 If this scan fails, the result displays the List views that are missing for certain planning item tables.

 To learn how to fix these, see [Create list views for new planning item tables in Strategic Planning](../task/create-list-views-for-new-planning-item-tables-in-strategic-planning.md).

</td></tr><tr><td>

Identify high-level planning entities enabled for planning, without a global rank

</td><td>

Identifies the number of high-level planning entities that do not have a global rank.

 If this scan fails, the result shows the planning items that do not have a global rank. Click **Run Fix Script** to populate a global rank to items for which this field is empty.

</td></tr></tbody>
</table>## Portfolio Planning diagnostics

The following are the diagnostic scans available to validate common configuration errors for planning items, goals, and portfolio plans:

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

Check Goal Assigned Entity Configuration for lens entities

</td><td>

Identifies the lens entities for which the goal assigned entity configuration is missing.

 If this scan fails, the result shows the lens entities that don’t have Assigned Entity Configuration.

</td></tr><tr><td>

Validate List views for planning items

</td><td>

Verifies that all the planning items that can be added to portfolio plans have the APW Prioritization and APW Default List views.

 If this scan fails, the result displays the List views that are missing for certain planning item tables.

 To learn how to fix these, see [Create list views for new planning item tables in Strategic Planning](../task/create-list-views-for-new-planning-item-tables-in-strategic-planning.md).

</td></tr><tr><td>

Validate Form section views for planning items

</td><td>

Verifies that all the planning items that can be added to portfolio plans have the APW Prioritization, APW Default, and APW New form views.

 If this scan fails, the result displays the Form section views that are missing for certain planning item tables.

 To learn how to fix these, see [Create form views for new planning item tables in Strategic Planning](../task/create-form-views-for-planning-item-tables-in-apw.md).

</td></tr><tr><td>

Validate Related list views for planning items

</td><td>

Verifies that all the planning items that are allowed on portfolio plans have the APW Default Related list view.

 If this scan fails, the result displays the Related list views that are missing for certain planning item tables.

 To learn how to fix these, see [Create related list views for new planning item types in Strategic Planning](../task/create-related-list-views-new-planning-item-types-strategic-planning.md).

</td></tr><tr><td>

Validate Workspace view rule for Default view of planning items

</td><td>

Verifies that all the planning items that are allowed on portfolio plans have the Default view's workspace view rule.

 If this scan fails, the result displays the Default view rule is missing for certain planning item tables.

 To learn how to fix these, see [Create workspace view rules for new planning item forms in Strategic Planning](../task/create-workspace-view-rules-for-planning-item-tables.md).

</td></tr><tr><td>

Validate the goal relationships for assigned entities

</td><td>

Identifies if there are any m2m goal relationships defined for assigned entities.

 If this scan fails, the result displays the goals that do have m2m goal relationships any assigned entity table. You can run the **Migrate goal relationships for assigned entities** scheduled job to migrate the existing goal relationship data from the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table to the Goals table. For more information, see [Migrate goal relationships for assigned entities](../../spw-goals/task/migrate-goal-relationships-for-assigned-entities-egm.md).

</td></tr><tr><td>

Validate Workspace view rule for APW Default view of planning items

</td><td>

Verifies that all the planning items that are allowed on portfolio plans have the APW Default view's workspace view rule.

 If this scan fails, the result displays the APW Default view rule is missing for certain planning item tables.

 To learn how to fix these, see [Create workspace view rules for new planning item forms in Strategic Planning](../task/create-workspace-view-rules-for-planning-item-tables.md).

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