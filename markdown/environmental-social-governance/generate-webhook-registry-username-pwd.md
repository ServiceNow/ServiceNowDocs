---
title: Generate webhook registry username and password
description: Generate a user name and password in your ServiceNow instance to authenticate webhook requests and retrieve the required metric data from the Workday application.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management \(formerly ESG\) with Workday, Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Generate webhook registry username and password

Generate a user name and password in your ServiceNow instance to authenticate webhook requests and retrieve the required metric data from the Workday application.

## Before you begin

Role required: sn\_esg.admin

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Integration with Workday** &gt; **Webhook Registry**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the webhook.|
    |Workday instance URL|Workday host URL and tenant name. This URL will be provided by your Workday administrator.|
    |Username|Username that will be generated. This field is automatically set after you generate the username and password.|
    |Password|Password that will be generated to log in to the Workday instance. This field is automatically set after you generate the username and password.|
    |Domain|Domain in which the registry is being created. Select **global** in this field.|

4.  Right-click the form header and select **Save**.

5.  Select **Generate username and password**.

    Copy and record the values of username and password. These values must be specified in the Workday instance to authenticate the webhook requests.


