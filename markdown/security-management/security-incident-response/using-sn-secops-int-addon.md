---
title: Using ServiceNow Security Operations Integration add-on
description: Create security events and incidents directly from Splunk alerts after setting up ServiceNow Security Operations Integration add-on.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-10-07"
reading_time_minutes: 1
breadcrumb: [Setup Splunk environment, Splunk integration setup, ServiceNow Security Operations add-on for Splunk overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Using ServiceNow Security Operations Integration add-on

Create security events and incidents directly from Splunk alerts after setting up ServiceNow Security Operations Integration add-on.

## Before you begin

Role required: sn\_si.integration\_user, sn\_si.analyst

## Procedure

1.  Log in to [Splunk Enterprise](https://splunk.secops-eng.com:8000/en-GB/app/launcher/home).

2.  Navigate to **Apps** &gt; **Search &amp; Reporting**.

3.  Enter a keyword in the New Search field.

    A list of events with the keyword show up.

4.  Expand any of the events using **\(&gt;\)** icon.

5.  Select **Event Actions**.

    -   **Create ServiceNow Security Event**: Events are stored in the em\_event table.

        **Note:**

        Install **Event Management** plugin to access the em\_event table.

    -   **Create ServiceNow Security Incident**: Incidents are stored in the sn\_si\_incident table.

        **Note:** The mapping is pre defined as we don't have a profile for this add-on.

    ![Event actions in Splunk enterprise](../image/splunk-event-actions.png)


