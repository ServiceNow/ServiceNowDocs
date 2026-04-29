---
title: View territory information in contextual side panel
description: The contextual side panel offers valuable insights and easy access to territory information, helping you make well-informed decisions and efficiently manage your territories.
locale: en-US
release: australia
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing territories and agents, Managing workforce, Use, Field Service Management]
---

# View territory information in contextual side panel

The contextual side panel offers valuable insights and easy access to territory information, helping you make well-informed decisions and efficiently manage your territories.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager, sn\_fsm\_tp.fsm\_territory\_read

## About this task

The contextual side panel provides comprehensive details about territories, markers, shapes, and heatmaps. Administrators can configure the displayed fields to show precisely the information needed. For more information, see [Configure territory fields to appear in Territory Planning console](configure-fields-to-appear-in-contextual-side-panel.md).

In the contextual side panel:

-   Clicking on a map marker icon representing a single data item displays the specific details of that data item.
-   Clicking on a co-located marker icon representing multiple data items, lists all the associated data items in the contextual side panel. To view specific details for each record, select the individual items.
-   Use the condition builder to further filter the data items. For example, add a condition to display only active work order tasks.

Territory Key Performance Indicators \(KPIs\) offer valuable insights into the performance of territories. The contextual side panel displays the KPIs for the territory. When your administrator activates the Performance Analytics - Content Pack - Field Service Management plugin. The KPIs configured in the `TerritoryIndicators (sn_fsm_tp.TerritoryIndicators)` extension point appear in the contextual side panel.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console**.

2.  In the Territories panel, select the territory you want to view.

3.  View details in the contextual side panel.

<table id="choicetable_wc2_mgn_2yb"><thead><tr><th align="left" id="d147987e123">

To view

</th><th align="left" id="d147987e126">

Do the following

</th></tr></thead><tbody><tr><td id="d147987e132">

**Map overlay data items**

</td><td>

-   Select the map marker on the map. The contextual side panel in the map provides detailed information about the selected map marker.
-   You can customize the display using the Settings icon \(![Settings icon](../image/IconPersonalizeList.png)\).


</td></tr><tr><td id="d147987e156">

**Territory**

</td><td>

-   Select a territory card from the territories panel, then select its geographical area. The contextual side panel displays information about the selected territory and its KPIs.
-   You can customize the display using the Settings icon \(![Settings icon](../image/IconPersonalizeList.png)\).
-   Additionally, access related data by selecting the **Related** tab in the contextual side panel.


</td></tr></tbody>
</table>
## Result

The following snapshot illustrates how you can view relevant territory information and its KPIs in the contextual side panel, helping you to efficiently manage your territories and resources. ![Snapshot displaying the San Diego territory details and Key Performance Indicators in the contextual side panel.](../image/territory-planning-csp.jpg)

