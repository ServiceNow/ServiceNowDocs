---
title: Ingest sample Microsoft Graph Security API alerts
description: Ingest sample alerts from your Microsoft Azure tenant.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Map alert fields, Create a profile, Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Ingest sample Microsoft Graph Security API alerts

Ingest sample alerts from your Microsoft Azure tenant.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  You can either pull the 5 most recent sample alerts or provide the unique alert IDs for the specific alerts that you want to use for your mapping experience.

    From the **Ingestion Preference** choice list, select one of the following:

    -   Retrieve most recent alerts: The 5 most recent alerts are retrieved.
    -   Select alerts based on alerts ID: Specify the alert ID for the alerts to be retrieved. You can specify a maximum of 5 alert ids separated by commas.
2.  Click **Fetch Sample Data** to pull the latest sample alert data from the Microsoft Azure tenant.

    The pull for sample alerts may take a few moments.

    The sample alert field values are populated on the left side of the form when sample alerts are ingested by the profile. These are the alerts that you map to the SIR security incident fields. The alert fields and values results are displayed as individual tabs.

    ![Microsoft Graph Security API: ingest alerts](../image/ms-graph-create-profile-2.png)


## What to do next

After you have fetched the sample data, the next step is map the alert fields to the security incident.

