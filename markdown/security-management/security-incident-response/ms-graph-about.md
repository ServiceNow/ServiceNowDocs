---
title: Microsoft Graph Security API alert ingestion integration
description: Use the Microsoft Graph Security API integration to ingest alerts from Microsoft Graph security providers and automatically create security incidents.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Microsoft Graph Security API alert ingestion integration

Use the Microsoft Graph Security API integration to ingest alerts from Microsoft Graph security providers and automatically create security incidents.

## Overview

The Microsoft Graph Security API is an intermediary service \(or broker\) that provides a single programmatic interface for connecting multiple security providers \(Native to Microsoft as well as ServiceNow Partners\).

The Microsoft Graph Security API integration addresses these issues by using the Microsoft Graph Security API to connect with different Microsoft security technologies like Azure Sentinel, Microsoft Defender Advanced Threat Protection, and Azure Advanced Threat Protection. Alerts from Microsoft Security providers are ingested and security incidents are automatically created in Security Incident Response.

## Key features

This integration includes the following key features:

-   Discovery of Microsoft Graph Security API alerts that are candidates for security incidents and automate the creation of security incidents.
-   Mapping of alert fields to security incident fields.
-   Aggregation of similar alerts to existing open security incidents instead of creating duplicate security incidents.
-   Preview alert field values and validate their mappings in the security incident.
-   Automatic alert status update for security incident creation and closure.
-   Set up scheduled ingestion of alerts to create security incidents periodically.

