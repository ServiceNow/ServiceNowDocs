---
title: Set up the Google Cloud Virtual Network spoke
description: Integrate the ServiceNow instance and Google Cloud Virtual Network spoke by using OAuth 2.0 credentials to authenticate ServiceNow requests.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Google Cloud Virtual Network Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Google Cloud Virtual Network spoke

Integrate the ServiceNow instance and Google Cloud Virtual Network spoke by using OAuth 2.0 credentials to authenticate ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription.
-   Activate and set up the [Google Compute Engine Spoke](../concept/gcomengine-spoke.md).
-   Activate the Google Cloud Virtual Network spoke.
-   Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Open the record for the Google Compute Engine spoke, for example, `Google Compute Cred`.

3.  For **Credential alias**, select the Connection and Credential alias record of the Google Cloud Virtual Network spoke.

4.  Right-click the form header and click **Save**.

5.  Click **Get OAuth Token**.


