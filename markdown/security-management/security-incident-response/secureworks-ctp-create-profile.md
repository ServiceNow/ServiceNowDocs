---
title: Create a profile for Secureworks CTP ticket ingestion integration
description: Create a profile in your ServiceNow AI Platform instance and determine which tickets need to be ingested and which tickets will be used to create security incidents. Before security incidents are created from ingested tickets, the field values from tickets are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be displayed.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Secureworks CTP Ticket Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a profile for Secureworks CTP ticket ingestion integration

Create a profile in your ServiceNow AI Platform instance and determine which tickets need to be ingested and which tickets will be used to create security incidents. Before security incidents are created from ingested tickets, the field values from tickets are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be displayed.

The integration allows you to ingest tickets based on the profiles that you configure in the Security Operations environment of your instance. All tickets are initially ingested for a configured ticket type in a profile. Ingested tickets can then be further filtered to specify which tickets create security incidents.

For example, you may prefer filters that create security incidents only for tickets that are identified as high-risk. Before a profile is activated, and it creates security incidents from ingested tickets, individual field values on the tickets are mapped to corresponding fields on a layout of security incident for a preview.

