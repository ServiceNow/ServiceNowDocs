---
title: Using ServiceNow Security Operations Event Ingestion Add-on for Splunk ES
description: Forward events on-demand from your Splunk Enterprise Security console to create a Security Incident Response \(SIR\) on the ServiceNow instance.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-10-10"
reading_time_minutes: 1
breadcrumb: [Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Using ServiceNow Security Operations Event Ingestion Add-on for Splunk ES

Forward events on-demand from your Splunk Enterprise Security console to create a Security Incident Response \(SIR\) on the ServiceNow instance.

## Before you begin

Role required: sn\_sec\_splunkes.api\_account\_access

## Procedure

1.  Log in to [Splunk Enterprise](https://splunk.secops-eng.com:8000/en-GB/app/launcher/home).

2.  Navigate to **Apps** &gt; **Enterprise Security**.

3.  Select **Mission Control**.

    A list of notable events generated in the Splunk console on the basis of correlation rule configured previously show up.

4.  Select any **Notable Event** from the list.

5.  Select **Ellipsis icon \(⋮\)**.

6.  From the drop down, select the **Workflow action label** configured while setting up the add-on.

    For more information on Workflow action label, see [Setup ServiceNow Security Operations Event Ingestion Addon for Splunk ES](splunk-es-addon.md)

    Events will go in **Splunk ES Event Import** table followed by **Splunk ES Event to Tasks** table.


## Result

A Security Incident Response \(SIR\) record is created on the ServiceNow instance as per the mapping specified in the Manual event forwarding profile. For instructions on how to set up a Manual event forwarding profile, see [Create and name an event profile](splunk-event-ingest-create-profile.md)

