---
title: Create a multi-record, custom field Splunk alert
description: To create a multiple record Splunk alert with custom fields, you must build a search that is designed to match the ServiceNow columns you want to populate.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Multiple-record, custom field Splunk alerts, ServiceNow Security Operations add-on for Splunk overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a multi-record, custom field Splunk alert

To create a multiple record Splunk alert with custom fields, you must build a search that is designed to match the ServiceNow columns you want to populate.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **Search**.

2.  In the **Search** box, create a search that generates your record data.

    See the [examples](../reference/multi-record-examples.md) for recommended search criteria.

3.  Click **Save As** and select **Alert**.

4.  Set the name, permissions, and schedule, as needed.

5.  Click **Add Actions**.

6.  Make one of the following selections.

    -   To create one event per result from your search, select **Create Multiple ServiceNow Security Events**.
    -   To create one incident per result from your search, select **Create Multiple ServiceNow Security Incidents**.
7.  Set any defaults, as needed.

    If the field in the search result is blank or not present, the defaults are used. If there is a value in the result, the defaults are overwritten.


