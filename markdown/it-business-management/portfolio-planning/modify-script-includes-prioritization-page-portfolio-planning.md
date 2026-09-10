---
title: Modify Script Includes for Prioritization page in Portfolio Planning
description: Modify the Script Includes for Prioritization and Hierarchy views of the Planning page to change the columns to be highlighted in these views in the workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/modify-script-includes-prioritization-page-portfolio-planning.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Customizing highlighted fields, Configuring Prioritization and Roadmap settings in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Modify Script Includes for Prioritization page in Portfolio Planning

Modify the Script Includes for Prioritization and Hierarchy views of the Planning page to change the columns to be highlighted in these views in the workspace.

## Before you begin

Role required: admin

## About this task

Portfolio Planning uses a dual-file script architecture to enable safe customizations:

-   **ServiceNow Controlled Files \(Read-Only\) - \*Impl**
    -   Maintained by ServiceNow and updated with every product release as needed
    -   Cannot be edited directly by users
    -   Examples: `APWBacklogConfiglmpl` and `APWGanttConfiglmpl`
-   **Customer Config Files \(Editable\) - \*Config**
    -   Designed for customer customizations and enhancements
    -   Extend the corresponding ServiceNow Controlled file
    -   Examples: `APWBacklogConfig` and `APWGanttConfig`

**How it works:** To customize the Prioritization view, copy a function from the ServiceNow Controlled file \(for example, `APWBacklogConfigImpl`\) into the corresponding Config file \(`APWBacklogConfig`\). Then modify the copied function to meet your requirements. Because your customizations are in the Config file, ServiceNow can update the ServiceNow Controlled files during releases without creating merge conflicts.

-   **When to use script customization**

    Use script customization when:

    -   You need to change which columns are highlighted in List or Hierarchy views
    -   Your highlighting requirements cannot be met through the UI configuration options
    -   You need to apply dynamic logic to determine which columns are highlighted

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Update the column name in the **Script** field of the Script Include.

<table id="choicetable_fs4_s21_hkc"><thead><tr><th align="left" id="d233658e195">

For this view

</th><th align="left" id="d233658e198">

Follow these steps

</th></tr></thead><tbody><tr><td id="d233658e204">

**Prioritization view**

</td><td>

1.  Copy the function from the ServiceNow Controlled file:

    1.  From the list of script includes, search and select **APWBacklogConfigImpl**
    2.  In the **Script** field, locate the `getColumnsForHighlightedValues` function.
    3.  Copy the complete function code:

        ```
getColumnsForHighlightedValues: function() {
  return ["planning_state", "status", "moscow"].concat(
    sn_align_core.APWCoreConstants.PROJECT_STATUS_REPORT_HEALTH_FIELDS
  );
}
        ```

The required function is copied.

2.  Paste and modify the function in the Config file.

    1.  From the list of script includes, search and select **APWBacklogConfig**
    2.  In the **Script** field, paste the function you copied.
    3.  Modify the function to include your desired columns. For example, to highlight the Priority column instead of MoSCoW:

        ```
getColumnsForHighlightedValues: function() {
  return ["planning_state", "status", "priority"].concat(
    sn_align_core.APWCoreConstants.PROJECT_STATUS_REPORT_HEALTH_FIELDS
  );
}
        ```

    4.  Update the column name in the pasted function as needed.

For example, if you want to highlight the Priority column instead of MoSCoW, update the return value to

        ```
getColumnsForHighlightedValues: function() {return ["planning_state", "status", "priority"].concat(sn_align_core.APWCoreConstants.PROJECT_STATUS_REPORT_HEALTH_FIELDS); }
        ```

    5.  Select **Update** to save your changes.
The required function is updated.

The Priority column is now highlighted in the Prioritization List view. During the next product upgrade, the ServiceNow Controlled file \(`APWBacklogConfigImpl`\) will be updated, but your customization in the Config file will remain intact and will not conflict.

</td></tr><tr><td id="d233658e283">

**Hierarchy view**

</td><td>

1.  Copy the required function from the Impl file.

    1.  From the list of script includes, search and select **APWGanttConfigImpl**
    2.  In the **Script** field, locate the `getColumnsForHighlightedValues` function.
    3.  Copy the complete function code:

        ```
getColumnsForHighlightedValues: function() {
  return ["planning_state", "status", "moscow"].concat(
    sn_align_core.APWCoreConstants.PROJECT_STATUS_REPORT_HEALTH_FIELDS
  );
}
        ```

The required function is copied.

2.  Paste and modify the function in the Config file.

    1.  From the list of script includes, search and select **APWGanttConfig**
    2.  In the **Script** field, paste the function you copied.
    3.  Modify the function to include your desired columns. For example, to highlight the Priority column instead of MoSCoW:

        ```
getColumnsForHighlightedValues: function() {
  return ["planning_state", "status", "priority"].concat(
    sn_align_core.APWCoreConstants.PROJECT_STATUS_REPORT_HEALTH_FIELDS
  );
}
        ```

    4.  Select **Update** to save your changes.
The required function is updated.

The Priority column is now highlighted in the Prioritization Hierarchy view. During the next product upgrade, the ServiceNow Controlled file \(`APWGanttConfigImpl`\) will be updated, but your customization in the Config file will remain intact and will not conflict.

</td></tr></tbody>
</table>
## What to do next

[Create highlighted values for Prioritization columns in Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/create-highlighted-values-prioritization-portfolio-planning.md)

**Parent Topic:**[Highlighted fields on the Prioritization tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/customizing-highlighted-fields-prioritization-page-portfolio-planning-workspace.md)

