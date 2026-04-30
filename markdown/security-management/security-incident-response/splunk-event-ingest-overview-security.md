---
title: Splunk Enterprise Security event ingestion integration
description: The Splunk Enterprise Security notable event ingestion integration with the Security Incident Response \(SIR\) product allows security incident analysts to collect and process notable event data \(referred to as notables\).
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Splunk Enterprise Security event ingestion integration

The Splunk Enterprise Security notable event ingestion integration with the Security Incident Response \(SIR\) product allows security incident analysts to collect and process notable event data \(referred to as notables\).

## Overview of Splunk Enterprise Security event ingestion integration

Data is ingested continually based on a configured polling schedule and it is used by analysts to identify and respond to potential cyber threats. Security events that are collected can be correlated into notable events in Splunk Enterprise Security and then ingested automatically with this integration. Also, individual notable events can be manually forwarded on-demand from the Splunk Enterprise Security Incident Review console and reporting interface into the Security Incident Response product of the ServiceNow AI Platform to create security incidents.

This integration provides a security operations center \(SOC\) analyst with visibility to notable events and related contributing event data. This data can be integrated into ServiceNow AI Platform Security Incident Response \(SIR\) security incidents for further investigation and remediation. Profiles are created in your ServiceNow AI Platform instance to handle different notable event types that are created via correlation searches in Splunk Enterprise Security. These profiles customize how different Splunk event fields are displayed on SIR security incidents.

## Key features

This integration includes the following key features:

-   Create multiple notable event ingestion profiles to create SIR security incidents for specific types of threats such as phishing and malware and unauthorized access attempts.
-   Create multiple event profiles for on-demand event forwarding from your Splunk ES incident review console to create SIR security incidents.
-   Drag-and-drop mapping of Splunk notable event field values to associated SIR security incident fields.
-   A preview of the SIR security incident layout based on sample notable events to validate event mapping details.
-   Ingest historical notable events as well as ongoing, new, and updated notable events on configurable intervals.
-   Filter out notable events that do not meet SIR incident generation criteria, for example, low priority events, events that have yet to achieve a specific status, and so on.
-   Aggregate events or alerts to existing SIR security incidents based on matching field values to avoid duplicate security incidents.
-   Update notable events based on SIR incident creation and/or closure conditionals via a bi-directional interface to keep Splunk ES notable event updates in sync with the ServiceNow SIR incident status.

## Supported ServiceNow AI Platform versions

The com.snc.si\_dep plugin is required for this integration. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before installing and activating the other Security Operations applications.

The following Security Operations applications must be installed and activated from the ServiceNow Store. Install and then activate one application at a time in the order listed below to ensure a smooth installation:

1.  Security Integration Framework
2.  Security Support Common
3.  Security Incident Response

For more information about installing the Security Operations core applications, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

## ServiceNow Addons

The ServiceNow Security Operations Event Ingestion Addon for Splunk ES is required only if you prefer to forward events manually from your Splunk Enterprise Security Incident Review console into your ServiceNow AI Platform instance. This ServiceNow addon is available in [splunkbase](https://splunkbase.splunk.com/).

This ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise application in splunkbase is not required for the automated alert ingestion that is supported by the integration.

## Splunk Supported versions

This integration has been tested with:

-   Splunk Enterprise version 10.0.0 and earlier.
-   Splunk Enterprise Security application version 8.3.0 and earlier.

## MID Server

This integration requires an installed and configured MID Server in your ServiceNow AI Platform® instance to connect to the Splunk service when the Splunk server is deployed within your corporate network. If you are using the Splunk Cloud service, a MID Server is not required. See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information about MID Servers.

## References

<table id="table_axk_n23_2gb"><thead><tr><th>

Reference

</th><th>

Document Identifier

</th><th>

Document Title

</th></tr></thead><tbody><tr><td>

1

</td><td>

Splunk product website

</td><td>

[Splunk Enterprise Security product website](https://www.splunk.com/en_us/software/enterprise-security.html).

</td></tr></tbody>
</table>## Checklist

For a printable checklist of these topics, see [Checklist for Splunk Enterprise Security Notable Event Ingestion integration](../task/splunk-event-ingest-checklist-security.md). You can use this list to monitor your progress as you work through the tasks of the integration.

