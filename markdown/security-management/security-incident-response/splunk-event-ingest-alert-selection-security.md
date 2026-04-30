---
title: Set Correlation rules
description: After you have created a profile for a scheduled notable event type ingestion, select a Splunk Enterprise Security correlation rule name for this profile for which you want to map corresponding notable events to a ServiceNow AI Platform Security Incident Response security incident.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up a profile for scheduled notable event ingestion, Create an event profile, Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set Correlation rules

After you have created a profile for a scheduled notable event type ingestion, select a Splunk Enterprise Security correlation rule name for this profile for which you want to map corresponding notable events to a ServiceNow AI Platform Security Incident Response security incident.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

View the available correlation rules in your ServiceNow AI Platform instance so you know the notable event types for which you want to ingest and create security incidents. Select a correlation rule. You can select one or more notable event from the list in this form.

## Procedure

1.  If you're not continuing from the previous section of the incident profile definition process, access the profile you're defining.

    1.  Navigate to **All**&gt;**Splunk ES Event Profile**.
    2.  Select the profile you're continuing to define.
    3.  Select **Notable Event Selection** in the progress bar.
2.  Clear **All Correlation Rules Selected** check box to select specific Correlation Rules.

    Selecting this check box will retrieve latest Correlation Rules from Splunk ES for active profile.

3.  In the **Correlation Rules List** search field, enter the Correlation Rule name created in the Splunk ES portal.

4.  Select the Correlation Rule\(s\).

5.  Use the **right arrow \( &gt;\)** to move the rule\(s\) from **Available** to **Selected** column.

    **Note:** Correlation rules must be unique across active profiles. A correlation rule associated with an active profile cannot be selected for another active profile. To reuse the rule, deactivate the profile it is currently associated with.

    ![Splunk ES Event Profile: Select Notable Event](../image/new-images/splunk_es_profile_select.png)

6.  Select **Continue**.


## What to do next

[Map notable events](splunk-event-ingest-map-alerts-security.md)

