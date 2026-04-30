---
title: Set up trusted media domains for secure file upload
description: Virtual Agent uses trusted media domains to check the URLs of attachment files before uploading them. If a URL is not from a trusted domain, Virtual Agent will not upload the attachment.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Supported Virtual Agent and Agent Chat features for custom chat integrations, Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up trusted media domains for secure file upload

Virtual Agent uses trusted media domains to check the URLs of attachment files before uploading them. If a URL is not from a trusted domain, Virtual Agent will not upload the attachment.

## Before you begin

Role required: admin

## About this task

For custom chat integrations, specify trusted media domains in either the Provider \[sys\_cs\_provider\] table or the Provider Channel Identity \[sys\_cs\_provider\_application\] table. The trusted media domain values in the Provider Channel Identity table override the corresponding values in the Provider table.

Pre-built integrations, such as Slack, Microsoft Teams, and Workplace from Facebook, have default trusted media domain values set at the provider level, in the Provider \[sys\_cs\_provider\] table. To change the default trusted values, specify the different trusted media domains in the Provider Channel Identity \[sys\_cs\_provider\_application\] table.

## Procedure

1.  Navigate to **All** &gt; **sys\_cs\_provider\_application.list** &gt; **Provider Channel Identity** and click **New**.

2.  On the form, fill in the fields.

<table id="table_xsb_sy5_tnb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the channel identity. For example: `VA SMS Twilio Adapter`

</td></tr><tr><td>

Provider

</td><td>

Select the name of your provider application that you set up previously. For example: `VA SMS Twilio Adapter Pro`.

</td></tr><tr><td>

Message auth

</td><td>

Message authentication for the channel identifier.

</td></tr><tr><td>

Inbound ID

</td><td>

Identifier for your bot. For example, the phone number.

</td></tr><tr><td>

Trusted media domains

</td><td>

Comma-separated list of one or more trusted domains for the provider. For example: `twilio.com`, `slack.com`

**Note:** Subdomains under a trusted domain are also trusted. You do not need to specify subdomains in this list.

 If this field is not visible, you can [configure the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) to show it.

 For security reasons, Virtual Agent checks that the URLs for attachments in conversations are from trusted domains specified here. If the URL is not for a trusted domain, Virtual Agent doesn't upload the attachment.

 If an attachment upload fails because Virtual Agent didn't trust the domain, Virtual Agent does not inform the end user why the attachment upload failed.

 **Note:** For Trusted Domains In custom chat integrations, the values specified in the Trusted media domains field of the Provider Channel Identities table \[sys\_cs\_provider\_application\] takes precedence over the Connections table \[sys\_cs\_provider\] and hence overrides.

</td></tr><tr><td>

Short description

</td><td>

Description for your channel identifier.

</td></tr></tbody>
</table>3.  Click **Submit**.

4.  Create additional channel identifiers using the same procedure.


**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

