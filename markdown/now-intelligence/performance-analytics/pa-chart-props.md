---
title: Chart properties for Performance Analytics
description: A chart refers here to a graphical component of a Performance Analytics widget or the Analytics Hub. These properties apply only to the Core UI, not visualizations in configurable workspaces.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Properties, Reference, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Chart properties for Performance Analytics

A chart refers here to a graphical component of a Performance Analytics widget or the Analytics Hub. These properties apply only to the Core UI, not visualizations in configurable workspaces.

<table id="table_mxc_mgp_wx"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.pa.default\_chart\_line\_color

</td><td>

Color of the scores in the Analytics Hub and widgets, including the trend line and bullet chart.

-   Format: RGBA
-   Default: 106,183,239,1

</td></tr><tr><td>

com.snc.pa.text.trendline\_points\_for.frequency

</td><td>

Maximum number of points visible in the text analytics trend-lineDefault: 30

</td></tr><tr><td>

com.snc.pa.default\_chart\_target\_color

</td><td>

Color of the target in a graph. -   Format: Hexadecimal
-   Default: \#506163

</td></tr><tr><td>

com.snc.pa.default\_chart\_personal\_target\_color

</td><td>

The line color for personal targets displayed on the Analytics Hub for a single indicator.

-   Type: string
-   Default value: \#879394

</td></tr><tr><td>

com.snc.pa.default\_chart\_threshold\_color

</td><td>

Color of the threshold in a chart. -   Format: Hexadecimal
-   Default: \#506163

</td></tr><tr><td>

com.snc.pa.default\_chart\_personal\_threshold\_color

</td><td>

The line color for personal thresholds displayed on the Analytics Hub for a single indicator.

-   Type: string
-   Default value: \#879394

</td></tr><tr><td>

com.snc.pa.default\_chart\_area\_color0

</td><td>

Color of the first gradient area in a chart. -   Format: RGBA
-   Default: 106,183,239,1

</td></tr><tr><td>

com.snc.pa.default\_chart\_area\_color1

</td><td>

Color of the second gradient area in a chart. -   Format: RGBA
-   Default: 106,183,239,0

</td></tr><tr><td>

com.snc.pa.navigator\_line\_color

</td><td>

Color of the Line in the chart navigator.

-   Format: RGBA.
-   **Default:**106,183,239,1

</td></tr><tr><td>

com.snc.pa.navigator\_area\_color0

</td><td>

Color of the first gradient area in the chart navigator. -   Format: RGBA.
-   Default: 204,204,204,0.25

</td></tr><tr><td>

com.snc.pa.navigator\_area\_color1

</td><td>

Color of the second gradient area in the chart navigator. -   Format: RGBA.
-   Default: 204,204,204,0.5

</td></tr><tr><td>

com.snc.pa.navigator\_mask\_fill\_color

</td><td>

Deprecated in the Analytics Hub. Mask fill color of the chart navigator.

-   Format: RGBA.
-   Default: 106,183,239,0.25

</td></tr><tr><td>

com.snc.pa.spark\_line\_width

</td><td>

Pixel width of the chart line. Used only on the workbench widget. Default: 1

</td></tr><tr><td>

com.snc.pa.scorecard.breakdown.chart.name\_max\_length

</td><td>

Maximum number of element names on the legend in a breakdown widget. Default: 27

</td></tr></tbody>
</table>**Parent Topic:**[Performance Analytics properties](pa-properties.md)

