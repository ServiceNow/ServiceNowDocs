---
title: Mapping alerts and events for the Splunk Enterprise Event Ingestion integration
description: After you identify the sources for scheduled alert ingestion or manual event forwarding, the next step is to map individual event fields to the fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create and name an event profile for the Splunk Enterprise Event Ingestion integration, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Mapping alerts and events for the Splunk Enterprise Event Ingestion integration

After you identify the sources for scheduled alert ingestion or manual event forwarding, the next step is to map individual event fields to the fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.

## Overview of Mapping alerts and events

For the mapping step, as a user with the **sn\_si.ingestion\_profile\_admin** role, you ingest sample alerts from your Splunk Enterprise console, or you export event data for a Splunk Enterprise event.

The following figures are examples of the default mapping grids that are provided for each type of event profile. This default mapping can be edited. This modification allows you to customize the fields that populate the security incident. With the mapping step, you can visualize how adding or removing event fields impacts the SIR security incident field values.

Select the **Alert Name**, and after you click to **Fetch Sample Data**, the Splunk alert field values are populated on the left side of the form when sample alerts are ingested by the profile. These are the Splunk alert fields that you map to the SIR security incident fields.

![Default mapping form for alerts.](../image/splunk-event-ingestion-alerts-mapping-fetch.png "Default mapping form for alerts")

After you click to load attachment data for forwarded events, the Splunk event fields are populated on the left side of the form. These are the Splunk data fields that are mapped to the SIR security incident fields.

![Default mapping form for events.](../image/mapping_default.png "Default mapping form for forwarded events")

You may prefer to review a few sample alerts on your Splunk console to ingest for the field mapping configuration step. This step is labeled, **Mapping** on the progress bar. If this page is not displayed, click **Mapping** on the progress bar.

Mapping alerts and exporting events on-demand from your Splunk enterprise console includes the following concepts and tasks:

-   Fetch Sample data for automatically ingested alert profiles. After data is fetched \(pulled\) from a fired alert on the Splunk Enterprise console, available alert fields and their corresponding values are displayed in a default mapping layout on the left side of the mapping form. Tabs are displayed for you to view the values for an alert ID that you pulled. Verify that all the critical fields from the Alert Sample Ingestion section on the left of the form are mapped to the grid on the right of the form.
-   If required, load event sample data for any manually forwarded event profiles. Sample data for these events is exported in a `.xml` file from the Splunk Enterprise console and loaded into your ServiceNow AI Platform® instance. The imported data is displayed in the Alert Sample Ingestion section on the left of the form.
-   Edit the mapping configuration by dragging alerts from the left side and dropping them on the mapping grid on the right. The mapping grid on the right associates the incoming alert field with an outgoing security incident field.
-   Customize the mapping grid by adding or removing fields. Track overlooked or duplicated fields with the color coding that is provided.
-   Set filter conditions so that you can specify which alerts are ingested into the SIR application, and which alerts are filtered out.
-   Define additional incident field criteria that aggregates an incoming alert to an existing SIR security incident to prevent duplicate incidents. This additional filtering can reduce the number of active, overlapping security incidents by placing all related security event data on a single security incident.
-   In certain cases, event field values in the Splunk Enterprise console may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical. For example, with the script editor, the Malware Alert and Virus Infection field values in the Splunk console both translate to Malicious Code Activity in the Category field on the SIR security incident.

## Scheduled alert profiles

After creating a scheduled alert profile, the process flow for the configuration is shown in the following figure.

![Process flow for scheduled alert.](../image/splunk_alert_flow.png "Process flow for scheduled alert profiles")

## Manual Event forwarding profiles

After creating a profile for an event, the process flow for the configuration is shown in the following figure.

![Process flow for event export.](../image/splunk_event_flow.png "Process flow for event profiles")

The next step is to ingest triggered alerts or export data and map values to the SIR security incident fields.

**Parent Topic:**[Create and name an event profile for the Splunk Enterprise Event Ingestion integration](../task/splunk-event-ingest-create-profile.md)

