---
title: Select scheduled alerts for the Splunk Enterprise Event Ingestion integration
description: After you have created a profile for a scheduled alert, select a Splunk alert for this profile that you want to map to a ServiceNow AI Platform Security Incident Response security incident.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create an event profile, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Select scheduled alerts for the Splunk Enterprise Event Ingestion integration

After you have created a profile for a scheduled alert, select a Splunk alert for this profile that you want to map to a ServiceNow AI Platform Security Incident Response security incident.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

View the available alerts in your ServiceNow AI Platform instance so you know which field values are available for mapping. Select an alert to verify that you receive the expected results on the basic form layout before you map the values to fields on SIR security incidents. You can only select one alert from the list in this form.

## Procedure

1.  If the Alert Selection page is not displayed, select it on the progress bar to display it.

    By default, the core Search &amp; Reporting App is selected.

2.  If the alert to be ingested is part of a different Splunk app, select **Splunk App Selection** and choose your Splunk app from the **Selected App** list.

3.  From the **Alert List**, choose an alert and move it to from the **Available** column to the **Selected** column.

    You can also choose multiple alerts. If the alerts are selected as part of a single profile, then the alerts will have common field mappings and profile settings.

    The list of alerts on this form matches the list of alerts in your Splunk console. Up to 500 alerts are displayed on this form. If there are more than 500 alerts listed in your Splunk console on the Alerts page, only the first 500 alerts are displayed on this form in your ServiceNow AI Platform instance.

    |Option|Description|
    |------|-----------|
    |In the Alert List search field, enter text.|The column below the search field is filtered with available options based on the text that you enter. Select an alert, and with the arrow keys, move the selected alarm from **Available** to **Selected**.|
    |In the Alert List, double-click an Alert.|The **Selected** column is populated with your selection.|
    |In the Alert List, single-click an alarm rule.|The alarm is selected. With the arrow keys, move the selected alert from **Available** to **Selected**.|

    ![Select an alert for a scheduled event profile.](../image/splunk-event-ingestion-alerts-selection.png)

4.  Choose one option to continue.

<table id="choicetable_svs_ttl_kdb"><thead><tr><th align="left" id="d469907e223">

Option

</th><th align="left" id="d469907e226">

Description

</th></tr></thead><tbody><tr><td id="d469907e232">

**Continue, or alternatively, click Mapping in the progress bar**

</td><td>

The Mapping form is displayed. **Mapping** is selected on the progress bar. The next step is to map alert fields to a SIR security incident.

</td></tr><tr><td id="d469907e249">

**Update**

</td><td>

Your data is saved and the Splunk Event Profiles list is displayed.

</td></tr><tr><td id="d469907e258">

**Previous**

</td><td>

The **Name** step is displayed.

</td></tr><tr><td id="d469907e270">

**Delete**

</td><td>

Delete this event profile and the Splunk Event Profiles list is displayed.

</td></tr></tbody>
</table>
## What to do next

You have successfully selected an alert for a scheduled alert profile. The next step is map alert values to fields on a security incident.

**Parent Topic:**[Create and name an event profile](splunk-event-ingest-create-profile.md)

