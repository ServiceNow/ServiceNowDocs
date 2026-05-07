---
title: Export the portfolio plan status or roadmap to Microsoft PowerPoint
description: Export the status of work items, roadmap, and key metrics of your portfolio plan and free-form roadmap into a Microsoft PowerPoint file so that you can keep your business stakeholders updated on the progress. Save time by avoiding copying data into reports and drive shared outcomes by enabling collaboration even with stakeholders who cannot access your ServiceNow instance.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Portfolio Planning, Strategic Portfolio Management]
---

# Export the portfolio plan status or roadmap to Microsoft PowerPoint

Export the status of work items, roadmap, and key metrics of your portfolio plan and free-form roadmap into a Microsoft PowerPoint file so that you can keep your business stakeholders updated on the progress. Save time by avoiding copying data into reports and drive shared outcomes by enabling collaboration even with stakeholders who cannot access your ServiceNow instance.

## Before you begin

[Install Export to PowerPoint for Strategic Portfolio Management](../../export-to-ppt/task/install-export-to-ppt.md).

**Important:** Export to PowerPoint is available only in the GCC, NSC, SPP-AU, SPP-SG, and Australia IRAP-Protected data center environments.

Role required: admin

## About this task

The following two PowerPoint templates are provided by default to generate a status report for your portfolio plan:

-   Portfolio plan status: Contains individual detailed slides for the top five items prioritized by rank.
-   Roadmap Template - default: Contains slides for Roadmap for this portfolio. You can export roadmap data for a maximum period of a year at a time.

You can customize the type of the data to be shown in the generated report by updating a predefined template or by creating your own branded template. See [Create a Microsoft PowerPoint template](../../export-to-ppt/task/create-ppt-template.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace** &gt; **Portfolio Planning**.

2.  Export the status of goals, work items, roadmap, and key metrics of your portfolio plan and free-form roadmap into a Microsoft PowerPoint file.

<table id="choicetable_qkd_qrh_bcc"><thead><tr><th align="left" id="d43577e148">

For exporting this data

</th><th align="left" id="d43577e151">

Perform these steps

</th></tr></thead><tbody><tr><td id="d43577e157">

**Portfolio plan or roadmap with default settings**

</td><td>

1.  From the list of portfolio plans, select one.
2.  From the portfolio plan header, select the More options icon \(![More actions icon in the portfolio plan header.](../../alignment-planner-workspace/images/more-actions.png)\) and then select **Export to PowerPoint**.

![Export to PowerPoint option from the More options menu.](../../alignment-planner-workspace/images/pp-actions-export-to-ppt.png)

3.  On the Export to PowerPoint window, select **Portfolio plan status** or **Roadmap Template - default** and select **Export**.

![Select a template to export portfolio plan.](../images/ppt-export-template-ppw.png)

</td></tr><tr><td id="d43577e208">

**Roadmap or free-form roadmap with customized settings**

</td><td>

1.  \(For a portfolio plan roadmap\) Select a portfolio plan from the list of portfolio plans and then select **Roadmap** from the Planning section.
2.  \(For a free-form roadmap\) From the Free-form Roadmaps tab, select a roadmap.
3.  From the Personalize side panel, select Export to PowerPoint icon \(![Export icon.](../../alignment-planner-workspace/images/icon-export-data.png)\).

If you want to export the progress tracking details, select the Tracking mode option on the roadmap before selecting the Export to PowerPoint icon.

4.  On the Export to PowerPoint side panel, fill the details.

    1.  Template: Select a template to which you want to export the roadmap.
    2.  Date range: Select a start and end date. You can select date range for a maximum period of a year.
    3.  Compact mode: Select to export 25 horizontal lanes per slide. The default mode exports 15 horizontal lanes per slide.
    4.  Show on slides: Select the items that you want to see on the slides. The available items are Roadmap milestones, Item milestones, Vertical lines, and Horizontal lanes.
    5.  Select **Export**.
![Export roadmap to PPT.](../../alignment-planner-workspace/images/export-roadmap-from-side-panel.png)

 **Note:** Dependencies and metrics on roadmap bar are not exported. Grouping is supported only with the first attribute selected in the Group by option.

</td></tr></tbody>
</table>
## Result

A PowerPoint file is generated with the relevant data.

This image is an example for an exported roadmap.![Exported roadmap.](../../alignment-planner-workspace/images/exported-roadmap-to-ppt.png)

