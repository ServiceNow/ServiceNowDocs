---
title: Set up a credential
description: Create a credential to enable secure authentication for Card Data Security integrations. This credential authenticates your ServiceNow instance with the tokenizer service gateway.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/set-up-an-oauth-credential.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [set up oauth credential, oauth 2.0 credentials, create oauth credential, integration hub credentials, oauth entity profile, card data security oauth credential, authenticated connections]
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up a credential

Create a credential to enable secure authentication for Card Data Security integrations. This credential authenticates your ServiceNow instance with the tokenizer service gateway.

## Before you begin

Role required: admin

For card network integrations \(Visa, Mastercard\), this task requires an OAuth Provider created for Card Data Security. See [Set up an OAuth Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-provider.md) for more information.

For Verifi integration, this task requires the unique API key provided by the tokenizer service during connection setup.

## Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

3.  Select the credential type.

    -   For card network integration, select **OAuth 2.0 Credentials**.
    -   For Verifi integration, select **API Key Credentials**.
4.  For card network integration, enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the OAuth 2.0 credential&gt;|
    |**OAuth Entity Profile**|&lt;The default profile from the OAuth Provider created for Card Data Security&gt;|

    For Verifi integration, enter the following field values.

    |Field|Value|
    |-----|-----|
    |**API Key**|&lt;The unique API key provided by the tokenizer service during connection setup&gt;|

5.  Select **Submit**.


## Result

The credential record is created.

## What to do next

For Verifi integration, see .

For card network integration, see [Set up the API REST message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-the-vault-api-rest-message.md).

