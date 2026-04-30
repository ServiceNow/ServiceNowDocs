---
title: Mapping
description: After selecting the LogRhythm source that you want to ingest, you need to map individual LogRhythm alarm fields to the ServiceNow AI Platform security incident fields.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create an alarm profile, LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Mapping

After selecting the LogRhythm source that you want to ingest, you need to map individual LogRhythm alarm fields to the ServiceNow AI Platform security incident fields.

Mapping alarms includes the following tasks:

-   Map LogRhythm alarms. For this task, you list and ingest \(Pull\) sample alarms using the alarm IDs or most recent alarms from the LogRhythm client console.
-   The Sample Alarm fields are categorized into three groups:
    -   Alarm fields: The alarm fields that are available and their corresponding values are displayed.
    -   Event fields: The event fields that are available and their corresponding values are displayed.
    -   DrillDownLog fields: The drilldown log fields that are available and their corresponding values are displayed.
-   Each Alarm ID that you pulled is displayed as a tab. On the Alarm ID tabs, verify that all critical alarm fields from the Alarm Sample Ingestion section on the left of the form are mapped to the SIR Incident Field Mapping section on the right of the form.
-   After you map the alarms to the SIR Incident Field Mapping field, you can see the alarm category also being display in the Input Expression field. For example, `${Alarm: alarmid}$`.
-   You can modify the configuration by adding or removing fields on the security incident. Track overlooked or duplicated fields with the color coding that is provided.
-   You can filter alarms to specify which alarms are ingested into the SIR application. You can either filter the alarms directly or use the alarm categories to drill down your search based on Alarms, Events, or DrillDownLogs.
-   Use the script editor if you want to format values for the Priority and Category fields on the security incident.

The next step is to [Map LogRhythm alarm fields to security incident fields](../task/logrhythm-map-alarms.md).

-   **[Map LogRhythm alarm fields to security incident fields](../task/logrhythm-map-alarms.md)**  
You map individual alarm fields to the security incident fields. The preconfigured mapping can be edited, and color coding provided for the fields helps you monitor alarms you have already mapped. This step helps you visualize how your edits impact the fields on the security incident.

**Parent Topic:**[Creating an alarm profile for LogRhythm](../task/create-alarm-profile-logrhythm.md)

**Related topics**  


[Map LogRhythm alarm fields to security incident fields](../task/logrhythm-map-alarms.md)

[Use the script editor to format LogRhythm values](../task/add-scripted-values-logrhythm.md)

[Filter alarms for LogRhythm](../task/filter-alarms-logrhythm.md)

