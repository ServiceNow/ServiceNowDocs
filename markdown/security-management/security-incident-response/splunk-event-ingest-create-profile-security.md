---
title: Create and name an event profile for the Splunk Enterprise Security event ingestion integration
description: You create an event profile in your ServiceNow AI Platform instance and determine which Splunk notable events create security incidents.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create and name an event profile for the Splunk Enterprise Security event ingestion integration

You create an event profile in your ServiceNow AI Platform instance and determine which Splunk notable events create security incidents.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

Before ServiceNow AI Platform Security Incident Response \(SIR\) security incidents are created from ingested notable events, the field values from alerts are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be created.

From an integration perspective using the available APIs, Splunk ES notable events are forwarded individually and manually as discrete notable events, or they’re automatically ingested into the Security Operations environment of your ServiceNow AI Platform instance depending on the profile type defined.

The integration workflows ingest different types of notable events such as unauthorized access attempts and malware, for example. These notable events are ingested based on the profiles that you configure in the Security Operations environment of your instance.

All notables are initially ingested for a configured correlation search type in a profile. Ingested notables can then be further filtered to specify which notables create security incidents. For example, you may prefer filters that create security incidents only for notable events that are identified as high-risk. Before a profile is activated, and it creates security incidents from ingested notable events, individual field values on the notable events are mapped to corresponding fields on a layout the security incident for a preview.

## Procedure

1.  Names for the event profiles in your ServiceNow AI Platform instance must be unique and can only be mapped to one active event profile at any given time.

2.  The ServiceNow AI Platform ingests specific notables using the workflows of the integration.

    All notable events that meet the selection criteria in your Splunk ES console are initially ingested into your ServiceNow AI Platform instance.

3.  A profile in your ServiceNow AI Platform is an encapsulation of a notable event in your Splunk ES console.

    There’s a one-to-one relationship between notable events that are ingested with a profile and connections to your Splunk ES console: one notable event type for one connection.

4.  To create profiles for scheduled notable events, see [Set up a profile for scheduled notable event ingestion](../concept/splunk-event-scheduled-security.md).

5.  To create profiles for manual event forwarding, see [Set up a profile for manual event forwarding](../concept/splunk-event-manual-security.md).


