---
title: Set up the API REST message
description: Configure the API REST message for your integration. This step points outbound REST messages to the correct tokenizer service endpoint.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/set-up-the-vault-api-rest-message.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [set up oauth vault api rest message, data security vault api, rest message oauth, tokenuri endpoint, oauth 2.0 authentication, oauth profile, data security rest message, vault api rest message configuration]
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up the API REST message

Configure the API REST message for your integration. This step points outbound REST messages to the correct tokenizer service endpoint.

## Before you begin

Role required: admin

For card network integration, this task requires an OAuth Provider created for Card Data Security. See [Set up an OAuth Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-provider.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message**.

2.  Select the REST Message record.

    -   For card network integration, select **Data Security Vault API**
    -   For Verifi integration, select **Verifi**.
3.  In the **Endpoint** field, update the value.

    -   For card network integration, enter the `tokenURI` value from the credentials JSON file.
    -   For Verifi integration, enter the tokenizer connection URL configured to route Verifi API calls.
4.  For card network integration, in **Authentication**, enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Authentication type**|OAuth 2.0|
    |**OAuth profile**|&lt;The default profile from the OAuth Provider created for Card Data Security&gt;|


## Result

The REST Message record is updated with the correct URL and OAuth profile.

