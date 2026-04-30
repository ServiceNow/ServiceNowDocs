---
title: Edit ServiceNow data on Service Observability dashboard templates
description: Edit Service Observability dashboard templates to view data from problem and business app records on the Overview or Observability dashboards.
locale: en-US
release: zurich
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Customize dashboard templates, Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Edit ServiceNow data on Service Observability dashboard templates

Edit Service Observability dashboard templates to view data from problem and business app records on the Overview or Observability dashboards.

## Before you begin

Role required: sn\_sow\_svcobs.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** and then navigate to a service record.

    You can access a service record from these pages in the SOW:

    -   **Services** list: Choose a service from the list.
    -   **Service dashboard**: Choose a service in the dashboard and select **Service Details**.
    -   **List**: Navigate to **Application Services** &gt; **Services** and select a service.
    -   **Express list** alert: Select a service from the **Impacted services** column.
    The Service Details page opens and the Overview tab is displayed.

    If charts are displaying error messages, see [Chart error states](../reference/chart-error-states.md).

2.  Open the template in editing mode.

    -   If you're editing a certified template, select **Duplicate**.
    -   If you're editing a custom template, select **Edit**.
    **Note:** Duplicating a certified template keeps you from overwriting it and also lets you reinstall it.

    The new dashboard is titled with the words `- Copy` appended. Use the pencil icon to change the dashboard name.

3.  To do basic editing, such as rearranging, resizing, or deleting charts, follow the instructions for [Edit in-line Platform Analytics dashboard elements](https://www.servicenow.com/docs/access?context=edit-db-elements-in-ac&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

4.  To add a new ServiceNow table, follow these steps:

    1.  In Edit mode, select **Add new element** and choose **List**.

    2.  In the **Configuration panel** in the **Data sources** section, choose **Add data source**.

    3.  In the **Add data source** page, find the **Table** whose data you want to display and choose **Add this source**.

    4.  In the **Columns and rows** section, add and arrange the columns to display.

5.  To edit an existing chart, follow these steps.

    1.  In Edit mode, select the chart to edit.

    2.  In the **Data** section of the Configuration panel, verify that the correct table is selected in **Table** field.

    3.  In the **Columns and rows** section, add and arrange the columns to display.

6.  When done customizing, select **Save** and then **Exit editing mode.**

7.  To return the template to the default \(Certified\) version, use the **More actions** menu to select **Return to certified**.


**Parent Topic:**[Customize Service Observability dashboard templates](customize-service-observability-dashboard-templates.md)

