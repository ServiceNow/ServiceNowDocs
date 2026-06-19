---
title: Set up the OAuth Vault API REST message
description: Configure the Data Security Vault API REST message with the correct endpoint URL and OAuth authentication profile. This setup enables secure communication between ServiceNow and the tokenizer service for Card Data Security.
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

# Set up the OAuth Vault API REST message

Configure the Data Security Vault API REST message with the correct endpoint URL and OAuth authentication profile. This setup enables secure communication between ServiceNow and the tokenizer service for Card Data Security.

## Before you begin

Role required: admin

This task requires an OAuth Provider created for Card Data Security. See [Set up an OAuth Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-provider.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message**.

2.  Select the record **Data Security Vault API**.

3.  In the **Endpoint** field, update the value to the `tokenURI` value from the credentials JSON file.

4.  In **Authentication**, enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Authentication type**|OAuth 2.0|
    |**OAuth profile**|&lt;The default profile from the OAuth Provider created for Card Data Security&gt;|


## Result

The Data Security Vault API record is updated with the correct URL and OAuth profile.

