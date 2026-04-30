---
title: Setup IBM QRadar profile
description: As a user with the sn\_si.admin role, you create an offense profile in your ServiceNow AI Platform instance and determine which offenses create security incidents. Before ServiceNow AI Platform Security Incident Response \(SIR\) security incidents are created from offenses, the field values from offenses are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be created.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up instance, IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Setup IBM QRadar profile

As a user with the sn\_si.admin role, you create an offense profile in your ServiceNow AI Platform instance and determine which offenses create security incidents. Before ServiceNow AI Platform Security Incident Response \(SIR\) security incidents are created from offenses, the field values from offenses are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be created.

## Before you begin

Role required: sn\_si.admin

## About this task

From an integration perspective using available APIs, IBM QRadar offenses are automatically ingested into the Security Operations environment of your ServiceNow AI Platform instance depending on the profile type defined. The integration workflows ingest different types of offenses such as unauthorized access attempts and malware, for example. These offenses are ingested based on the profiles that you configure in the Security Operations environment of your instance. All offenses are initially ingested for a configured offense type in a profile. Ingested offenses can then be further filtered to specify which offenses create security incidents. For example, you may prefer filters that create security incidents only for offenses that are identified as high-risk. Before a profile is activated, and it creates security incidents from ingested offenses, individual field values on the offenses are mapped to corresponding fields on a layout of security incident for a preview.

Names for the offense profiles in your ServiceNow AI Platform instance must be unique. You can create multiple configurations for multiple sources and you can also create multiple profiles for a single source.

