---
title: Configure the landing page for created demand records
description: Configure a system property that controls which tab opens when a demand record is created. Set this property to match your team's workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/configure-demand-record-landing-page-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Configure the landing page for created demand records

Configure a system property that controls which tab opens when a demand record is created. Set this property to match your team's workflow.

## Before you begin

Role required: admin

## Procedure

1.  Select **All**.

2.  Search for `sys_properties.list` in the filter navigator.

3.  Select **New**.

4.  Enter the system property form field values.

<table id="table_hfx_mlv_ckc"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

`sn_align_ws.demand_record_landing_page`

</td></tr><tr><td>

Choices

</td><td>

Enter the following values, separated by commas: -   `playbook`
-   `details`
-   `docs`
-   `financials`


</td></tr><tr><td>

Type

</td><td>

`string`

</td></tr><tr><td>

Value

</td><td>

A single value from the choices list — for example, `docs`. **Note:** The property defaults to `details` if the value is unset or invalid.

</td></tr></tbody>
</table>5.  Select **Submit**.


## What to do next

To change the landing page after setting this property, open the system property record, select a different value in the **Value** field, and select **Update**.

**Related topics**  


[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t\_AddAPropertyUsingSysPropsList.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md)

[Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/create-a-demand-ppw.md)

