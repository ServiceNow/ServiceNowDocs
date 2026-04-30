---
title: Provide Signing Key in ServiceNow instance
description: Provide Slack app details and Signing Key in your ServiceNow instance for authenticating requests from ServiceNow.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up Slack spoke, Slack Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Provide Signing Key in ServiceNow instance

Provide Slack app details and Signing Key in your ServiceNow instance for authenticating requests from ServiceNow.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Slack** &gt; **Slack Configurations**.

2.  Open the default record.

    You can also create new record to provide other signing keys.

3.  On the form, fill these values.

<table id="table_nwj_mdh_3mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Slack App

</td><td>

Name of your Slack app.**Note:** This name should same as the app name provided while creating the Slack app.

</td></tr><tr><td>

Connection Alias

</td><td>

Connection alias associated with the selected app in the **Connections** tab.

</td></tr><tr><td>

Property Name

</td><td>

Name of the Slack configuration. Enter `Signing Secret`.

</td></tr><tr><td>

Signing Secret

</td><td>

Signing Secret of your Slack app.

</td></tr></tbody>
</table>4.  Click **Update**.


