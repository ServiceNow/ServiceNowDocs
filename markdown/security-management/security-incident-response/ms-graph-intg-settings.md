---
title: Microsoft Graph Security API integration configuration settings
description: Use this option to modify the Microsoft Graph Security API ingestion integration default system properties.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Microsoft Graph Security API integration configuration settings

Use this option to modify the Microsoft Graph Security API ingestion integration default system properties.

## Before you begin

Role required: sn\_si.admin

## About this task

Modify the default configuration properties to limit the number of security incidents that can be created during a 24 hour period or the number of alerts that can be aggregated in one security incident.

To modify the system properties, log in as a user with the `sn_si.admin` role and navigate to **Microsoft Graph Security API Integration** &gt; **Microsoft Graph Security API Integration Settings**.

The default configuration settings are displayed. You can modify these settings if required.

![Microsoft Graph Security API: Integration Settings](../image/ms-graph-intg-settings.png)

Any modified integration settings will be applied during the next polling interval as defined in the profile.

