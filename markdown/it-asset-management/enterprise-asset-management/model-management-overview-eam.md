---
title: Enterprise model management overview for Enterprise Asset Workspace
description: Use the Enterprise model management view in the Enterprise Asset Workspace to create and manage enterprise models. You can also view details such as model lifecycle overview, model status, and enterprise models up for end of life.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enterprise Asset Workspace, Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Enterprise model management overview for Enterprise Asset Workspace

Use the Enterprise model management view in the Enterprise Asset Workspace to create and manage enterprise models. You can also view details such as model lifecycle overview, model status, and enterprise models up for end of life.

Take care of any urgent model related action items such as entering a missing model number or manufacture name.

You can access the Enterprise model management view by navigating to **Enterprise Asset Workspace** &gt; **Enterprise model management**.

To access detailed information and take relevant action, select any widget. You can also narrow your results by using the **Model category** filter.

![Model management view](../image/modeloverview.png "Enterprise model management view")

<table id="table_a3f_2h4_nrb"><thead><tr><th>

Widget or chart

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enterprise models up for end of life this year

</td><td>

Count of enterprise models whose start date of the end of life phase is the current year.

</td></tr><tr><td>

Consumable models up for end of life this year

</td><td>

Count of consumable models whose start date of the end of life phase is the current year.

</td></tr><tr><td>

Missing data

</td><td>

Count of models that have missing model name, manufacturer, and model number.

</td></tr><tr><td>

Model lifecycle overview

</td><td>

Count of models that are present in each life cycle stage such as General Availability, End of Support, End of Life, and End of Sale.

</td></tr><tr><td>

Alternate equipment maintenance models

</td><td>

Count of models for which alternate equipment maintenance is enabled and are grouped by model categories.

</td></tr><tr><td>

Model status

</td><td>

Current count of models based on the status of the models.

</td></tr><tr><td>

Enterprise model risk heat map

</td><td>

Displays the risk heat map for number of models that have the likelihood and impact values. To view this heat map, ensure that the band score records in the Risk Score module are frozen.**Note:** If risk likelihood, risk impact, and risk score are not frozen, the heat map is rendered in a draft mode with no risk values in the model record. If only one of these vectors is frozen, the heat map is not rendered. If all three vectors are frozen, the heat map is rendered in a production mode and the risk values are populated in the model record.

</td></tr></tbody>
</table>