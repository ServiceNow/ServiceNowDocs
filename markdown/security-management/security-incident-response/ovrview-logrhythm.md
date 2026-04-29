---
title: LogRhythm Overview
description: The mapping flexibility of this integration provides an analyst with visibility to events and related alarm data that can be integrated into ServiceNow AI Platform security incidents for further investigation and remediation.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# LogRhythm Overview

The mapping flexibility of this integration provides an analyst with visibility to events and related alarm data that can be integrated into ServiceNow AI Platform security incidents for further investigation and remediation.

Alarm profiles are created in your ServiceNow AI Platform instance to customize how different LogRhythm alarm fields are displayed on a ServiceNow AI Platform security incident. A default mapping of alarm fields is provided, which can be edited to meet customer-specific needs.

The following figure is an example of a customer environment. When an event triggers the creation of a security incident in the ServiceNow AI Platform® instance, a request is sent from your ServiceNow AI Platform® instance to pull alarms from the LogRhythm Client Console either through a MID Server or even without it.

The REST API key is used by the ServiceNow AI Platform® to authenticate with the LogRhythm Client Console. This connection allows your ServiceNow AI Platform instance to pull individual LogRhythm alarms based on configured profiles.

The REST API is used to gather message details not accessed by the REST API.

![A customer environment.](../image/logrhythm-integration-flowchart.png "LogRhythm integration")

## Key features

This integration includes the following key features:

-   Flexibility to create multiple alarm profiles for different alarm types such as Phishing and Malware.
-   Drag-and-drop mapping of LogRhythm alarm field values to associated SIR security incident fields.
-   A Preview of the SIR security incident layout based on LogRhythm sample alarms.
-   Ingest historical alarms as well as ongoing future alarms on configurable intervals.
-   Automated LogRhythm alarm closure upon SIR incident closure. A URL to the SIR incident as well as an incident ID is provided for easy reference.

## Supported releases of the ServiceNow AI Platform

This integration is compatible with the Quebec or later releases of the ServiceNow AI Platform®.

## Supported versions of LogRhythm

This integration is compatible with LogRhythm 7.8 or later. The earlier versions aren’t supported due to API limitations.

**Note:** The following topics are numbered. For a smooth installation and to help you verify expected results, follow the topics in the order they’re presented.

1.  [Set up the REST API](../task/drilldown-api-lr.md)  
You use the LogRhythm REST API key to gather additional event details for individual alarm fields. The API key provides details that are unavailable using the LogRhythm REST API.
2.  [Install the plugin and configure LogRhythm](../task/install-and-config-logrhythm.md)  
Before you run the integration on your instance, complete the installation and configuration steps so the application properly integrates with Security Operations on the ServiceNow AI Platform®.
3.  [Creating an alarm profile for LogRhythm](../task/create-alarm-profile-logrhythm.md)  
In an alarm profile that you create and name, you specify which alarms you want to pull from the LogRhythm Client Console. You also define how they are mapped to fields on a ServiceNow AI Platform security incident.
4.  [Additional configurations for the LogRhythm integration](../task/configure-system-and-troubleshooting-properties.md)  
Use the LogRhythm Integration Settings to modify the preset system and troubleshooting properties as per you requirements.
5.  [Troubleshooting the LogRhythm integration](troubleshooting-logrhythm-integration.md)  
Troubleshoot connectivity and alarm ingestion issues.

**Parent Topic:**[Security Incident Response integrations](../../security-incident-response/concept/sir_integrations.md)

