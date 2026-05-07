---
title: Save searches in your Splunk Enterprise console for the Splunk Enterprise Event Ingestion integration
description: The following steps for saving searches in your Splunk Enterprise console are provided for a user with the Splunk Enterprise administrator role.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration architecture and external systems connection, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Save searches in your Splunk Enterprise console for the Splunk Enterprise Event Ingestion integration

The following steps for saving searches in your Splunk Enterprise console are provided for a user with the Splunk Enterprise administrator role.

## Before you begin

If you already have existing saved searches and triggered alerts in your Splunk Enterprise console, you are not required to modify these searches for this integration.

The integration of the ServiceNow AI Platform® Security Operations product with the Splunk event notification service pulls event and alert information from Splunk.

Prior to ingesting alerts into your Security Operations environment, configure searches in your Splunk Enterprise console so that you automatically pull the relevant security events in Splunk Enterprise that you want to save as alerts.

If you do not have saved searches and triggered alerts established for notification when important security events occur in your Splunk Enterprise console, follow these steps to save searches.

Role required: Splunk Enterprise administrator

## Procedure

1.  Log in to your Splunk Enterprise account.

2.  Click the **Search** tab.

3.  In the New Search field that is displayed, enter a value for the alert, for example, Malware.

4.  To view the events related to your search, to the right of the New Search field, click the search icon or press enter.

    The search results with events are displayed.

5.  To save the search as an alert, in the upper right of the page, expand the Save As choice list and select **Alert**.

6.  In the form that is displayed, fill in the fields.

<table id="choicetable_zvm_5cv_3fb"><thead><tr><th align="left" id="d328863e158">

Field

</th><th align="left" id="d328863e161">

Description

</th></tr></thead><tbody><tr><td id="d328863e167">

**Title**

</td><td>

Descriptive name for the alert, for example, Malware Events. After you save this search as an alert, events from a fired alert in the Splunk service are automatically processed into triggered alerts using this search data. This triggered alert title is used in the event profile that you create in your ServiceNow AI Platform instance to identify which events are ingested into your instance for ServiceNow AI Platform® Security Incident Response SIR security incident creation.

</td></tr><tr><td id="d328863e193">

**\(Optional\) Description**

</td><td>

Text to help you distinguish this alert from other alerts.

</td></tr><tr><td id="d328863e202">

**Alert type**

</td><td>

In the fields that are displayed, select **Scheduled** to search for this alert on a schedule, or **Real-time** to search continuously for this alert.

</td></tr><tr><td id="d328863e217">

**Trigger results**

</td><td>

You may prefer to set one of the following filter conditions:-   Number of Results is greater than or less than
-   One-time \(once\) for each result


</td></tr><tr><td id="d328863e236">

**Trigger actions**

</td><td>

Add actions to trigger this alert. Expand the Add choice list and click **Add to Triggered Alerts** so that it is displayed on the form. You may prefer this setting for the alerts that you ingest into your ServiceNow AI Platform instance.

</td></tr></tbody>
</table>7.  Click **Save**.

    Your alert is saved, and it is displayed under the Alerts tab on the Search page.

    The Splunk service pulls in the events by matching the criteria that you configured in the alert. It caches the events, and you then request these events from your profiles that you set up in your ServiceNow AI Platform instance. Because the ingestion pull of events occurs from a cache in the Splunk service, this ingestion from your ServiceNow AI Platform does not impact performance on your Splunk platform.


## What to do next

You have successfully completed the required setup for the integration in your Splunk Enterprise console. If you have not already installed the application for the integration from the ServiceNow Store, the next step is to install the application for the integration and configure it.

**Parent Topic:**[Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration](../concept/splunk-event-ingest-integration-architecture.md)

