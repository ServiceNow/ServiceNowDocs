---
title: Portal board widget form
description: Learn about the fields of portal board widget form.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Form field information for Project Management, Project Management reference, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Portal board widget form

Learn about the fields of portal board widget form.

<table id="table_oc2_3zk_xcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the widget you are configuring.

</td></tr><tr><td>

Order

</td><td>

The order in which your widgets appear on both your Investment Board and the Investment Portal page. Lower numbers are placed ahead of higher numbers.

 For example, a widget with an order set to 100 appears before a widget with an order set to 200.

</td></tr><tr><td>

Aggregate type

</td><td>

Type of aggregation applied for the investment widget calculation: **Sum**, **Average**, **Minimum**, **Maximum**, and **Count**.For example, you are aggregating the actual cost of three projects, A, B, and C, surfaced by a filter. Actual costs are 1000 for project A, 2000 for project B, and 3000 for project C.

 If sum is selected as the aggregate type, then the actual cost metric value would be 6000. If average is selected as the aggregate type, then the actual cost metric value would be 2000. If minimum is selected as the aggregate type, then the actual cost metric value would be 1000. If maximum is selected as the aggregate type, then the actual cost metric value would be 3000. If count is selected as the aggregate type, then the actual cost metric value would be 3.

</td></tr><tr><td>

Scripted

</td><td>

Check box to specify a script for the investment widget calculation.

</td></tr><tr><td>

Show Label

</td><td>

Check box to display either the label or the color indicator.If you clear the check box, the **Color** field displays, which allows you to set the color.

</td></tr><tr><td>

Active

</td><td>

Check box to indicate that the investment widget is active.

</td></tr><tr><td>

Display on board

</td><td>

Check box to display the investment widget on your investment board.

</td></tr><tr><td>

Parent widget

</td><td>

Parent widget for this investment metric widget. A parent widget can have up to a maximum of three child widgets.

</td></tr><tr><td>

Include by default

</td><td>

Check box to show an active investment widget by default on:-   new boards
-   existing boards that do not have widget selection configured

The check box is selected by default.For more information on configuring widgets on an investment board, see [Widget Configuration](../task/use-investment-portal.md#image_cwc_2xh_ycb).

</td></tr><tr><td>

Short description

</td><td>

Brief description about the investment widget.

</td></tr><tr><td>

Script

</td><td>

Script written for the dynamic calculation of investment widget. This field is displayed only when the **Scripted** check box is selected. The following script returns a string containing the desired output to be displayed on widget. Five variables \(which are programmatically introduced to the script\) are available:

 -   projectFilter: Project filter of Investment Portal board.
-   demandFilter: Demand filter of Investment Portal board.
-   projectClass: Project class of Investment Portal board which is used during teamspaces value evaluation. It returns tsp1\_project for Teamspace1 Portal Board.
-   demandClass: Demand class of Investment Portal board which is used during teamspaces value evaluation. It returns tsp1\_demand for Teamspace1 Portal Board.
-   boardSysId: SysId of Investment Portal board. It provides access to more information on Investment Portal board when needed.

 **Sample scripted widget for project cost** ```
totalProjectCost();

function totalProjectCost() 
{
    var totalCost = 0;
    
    if(!JSUtil.nil(projectClass) && !JSUtil.nil(projectFilter))
{ 
        var projectGa = new GlideAggregate(projectClass);
        projectGa.addEncodedQuery(projectFilter);
        projectGa.setGroup(false);
        projectGa.addAggregate('SUM', 'cost');

        projectGa.query();

        if(projectGa.next()) 
{
            if(projectGa.getAggregate('SUM', 'cost'))
            totalCost += parseFloat(projectGa.getAggregate('SUM', 'cost'));
        }
    }
    return PPMCurrencyHelper.defaultCurrencySymbol() + PPMCurrencyHelper.getFormattedAmount(totalCost);
}
```

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Project aggregate column|Aggregation is applied on the selected column of the Project \[pm\_project\] table.|
|Project table|Table from which projects are being filtered.|
|Project filter|Criteria applied to filter projects from the Project table.|

|Field|Description|
|-----|-----------|
|Demand aggregate column|Aggregation is applied on the selected column of the Demand \[dmn\_demand\] table.|
|Demand table|Table from which demands are being filtered.|
|Demand filter|Criteria applied to filter demands from the Demand table.|

**Related topics**  


[Configure your investment metrics as widgets](../task/configure-investment-metrics.md)

