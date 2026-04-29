---
title: Integrating Microsoft 365 with ServiceNow reporting
description: The Microsoft 365 for ServiceNow Reporting \(sn\_esg\_msoff\_intg\) integration provides disclosure reporting capabilities to ESG reporting disclosure managers to seamlessly report ServiceNow Operational Sustainability Management system data, list reports, charts, pivot, and multi pivot reports using Microsoft Word.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Integrating Microsoft 365 with ServiceNow reporting

The Microsoft 365 for ServiceNow Reporting \(sn\_esg\_msoff\_intg\) integration provides disclosure reporting capabilities to ESG reporting disclosure managers to seamlessly report ServiceNow Operational Sustainability Management system data, list reports, charts, pivot, and multi pivot reports using Microsoft Word.

An ESG reporting disclosure manager may need to create disclosures to be transparent with the stakeholders about the impact of their activities. For example, if an organization is planning to engage in an activity that requires them to drill for oil in a protected area, the disclosure manager may create a disclosure that outlines the potential impacts of the activity on the environment and local communities as well as the measures being taken to mitigate those impacts.

This integration allows the reporting managers to view the inventory of the ServiceNow Operational Sustainability Management data links on the disclosure report and refresh the inserted data to be in synchronization with the latest ServiceNow Operational Sustainability Management data. An audit trail is also established between the data imported and the ServiceNow instance. The audit trail provides any auditor the ability to click the links in the document and access the source of the data in the ServiceNow instance.

You can also track any changes made to the data inserted using configuration and log those changes in the log table. For more information see, [Set up Microsoft 365 reporting configuration](../task/configure-o365-reporting-configs.md).

**Note:** This integration is compatible with the desktop version 16.71 \(23031200\) and the web version 16.0.16412.41005 of Microsoft Word. However, the charts are not interactive in the web version. This means that you cannot modify the chart colors, formats, and so on. The supported Windows Office version is 2303 \(Build 16130.20394\).

You can change the format, style, and colors of the imported data. The following chart styles are supported in this integration:

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

![The data that is imported from an instance in to a Word document.](../images/data-imported-in-word-doc.jpg "How various types of imported data appears in a document")

-   **[Workflow of Microsoft 365 for ServiceNow Reporting](workflow-ms-365.md)**  
The Microsoft 365 for ServiceNow Reporting integration utilizes a workflow that requires participation from multiple user roles such as system administrators, ESG administrators, and disclosure managers. By defining a clear workflow, individuals and teams can better understand their roles and responsibilities and generate the necessary disclosures.
-   **[Install the ServiceNow Reporting add-in](../task/install-o365-addin.md)**  
Install the ServiceNow Reporting add-in to your Microsoft Word document. This add-in is required to import reports and data from your ServiceNow® instance to Microsoft Word documents to create disclosure reports.
-   **[Set up Microsoft 365 reporting configuration](../task/configure-o365-reporting-configs.md)**  
Set up the Microsoft 365 reporting configuration records to specify the data points and reports that you want to import in to a Microsoft Word document for disclosure reporting purposes.
-   **[Add additional reporting configuration filters for a Microsoft 365 configuration record](../task/add-additional-reporting-filters.md)**  
Add additional reporting filters to specify at a granular level what data must be imported to the disclosure report from a table.
-   **[Add the ServiceNow Reporting add-in into Microsoft Word](../task/add-the-sn-esg-addin-into-ms-word.md)**  
Before you can import data into your Microsoft Word document to create your disclosure reports, you must add the ServiceNow Reporting add-in to your Microsoft Word.
-   **[Import data in to a Microsoft Word disclosure report](../task/import-data-into-ms-word.md)**  
Import and insert data and reports into a Microsoft Word disclosure report document from a ServiceNow instance. You can only import and insert the data that is configured in your reporting configurations.

**Parent Topic:**[Integrating Operational Sustainability Management \(formerly ESG\) with other applications](integrate-esg.md)

