---
title: Widget form
description: Use the widget form to configure a new widget.
locale: en-US
release: zurich
product: Demand Management
classification: demand-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Demand Management forms, Reference, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Widget form

Use the widget form to configure a new widget.

<table id="table_osc_b4b_xvc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the widget.

</td></tr><tr><td>

Scripted

</td><td>

Option for indicating the value on the widget is from a code script.By default, this option is selected and is read-only.

</td></tr><tr><td>

Show Label

</td><td>

Option for displaying either the label or the color indicator.If you clear the check box, the **Color** field appears and you can set the color.

</td></tr><tr><td>

Active

</td><td>

Option for indicating the status of the widget.Only active widgets are shown on the Demand Financials page.

</td></tr><tr><td>

Parent widget

</td><td>

Widget that is the parent of the current widget.The current widget displays in the Child widgets related list of the selected widget.

 You can add a maximum of three child widgets for a parent widget.

</td></tr><tr><td>

Formatter required

</td><td>

Option for specifying whether a currency formatter is required for the widget.

</td></tr><tr><td>

Script

</td><td>

Code script that returns a requested metric value that is displayed on the widget.

 In the script, use the context and filter objects. The context object contains all the demand financial fields, such as total\_costs, irr\_value, and capital\_budget.

 The following sample script returns the capital budget metric value of a demand to appear on the widget.

 ```
var context = JSON.parse(context);
var filter = context.filters;

var now_GR = new GlideRecord('dmn_demand');
gr.addEncodedQuery(filter['dmn_demand']);
gr.query();
if(gr.next())
	gr.getValue('capital_budget');
Collapse
```

</td></tr><tr><td>

Short description

</td><td>

Description of the widget.

</td></tr></tbody>
</table>**Parent Topic:**[Demand Management forms](../concept/demand-management-forms.md)

