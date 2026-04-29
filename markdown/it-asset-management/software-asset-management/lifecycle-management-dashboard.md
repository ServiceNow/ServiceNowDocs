---
title: Lifecycle management dashboard
description: Review and track the end of life \(EOL\) software products in your asset estate to reduce risks associated with software products that are reaching or have reached EOL.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Software asset analytics view, Software Asset Workspace, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Lifecycle management dashboard

Review and track the end of life \(EOL\) software products in your asset estate to reduce risks associated with software products that are reaching or have reached EOL.

The Lifecycle management dashboard displays reports on product life cycles, the current and past EOL product life cycles, and the upcoming EOL product life cycles for the next 18 months. You can also view EOL workflow status and workflow action.

**Note:** The Lifecycle management dashboard is only visible if you activate the Software Asset Management Professional plugin from ServiceNow Store.

Access the Lifecycle management dashboard by navigating to **Workspaces** &gt; **Software Asset Workspace** &gt; **Software asset analytics** &gt; **Lifecycle management**.

You can filter the dashboard reports based on a publisher or product. Select any report to view more information on product life cycles.

![Lifecycle management dashboard view displaying product lifecycles](../image/lifecycle-management-dashboard-updated.png "Lifecycle management dashboard")

<table id="table_cs4_3k1_t1c"><thead><tr><th>

Report

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product lifecycle overview

</td><td>

Software Lifecycle Report\[sam\_sw\_product\_lifecycle\_report\]

</td><td>

Product life-cycle details for all the software products installed in your environment.Select a life-cycle phase to determine the current phase of the software products in your environment.

</td></tr><tr><td>

Current and past end of life product lifecycles

</td><td>

Software Lifecycle Report\[sam\_sw\_product\_lifecycle\_report\]

</td><td>

Software product life-cycles in your environment that are based on their EOL timelines.The chart displays data from the current year and the previous 15 years.

</td></tr><tr><td>

Lifecycle data completeness

</td><td>

Software Lifecycle Playbook\[sam\_sw\_lifecycle\_playbook\]

</td><td>

Lists all the open lifecycle playbooks that have been created.

 You can open any of the existing playbooks to update or complete them.

 You can select **Add to lifecycle data** to create a playbook for lifecycle data. For details on creating the playbook, see [Create a comprehensive lifecycle report using a guided experience](../task/create-lifecyclereporting-guidedexperience.md).

</td></tr><tr><td>

End of life workflow stages

</td><td>

Software EOL Request \[samp\_sw\_eol\_request\]

</td><td>

EOL workflows grouped by the following stages:-   Open
-   Analysis
-   Action initiated
-   Completed
-   Cancelled

</td></tr><tr><td>

End of life workflow actions

</td><td>

Software EOL Request \[samp\_sw\_eol\_request\]

</td><td>

EOL workflows grouped by action initiated:-   Pending: Action is pending.
-   Remove EOL software: Remove the EOL software product from the asset inventory.
-   Upgrade: Upgrade to the latest or the supported software version.
-   Purchase support: Purchase additional support for maintenance.
-   Move to Azure: Migrate to Microsoft Azure. This action is available only for Microsoft products.
-   Accept risk: Accept the risks associated with the EOL software.

**Note:** This chart doesn't include EOL workflows that are in the Draft or Cancelled stage.

</td></tr><tr><td>

Upcoming end of life product lifecycles in next 18 months

</td><td>

Software Lifecycle Report\[sam\_sw\_product\_lifecycle\_report\]

</td><td>

Software product life-cycles in your environment that are reaching EOL in the next 18 months.

</td></tr></tbody>
</table>## Managing workflow to reduce risks associated with EOL software

Tracking product life cycles enables you to manage software products that are reaching or have already reached EOL, end of support \(EOS\), or end of extended support.

You can take required action for your EOL software products by using the Software Product Lifecycle report. The report opens when you select the **Upcoming end of life product lifecycles in next 18 months** or **Current and past end of life product lifecycles** report on the Lifecycle management dashboard. You can create an EOL request for the software products that have the Current phase as End of Support, End of Extended Support, or End of Life. For more details, see [Create an end of life workflow request for your software products](../task/manage-eol-risk.md).

