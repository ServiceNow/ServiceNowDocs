---
title: Explore Mapping
description: After you identify the specific correlation rule and notable event type for the profile, the next step is to map individual notable event fields to the fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up a profile for scheduled notable event ingestion, Create an event profile, Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Explore Mapping

After you identify the specific correlation rule and notable event type for the profile, the next step is to map individual notable event fields to the fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.

## Overview of Mapping

For the mapping step, you can ingest sample notable events for the selected correlation rule or export notable event data for manually forwarded notable events. The event mapping process is identical regardless of the profile type you are creating.

The following figures are examples of the default mapping configurations that are provided for each type of event profile. You can customize the fields that populate the security incident. During this mapping phase, you can ensure all relevant notable event field data is mapped to the appropriate place on the SIR incident form and then visualize the SIR incident in the preview section.

If Multiple correlations are used, then notable events can be fetched by selecting required Event. Use **Alert Name** to choose your alert if you have configured multiple alerts for ingestion.

After you click to fetch data, the Splunk notable event field names and corresponding values are populated on the left side of the form. These are the Splunk notable event fields that are available to map to the SIR security incident fields. Some fields can be mapped multiple times to the SIR security incident fields.

![Default mapping for scheduled notable events](../image/new-images/splunk_es_default_notable.png)

You may prefer to review a few sample notable events on your Splunk console to ingest for the field mapping configuration step. This step is labeled Mapping on the progress bar. If this page is not displayed, click **Mapping** on the progress bar. You can ingest up to five sample notable events from Splunk Enterprise Security to assist with the notable event field mapping process. There are options to either ingest the five most recent notable events for the correlation rule selected or ingest up to five specific notable events based on the notable event IDs.

Below is a summary of the steps required to map notable events:

-   Scheduled Notable Event Sample Data Ingestion: For sample data that is used for automatically ingested notable event profiles, available notable event fields and their corresponding values are displayed in a default mapping layout on the left side of the mapping form once the sample data is retrieved. Tabs are displayed for you to view the values for a specific notable event ID that you pulled. Verify that all the critical fields from the notable event sample ingestion section on the left of the form are mapped to ServiceNow security incident fields on the right of the form.
-   Field Mapping: Edit the mapping configuration by dragging notable event fields from the left side and dropping them on the ServiceNow SIR incident mapping section on the right. The mapping on the right associates the incoming notable event field with an outgoing security incident field.
-   Mapping Experience: Customize the mapping grid by adding or removing fields using the + icon at the bottom of the SIR incident field mapping section. Track overlooked or duplicated fields with the color coding that is provided \(mapped fields are greyed out, blue fields are unmapped\).
-   Incident Generation Conditions: Once the mapping section is complete, you can set filter conditions so that you can specify which notable events should create security incidents versus which notable events should be filtered out, for example, low priority notable events. This is done in the Incident Generation Conditions section located below the Notable Event Mapping section.
-   Event Aggregation Criteria: Define additional Event Aggregation criteria that aggregates an incoming notable event to an existing SIR security incident instead pf creating similar, potentially duplicate incidents. Using field matching value criteria for each profile, this additional aggregation capability can reduce the number of active, overlapping security incidents by placing all related security notable event data on a single security incident.
-   Format Field Translation: In certain cases, event field values in the Splunk Enterprise notable events may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical. For example, with the script editor, a category value of Malware Alert and Virus Infection may have different field values for the source category but both values can be translated to a common Malicious Code Activity in the Category field on the SIR security incident using the Format Field Translation functionality.

The next step is to ingest notable events and map values to the SIR security incident fields.

