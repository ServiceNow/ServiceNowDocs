---
title: Configure a CORS rule for Engagement Messenger
description: Configure a cross-origin resource sharing \(CORS\) rule to enable cross-domain requests between Engagement Messenger and your website where you want to deploy the messenger.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up Engagement Messenger, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Configure a CORS rule for Engagement Messenger

Configure a cross-origin resource sharing \(CORS\) rule to enable cross-domain requests between Engagement Messenger and your website where you want to deploy the messenger.

## Before you begin

Role required: admin

You must complete the following tasks:

-   [Configure Engagement Messenger](create-engagement-messenger-module.md).
-   [Create an identity provider \(IdP\) for Engagement Messenger](../concept/create-identity-providers-for-engagement-messenger.md).

## About this task

Use the Engagement Messenger API and your website URL to create a CORS rule.

## Procedure

1.  Navigate to **All** &gt; **Engagement Messenger** &gt; **Administration** &gt; **CORS Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ykv_fcs_f4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the CORS rule.

</td></tr><tr><td>

Application

</td><td>

Application scope for this record.

</td></tr><tr><td>

REST API

</td><td>

Engagement Messenger REST API that this CORS rule applies to.

 Set this field to **Engagement Center API \[sn\_csm\_ec/engagement\_center\_api\]**.

</td></tr><tr><td>

Domain

</td><td>

Domain that sends the request to this REST API. Set this field value to the URL of the website where you want to deploy the messenger.

 For example, **https://www.example.com**.

</td></tr><tr><td>

Max age

</td><td>

Number of seconds to cache the client session. After an initial CORS request, further requests from the same client within this time do not require a preflight message.

 If you do not specify a value, the default value of 0 indicates that all requests require a preflight message.

</td></tr><tr><td>

HTTP Methods

</td><td>

Allowed HTTP methods. Enable the GET and POST methods.

</td></tr><tr><td>

HTTP Headers

</td><td>

Comma-separated list of HTTP headers to send in the response. You can leave this field empty.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

[Create HTTP response headers for Engagement Messenger](create-http-response-headers-for-ec.md).

