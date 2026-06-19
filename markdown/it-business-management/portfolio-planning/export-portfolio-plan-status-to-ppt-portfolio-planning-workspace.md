---
title: Export the portfolio plan status or roadmap to Microsoft PowerPoint
description: Export the status of work items, roadmap, and key metrics of your portfolio plan and free-form roadmap into a Microsoft PowerPoint file so that you can keep your business stakeholders updated on the progress. Save time by avoiding copying data into reports and drive shared outcomes by enabling collaboration even with stakeholders who cannot access your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/portfolio-planning/export-portfolio-plan-status-to-ppt-portfolio-planning-workspace.html
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Portfolio Planning, Strategic Portfolio Management]
---

# Export the portfolio plan status or roadmap to Microsoft PowerPoint

Export the status of work items, roadmap, and key metrics of your portfolio plan and free-form roadmap into a Microsoft PowerPoint file so that you can keep your business stakeholders updated on the progress. Save time by avoiding copying data into reports and drive shared outcomes by enabling collaboration even with stakeholders who cannot access your ServiceNow instance.

## Before you begin

[Install Export to PowerPoint for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/export-to-powerpoint-for-application-portfolio-management/install-export-to-ppt.md).

**Important:** Export to PowerPoint is currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. Please check for availability updates in future releases.

Role required: admin

## About this task

The following two PowerPoint templates are provided by default to generate a status report for your portfolio plan:

-   Portfolio plan status: Contains individual detailed slides for the top five items prioritized by rank.
-   Roadmap Template - default: Contains slides for Roadmap for this portfolio. You can export roadmap data for a maximum period of a year at a time.

You can customize the type of the data to be shown in the generated report by updating a predefined template or by creating your own branded template. See [Create a Microsoft PowerPoint template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/export-to-powerpoint-for-application-portfolio-management/create-ppt-template.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace** &gt; **Portfolio Planning**.

2.  Export the status of goals, work items, roadmap, and key metrics of your portfolio plan and free-form roadmap into a Microsoft PowerPoint file.

<table id="choicetable_qkd_qrh_bcc"><thead><tr><th align="left" id="d45561e148">

For exporting this data

</th><th align="left" id="d45561e151">

Perform these steps

</th></tr></thead><tbody><tr><td id="d45561e157">

**Portfolio plan or roadmap with default settings**

</td><td>

1.  From the list of portfolio plans, select one.
2.  From the portfolio plan header, select the More options icon \(\[Omitted image "more-actions.png"\] Alt text: More actions icon in the portfolio plan header.\) and then select **Export to PowerPoint**.

\[Omitted image "pp-actions-export-to-ppt.png"\] Alt text: Export to PowerPoint option from the More options menu.

3.  On the Export to PowerPoint window, select **Portfolio plan status** or **Roadmap Template - default** and select **Export**.

\[Omitted image "ppt-export-template-ppw.png"\] Alt text: Select a template to export portfolio plan.

</td></tr><tr><td id="d45561e208">

**Roadmap or free-form roadmap with customized settings**

</td><td>

1.  \(For a portfolio plan roadmap\) Select a portfolio plan from the list of portfolio plans and then select **Roadmap** from the Planning section.
2.  \(For a free-form roadmap\) From the Free-form Roadmaps tab, select a roadmap.
3.  From the Personalize side panel, select Export to PowerPoint icon \(\[Omitted image "icon-export-data.png"\] Alt text: Export icon.\).

If you want to export the progress tracking details, select the Tracking mode option on the roadmap before selecting the Export to PowerPoint icon.

4.  On the Export to PowerPoint side panel, fill the details.

    1.  Template: Select a template to which you want to export the roadmap.
    2.  Date range: Select a start and end date. You can select date range for a maximum period of a year.
    3.  Compact mode: Select to export 25 horizontal lanes per slide. The default mode exports 15 horizontal lanes per slide.
    4.  Show on slides: Select the items that you want to see on the slides. The available items are Roadmap milestones, Item milestones, Vertical lines, and Horizontal lanes.
    5.  Select **Export**.
\[Omitted image "export-roadmap-from-side-panel.png"\] Alt text: Export roadmap to PPT.

 **Note:** Dependencies and metrics on roadmap bar are not exported. Grouping is supported only with the first attribute selected in the Group by option.

</td></tr></tbody>
</table>
## Result

A PowerPoint file is generated with the relevant data.

This image is an example for an exported roadmap.\[Omitted image "exported-roadmap-to-ppt.png"\] Alt text: Exported roadmap.

