---
title: Using ServiceNow Event Ingestion Integration add-on
description: Map alerts from Splunk console to create a Security Incident Response \(SIR\) on the ServiceNow instance.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-10-10"
reading_time_minutes: 1
breadcrumb: [Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Using ServiceNow Event Ingestion Integration add-on

Map alerts from Splunk console to create a Security Incident Response \(SIR\) on the ServiceNow instance.

## Before you begin

Role required: sn\_sec\_splunk\_v2.api\_account\_access

## Procedure

1.  Log in to [Splunk Enterprise](https://splunk.secops-eng.com:8000/en-GB/app/launcher/home).

2.  Navigate to **Apps** &gt; **Search &amp; Reporting**.

3.  Select **Alerts**.

    A list of alerts generated in the Splunk console on the basis of correlation rule configured previously show up.

4.  Select any **Configured Alert** from the list.

    Trigger History of the configured alert show up.

5.  Select **View Results** against the alert.

6.  Expand any of the alerts using **\(&gt;\)** icon.

7.  From the drop down, select the **Workflow action label** configured while setting up the add-on.

    For more information on Workflow action label, see [Set up ServiceNow Event Ingestion Integration add-on](splunk-event-ingest-setup-prereqs.md)

    Alerts will go in **Splunk Import** table followed by **Splunk Event to Tasks** table.


## Result

A Security Incident Response \(SIR\) record is created on the ServiceNow instance as per the mapping specified in the Manual event forwarding profile. For instructions on how to set up a Manual event forwarding profile, see [Create and name an event profile for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-create-profile.md)

**Parent Topic:**[Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration](../concept/splunk-event-ingest-integration-architecture.md)

