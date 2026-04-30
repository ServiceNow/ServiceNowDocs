---
title: Working with Reports in TISC
description: The Reports module in the Threat Intelligence Library section enables you to create, manage, and publish reports that use any intelligence available in the Threat Intelligence Library.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-11-24"
reading_time_minutes: 4
breadcrumb: [TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Working with Reports in TISC

The Reports module in the Threat Intelligence Library section enables you to create, manage, and publish reports that use any intelligence available in the Threat Intelligence Library.

Reports in the threat intelligence library are categorized into case reports and intelligence reports.

They support key capabilities such as previewing, publishing, sharing via email, and downloading. These reports provide analysts with a structured and shareable format for threat intelligence reporting.

## Case Reports

Case Reports contain information specific to an individual case. Using the case designated templates, analysts can generate reports that automatically pull data from the fields, related records, and intelligence within the selected case.

Access to the Case Reports is strictly controlled. Only users or groups with permission to access the case can view or interact with its reports. Without the appropriate permissions, the report and its contents are not accessible.

Case Reports follow the same structure and capabilities as the existing CTI case reporting. For more information, see [About Report Templates in TISC](tisc-report-templates.md). These case reports appear in **All Reports** and **Case Reports** views of the threat intelligence library **Reports** module providing a structured and secure result for case level investigations.

## Intelligence Reports

Intelligence Reports provide a flexible way to generate structured reports using any available threat intelligence from the Threat Intelligence Library. Using templates of the **Intelligence Report** category, analysts can create reports that incorporate data from library lists and specific intelligence objects without depending on a case.

Unlike Case Reports, Intelligence Reports do not display case-specific fields or records. Instead, analysts can use record selection tools, slash commands, and table insertion options to customize the content of the report.

Slash commands in the threat intelligence report allow you to quickly insert dynamic content such as record counts, specific records, or system users into a report.

The following describes the usage of slash commands available within the Intelligence Report Editor.

<table id="table_bqn_lgf_nhc"><thead><tr><th>

Slash Command

</th><th>

Usage

</th><th>

Wokflow

</th><th>

Supported Tables

</th></tr></thead><tbody><tr><td>

Mention Count

</td><td>

When you select this option, you can choose a table from the **Supported Tables** list to add the total record count to the report.

</td><td>

1.  Select **Mention Count** from the slash command menu.
2.  Choose a table from the supported table list.
3.  The application inserts the total records count for the selected table into the report.

</td><td rowspan="2">

-   Observable
-   Indicator
-   Attack Pattern
-   Campaign
-   Course of Action
-   Identity
-   Infrastructure
-   Intrusion Set
-   Location
-   Malware
-   Malware Analysis
-   Marking Definition
-   Object Sighting
-   Observed Data
-   Threat Actor
-   Threat Event
-   Threat Grouping
-   Threat Note
-   Threat Opinion
-   Threat Report
-   Tool
-   Vulnerability
-   Data Component
-   Data Source

</td></tr><tr><td>

Select a RecordWhen you navigate to an observable and type “/”, an option to select a corresponding fields appears. This allows you to browse and search the available fields for that record. Selecting a field automatically inserts its value into your input.

The following is the screen shot that illustrates the navigation of selecting a record\(s\) using slash command.

</td><td>

You can select a table from the provided **Supported Tables** list, and once selected, a drop down menu will display all the available records in that table, allowing you to choose the desired record.

</td><td>

1.  Select **Mention Count** from the slash command menu.
2.  Choose a table from the supported table list.
3.  The application inserts the total record count for the selected table into the report.

</td></tr><tr><td>

Select a User

</td><td>

By selecting this option, you can choose any individual from the list of system users to include in the report.

</td><td>

1.  Select **Select a User** from the slash command menu.
2.  Choose a user from the system user list.
3.  The selected user is inserted into the report.

</td><td>

NA

</td></tr></tbody>
</table>Reports include pre-defined templates, tables offering a comprehensive view of relevant intelligence.

Intelligence Reports appear in the **All Reports** and **Intelligence Reports** views of the threat intelligence library **Reports** module.

-   **[View All Reports](tisc-reports.md)**  
Use this section to view all the list of reports.
-   **[View Case Reports](../task/tisc-case-reports.md)**  
View Case Reports.
-   **[View Intelligence Reports](../task/tisc-view-intel-reports.md)**  
View intelligence reports.
-   **[View my reports](../task/tisc-view-my-reports.md)**  
View the reports that you created.

**Parent Topic:**[TISC Library Repository](tisc-ioc.md)

**Related topics**  


[Observables](observables.md)

[Indicators](indicator.md)

[Threat Entities](tisc-threat-entities.md)

[Other Objects](tisc-other-objects.md)

[Vulnerability](vulnerability.md)

[Define RSS Feeds](../task/define-rss-feeds.md)

[MITRE-ATT&amp;CK Repository](tisc-mitre-att-ck-framework-overview.md)

[Relationships Objects](relationship-objects.md)

[Potential Relationships](potential-relationships.md)

[Vulnerability relationship mapping](tisc-vul-relationship-map.md)

