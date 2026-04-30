---
title: Copy Splunk Enterprise Event Ingestion profiles from one instance to another using export/import functionality
description: You can export and import Splunk Enterprise Event Ingestion profiles settings from one ServiceNow AI Platform instance to a different ServiceNow AI Platform instance.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration architecture and external systems connection, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Copy Splunk Enterprise Event Ingestion profiles from one instance to another using export/import functionality

You can export and import Splunk Enterprise Event Ingestion profiles settings from one ServiceNow AI Platform instance to a different ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

This functionality allows the security administrator to copy profiles that have been tested and verified on one ServiceNow AI Platform instance, for example on non-production, to another ServiceNow AI Platform instance, for example production, without the need to redo all configuration settings. The settings that are exported and imported include profile name, correlation rules, mappings, filters, aggregation criteria, field translations, fetched sample data, scheduling, and configuration tile source information.

**Note:** When you export a manual event forwarding profile type, the attachment data used for the sample field mapping is copied, however, the attachment file itself is not exported.

## Procedure

1.  Navigate to **All** &gt; **Splunk Integration** &gt; **Splunk Event Profiles**.

2.  Select a profile that you want to export to another ServiceNow AI Platform instance.

    You can select multiple profiles for export.

3.  From the Actions menu, click **Export**.

4.  Once the export complete message appears, click **Download**.

    The following illustration shows exporting a Splunk profile \(Manual Profile 2\) from your ServiceNow AI Platform instance \(psand.service-now.com\).![Exporting Splunk profiles.](../image/splunk-event-ingestion-export.gif)

    The exported payload.xml file is downloaded on your computer. The file contains the profile name, correlation rules, mappings, filters, aggregation criteria, field translations, fetched sample data, scheduling, and configuration tile source information. When you select and download multiple profiles, they appear in the same payload.xml file.

    You can now proceed to import the profile in another ServiceNow AI Platform instance.

5.  Navigate to **Splunk Integration** &gt; **Splunk Event Profiles**.

6.  Click **Import**.

7.  Click **Choose file** and select the xml file on your computer.

8.  Click **Upload**.

9.  Click **Close and Reload Profiles**.

    The following illustration shows importing a Splunk profile \(Manual Profile 2\) from the ServiceNow AI Platform instance \(psand.service-now.com\) to another ServiceNow AI Platform instance \(ppsand.service-now.com\).

    ![Importing Splunk profiles.](../image/splunk-event-import.gif)

    You have successfully imported the profile from another ServiceNow AI Platform instance.

    Verify that the exported Source \(Splunk API account and Splunk server URL\) and MID Server configuration settings are valid and available in imported ServiceNow AI Platform instance. Update your Splunk Enterprise Event Ingestion configuration if required.

10. Verify the MID Server settings after your import a profile.

11. Navigate to **Security Operations** &gt; **Integration Configurations**.

12. Select the Splunk Enterprise Event Ingestion configuration tile, and click **Update**.

13. Review and update the Source and MID Server details as required.


**Parent Topic:**[Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration](../concept/splunk-event-ingest-integration-architecture.md)

