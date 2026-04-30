---
title: Integrating Microsoft 365 with Management Reporting of Risk
description: The Management Reporting of Risk \(sn\_grc\_mgmt\_report\) integration provides reporting capabilities to Risk reporting managers to report ServiceNow Risk Management system data, list reports, charts, pivot, and multi-pivot reports using Microsoft Word.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Integrating Microsoft 365 with Management Reporting of Risk

The Management Reporting of Risk \(sn\_grc\_mgmt\_report\) integration provides reporting capabilities to Risk reporting managers to report ServiceNow Risk Management system data, list reports, charts, pivot, and multi-pivot reports using Microsoft Word.

The risk managers prepare reports for board members or senior management periodically to provide updates on the risk profile based on the information available in ServiceNow.

This integration enables the risk reporting managers to view the inventory of the ServiceNow Risk Management data links on the report and refresh the inserted data to be in synchronization with the latest ServiceNow Risk Management data. An audit trail is also established between the data imported and the ServiceNow instance. The audit trail provides any auditor the ability to select the links in the document and access the source of the data in the ServiceNow instance.

**Note:** This integration is compatible with the desktop version 16.71 \(23031200\) and the web version 16.0.16412.41005 of Microsoft Word. However, the charts aren’t interactive in the web version. This means that you can’t modify the chart colors, formats, and so on. The supported Windows Office version is 2303 \(Build 16130.20394\).

You can also change the format, style, and colors of the imported data. The following chart styles are supported:

<table id="table_u13_znk_2xb"><thead><tr><th>

Chart type

</th><th>

Styles supported

</th></tr></thead><tbody><tr><td>

Pie chart

</td><td>

-   Chart color
-   Display data label
-   Chart title
-   Show legend

</td></tr><tr><td>

Bar chart

</td><td>

-   Chart color
-   Display data label
-   Chart title
-   X-Axis and Y-Axis
    -   Title
    -   Title bold
    -   Display grid
    -   Label bold

</td></tr><tr><td>

Horizontal bar chart

</td><td>

-   Chart color
-   Display data label
-   Chart title
-   X-Axis
    -   Title
    -   Title bold
    -   Display grid
    -   Label bold
-   Y-Axis
    -   Display grid
    -   Label bold

</td></tr></tbody>
</table>The following image shows how the imported data appears in a document.

![How the imported data appears in a Word document.](../image/data-imported-risk-instance-word.jpg "How various types of imported data appears in a document")

