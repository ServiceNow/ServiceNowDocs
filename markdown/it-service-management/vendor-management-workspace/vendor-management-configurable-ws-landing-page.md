---
title: Vendor Management Workspace landing page
description: Monitor vendor metrics, the number of recently created contracts, the ones that are ending soon and the number of active improvement initiatives at any given time. See which characteristics contribute to the success of your vendors. View how your vendors are ranked against those characteristics in comparison to other vendors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/vendor-management-workspace/vendor-management-configurable-ws-landing-page.html
release: zurich
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, Vendor Management Workspace, IT Service Management]
---

# Vendor Management Workspace landing page

Monitor vendor metrics, the number of recently created contracts, the ones that are ending soon and the number of active improvement initiatives at any given time. See which characteristics contribute to the success of your vendors. View how your vendors are ranked against those characteristics in comparison to other vendors.

You can clone an existing landing page and customize it using the Next Experience UI Builder. For more information, see [Customize a Vendor Management Workpace page using the Next Experience UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/vendor-management-workspace/customize-vmw-page.md).

\[Omitted image "vendor-management-workspace-landing-page.png"\] Alt text: Vendor Manager Workspace Landing Page

## Required Vendor Manager Workspace roles

If you have the Vendor Manager \[sn\_vlm.vendor\_manager\] role, you can access the Vendor Management Workspace landing page.

## Use cases

<table id="table_uj4_rww_r4b"><thead><tr><th>

End user and goal

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

As a vendor manager, you can analyze real-time details such as:-   Breakdown of vendors by KPI groups.
-   How many new contracts were created in the last 30 days.
-   How many contracts are ending in the next 90 days.
-   Number of continual improvement initiatives that are currently open.
-   The top five vendor success indicators.

</td><td>

Vendor Manager \[sn\_vlm.vendor\_manager\]

 To view reports on catalog items ordered, the sc\_req\_item access control list \(ACL\) must be enabled.

</td></tr></tbody>
</table>## Indicators

-   **Vendor score**

    Vendor performance of all vendors in your organization that's based on their vendor score for the last 90 days.

-   **Vendor satisfaction**

    Satisfaction of stakeholders who collaborate with your vendors.


## Breakdowns

The indicators breakdown is by vendors.

## Data visualizations

Select a visualization to drill down and analyze further details.

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Vendors by KPI group|Donut\[Omitted image "icon-donut-report.png"\] Alt text: Donut|Company \[core\_company\]|Breakdown of vendors KPI groups.|
|New contracts|Single score\[Omitted image "single-score.png"\] Alt text: Single score report|Contract \[ast\_contract\]|Number of contracts created in the last 30 days.|
|Contracts ending|Single score\[Omitted image "single-score.png"\] Alt text: Single score report|Contract \[ast\_contract\]|Number of contracts ending the next 90 days.|
|Improvement initiatives|Single score\[Omitted image "single-score.png"\] Alt text: Single score report|Improvement Initiative \[sn\_cim\_register\]|Number of active improvement initiatives.|

**Parent Topic:**[Managing vendors using Vendor Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/vendor-management-workspace/using-vendor-management-workspace.md)

