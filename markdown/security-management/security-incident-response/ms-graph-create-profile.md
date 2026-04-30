---
title: Create a profile for the Microsoft Graph Security API alert ingestion integration
description: As a user with the sn\_si.admin role, you create an alert profile in your ServiceNow AI Platform instance and determine which alerts create security incidents. Before security incidents are created from ingested alerts, the field values from alerts are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be displayed.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a profile for the Microsoft Graph Security API alert ingestion integration

As a user with the sn\_si.admin role, you create an alert profile in your ServiceNow AI Platform instance and determine which alerts create security incidents. Before security incidents are created from ingested alerts, the field values from alerts are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be displayed.

## Before you begin

Role required: sn\_si.admin

## About this task

The integration allows you to ingest different types of alerts such as unauthorized access attempts and malware, for example. These alerts are ingested based on the profiles that you configure in the Security Operations environment of your instance. All alerts are initially ingested for a configured alert type in a profile. Ingested alerts can then be further filtered to specify which alerts create security incidents.

For example, you may prefer filters that create security incidents only for alerts that are identified as high-risk. Before a profile is activated, and it creates security incidents from ingested alerts, individual field values on the filtered alerts are mapped to corresponding fields on a layout of security incident for a preview. All alerts that meet the selection criteria in your Microsoft Azure tenant and are available over the Microsoft Graph Security API are initially ingested into your ServiceNow AI Platform instance.

