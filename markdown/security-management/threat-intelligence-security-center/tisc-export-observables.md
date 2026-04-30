---
title: Export intelligence data
description: Use the export feature to manually export the intelligence data in various formats.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-04-15"
reading_time_minutes: 2
breadcrumb: [Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Export intelligence data

Use the export feature to manually export the intelligence data in various formats.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

Currently, the export functionality is limited to observables, indicators, and case management. The following procedure describes how you can export the observables data, and follow the same procedure to export the indicators data.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Observables** &gt; **All Observables**.

2.  Select any observable\(s\).

3.  Click **Export** button.

    **Note:** The **Export** button is enabled only when observables are selected for export. If no observables are selected, the button remains disabled.

4.  Select the desired file type for export.

    Currently, the supported export formats are Excel, CSV, and STIX 2.1 JSON. Suppose, if your export type is Excel then the number of records that can be exported at a time is limited to 10,000, regardless of the selected format type.

    If the selection exceeds 10,000 records, then an error message is displayed indicating that the maximum limit for the selected format type has been surpassed, and only the first 10000 records will be exported.

    If the export format is CSV and the record limit is exceeded, an alert message will be displayed indicating that the export is **in progress** state, along with a link to view the export status. You can click the link to view the status, refresh the record, and once it moves to **processed** state after refreshing then you can download the attachment.

5.  Click **Export**.

    **Note:** You can also view export data from the **Imports/Exports** module.

    A confirmation message displayed indicating that the export is successful and your download is complete.


**Parent Topic:**[Threat Intelligence Security Center Library](../concept/threat-intelligence-security-center-library.md)

**Related topics**  


[Understanding the Data Model](../reference/understanding-the-data-model.md)

[TISC Library Objects form view](../concept/tisc-library-home-page-view.md)

[TISC Library Repository](../concept/tisc-ioc.md)

[Access Vulnerability Downstream actions](../concept/downstream-actions-from-the-vulnerability-form-view.md)

[Deleting threat intelligence library records](tisc-delete-lib-records.md)

[Confirm Potential Relationships from Related Records](confirm-potential-relationships.md)

[Automated Correlation](../concept/automated-correlation-rules.md)

