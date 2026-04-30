---
title: Customer Experience components
description: Several types of components are installed with the Customer Experience feature, including properties, tables, and business rules.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins for Field Service Management, Field Service Management reference, Field Service Management]
---

# Customer Experience components

Several types of components are installed with the Customer Experience feature, including properties, tables, and business rules.

## Tables

Customer Experience adds the following table.

<table id="table_uyt_lvc_zmb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent Rating\[wm\_agent\_rating\]

</td><td>

Stores the agent rating record.

</td></tr></tbody>
</table>## Properties

Customer Experience adds the following properties.

<table id="table_onn_brc_zmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_fsm\_customer\_ex.work.management.cx.share\_agent\_details

</td><td>

Updates the geolocation map with the latest location of an agent.-   Type: true/false
-   Default value: true
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

sn\_fsm\_customer\_ex.work.management.cx.show\_route\_on\_map

</td><td>

Displays the route taken by an agent on a map. -   Type: true/false
-   Default value: true
-   Location: **Field Service** &gt; **Administration** &gt; **Properties**

 **Note:** If this property is disabled, the map displays a straight line route.

</td></tr></tbody>
</table>## Business rules

Customer Experience adds the following business rules.

<table id="table_cqs_q5c_zmb"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Auto assessment business rule

</td><td>

Work Order Task \[wm\_task\]

</td><td>

Triggers an agent feedback survey when a work order task is set to Complete.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

