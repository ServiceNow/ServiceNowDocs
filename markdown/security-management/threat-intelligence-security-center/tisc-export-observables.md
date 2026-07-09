---
title: Export intelligence data
description: Use the export feature to manually export the intelligence data in various formats.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/tisc-export-observables.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-03"
reading_time_minutes: 2
keywords: [export,intelligence data,tisc,observables,marking definition,tlp2.0]
breadcrumb: [Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Export intelligence data

Use the export feature to manually export the intelligence data in various formats.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

The export functionality is limited to observables, indicators, and case management. The following procedure describes exporting observables data. Follow the same procedure to export indicators data.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables** &gt; **All Observables**.

2.  Open any observable record.

3.  Select **Export**.

    **Note:** The **Export** button is enabled only when observables are selected for export. If no observables are selected, the button remains inactive.

4.  Select the desired file type for export.

    -   The supported export formats are Excel, CSV, and STIX 2.1 JSON. If your export type is Excel, you can export up to 10,000 records at a time.
    -   If the selection exceeds 10,000 records, the system displays an error message indicating that the maximum limit has been surpassed. Only the first 10,000 records will be exported.
    -   If the export format is CSV and the record limit is exceeded, the system displays an alert message. The message indicates that the export is in progress, along with a link to view the export status. You can click the link to view the status, and refresh the record. After it moves to **processed** state, you can download the attachment.

        **Note:** When you export records in STIX 2.1 format, the system includes Traffic Light Protocol \(TLP\) definitions applied to the intelligence object. The export includes them as TLP 2.0 marking definition objects. For more information, see [Define Marking Definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/define-market-definition.md).

5.  Select **Export**.

    **Note:** You can also view export data from the **Imports/Exports** module.

    The system displays a confirmation message indicating that the export is successful and your download is complete.


**Parent Topic:**[Threat Intel Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/threat-intelligence-security-center-library.md)

**Related topics**  


[Understanding the Data Model]()

[TISC Library Objects form view]()

[TISC Library Repository]()

[Access Vulnerability Downstream actions]()

[Deleting threat intelligence library records]()

[Confirm Potential Relationships from Related Records]()

[Automated Correlation]()

