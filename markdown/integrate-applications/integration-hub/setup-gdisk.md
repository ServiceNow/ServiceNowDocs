---
title: Set up the Google Persistent Disk spoke
description: Integrate the ServiceNow instance and Google Persistent Disk spoke by using G Suite credentials to authenticate ServiceNow requests.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Google Persistent Disk Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Google Persistent Disk spoke

Integrate the ServiceNow instance and Google Persistent Disk spoke by using G Suite credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Persistent Disk spoke.
-   Activate and set up the [Google Compute Engine Spoke](../concept/gcomengine-spoke.md).
-   Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Open record for the Google Compute Engine spoke. For example, `Google Compute Cred`.

3.  For **Credential alias**, select the Connection and Credential alias record of the Google Persistent Disk spoke.

4.  Right-click the form header and click **Save**.

5.  Click **Get Oauth Token**.


