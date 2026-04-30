---
title: Create a profile for ArcSight ESM correlation event ingestion integration
description: As a user with the sn\_si.admin role, you create a profile in your ServiceNow AI Platform instance and determine which correlation events create security incidents. Before ServiceNow AI Platform Security Incident Response \(SIR\) security incidents are created from correlation events, the field values from events are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be created.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up your ServiceNow AI Platform instance for the ArcSight ESM event ingestion integration, ArcSight ESM Event Ingestion for Security Operations integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a profile for ArcSight ESM correlation event ingestion integration

As a user with the sn\_si.admin role, you create a profile in your ServiceNow AI Platform instance and determine which correlation events create security incidents. Before ServiceNow AI Platform Security Incident Response \(SIR\) security incidents are created from correlation events, the field values from events are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be created.

## Before you begin

Role required: sn\_si.admin

## About this task

Correlation events are automatically ingested into the Security Operations environment of your ServiceNow AI Platform instance depending on the profile type defined. A profile is an encapsulation of one type of correlation event like unauthorized access attempts or malware.

After a correlation event has been ingested, you can map individual correlation event fields to corresponding fields in the security incident. You can filter correlation events to specify which events create security incidents. For example, you may prefer filters that create security incidents only for correlation events identified as high-risk. You can also define additional event aggregation criteria so that incoming duplicate correlation events are aggregated to an open security incident. Finally, you can define an ingestion schedule and activate the profile.

Names for the event profiles in your ServiceNow AI Platform instance must be unique and can only be mapped to one active event profile at any given time.

