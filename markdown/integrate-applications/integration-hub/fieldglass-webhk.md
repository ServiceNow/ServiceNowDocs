---
title: Set up webhook for the SAP Fieldglass spoke
description: Retrieve the required information from SAP Fieldglass instance to your ServiceNow instance by setting up webhook to authenticate the requests.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SAP Fieldglass Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up webhook for the SAP Fieldglass spoke

Retrieve the required information from SAP Fieldglass instance to your ServiceNow instance by setting up webhook to authenticate the requests.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **SAP Fieldglass Spoke** &gt; **SAP Fieldglass Webhook Registries**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |SAP Fieldglass Event|Event for which you want to set up the webhook. For example, `Create job posting`.|
    |User name|Leave this field empty.|
    |Password|Leave this field empty.|
    |SAP Fieldglass Instance|URL of your SAP Fieldglass instance.|

4.  Click **Generate UserName and Password**.

    **User name** and **Password** are displayed.

5.  Copy and record the values.

6.  Share information with the appropriate teams.

    -   Contact the SAP Fieldglass team to configure the webhook endpoint.
    -   Share the user name and password combination with the SAP Fieldglass team.

