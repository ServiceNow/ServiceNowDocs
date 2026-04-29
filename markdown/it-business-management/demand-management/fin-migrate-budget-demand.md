---
title: Migrate budget of active demands to Next Experience
description: Migrate your demand budget to Next Experience to manage the financials using Project Workspace.
locale: en-US
release: australia
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Migrate budget of active demands to Next Experience

Migrate your demand budget to Next Experience to manage the financials using Project Workspace.

## Before you begin

Role required: it\_demand\_manager

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Migrate baselines using one of the following options.

<table id="choicetable_v4j_f5z_d1c"><thead><tr><th align="left" id="d206733e85">

Choice

</th><th align="left" id="d206733e88">

Description

</th></tr></thead><tbody><tr><td id="d206733e94">

**Using list actions**

</td><td>

1.  Select the required demands from the projects list.
2.  Select the **Actions on selected rows...** list and select **Migrate Budget**.
3.  On the migrate budget confirmation window, select **OK**.


</td></tr><tr><td id="d206733e124">

**Using related links**

</td><td>

1.  Open the required demand.
2.  Select the **Migrate Budget** related link.
3.  On the migrate budget confirmation window, select **OK**.


</td></tr><tr><td id="d206733e151">

**Activate a scheduled job**

</td><td>

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
2.  Filter the Name field to locate the **Migrate budget for active demands and projects** scheduled job and open it.
3.  Select **Active** and on the Scheduled Script Execution form, fill the fields.

For a description of the field names, see [Scheduled Script Execution Form](../../project-management/reference/scheduled-script-execution-form.md).

4.  Select **Update**.


</td></tr></tbody>
</table>    **Note:** After migration, you won't be able to view the budget on Classic UI. You're encouraged to manage budget using the Financials in Next Experience.


**Parent Topic:**[Create a demand](t_CreatingDemands.md)

