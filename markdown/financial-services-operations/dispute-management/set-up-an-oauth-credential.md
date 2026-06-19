---
title: Set up an OAuth Credential
description: Create an OAuth 2.0 credential to enable secure authentication for Card Data Security integrations. This credential uses an existing OAuth Provider to establish authenticated connections with external systems.
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

# Set up an OAuth Credential

Create an OAuth 2.0 credential to enable secure authentication for Card Data Security integrations. This credential uses an existing OAuth Provider to establish authenticated connections with external systems.

## Before you begin

Role required: admin

This task requires an OAuth Provider created for Card Data Security. See [Set up an OAuth Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-provider.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

3.  Select **OAuth 2.0 Credentials**.

4.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the OAuth 2.0 credential&gt;|
    |**OAuth Entity Profile**|&lt;The default profile from the OAuth Provider created for Card Data Security&gt;|

5.  Select **Submit**.


## Result

The OAuth credential record is created.

## What to do next

[Set up the OAuth Vault API REST message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-the-vault-api-rest-message.md).

