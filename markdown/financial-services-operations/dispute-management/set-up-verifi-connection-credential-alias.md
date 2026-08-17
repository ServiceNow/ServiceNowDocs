---
title: Set up the Verifi Connection &amp; Credential Alias
description: For Verifi integrations, set up a dedicated Verifi connection alias for Card Data Security operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/set-up-verifi-connection-credential-alias.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-05-29"
reading_time_minutes: 1
keywords: [Verifi, Card Data Security, Connection and Credential Alias, Integration Hub, OAuth, JWT provider, tokenizer, card dispute resolution, VerifiCardDataSecurity]
audience: administrator
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up the Verifi Connection &amp; Credential Alias

For Verifi integrations, set up a dedicated Verifi connection alias for Card Data Security operations.

## Before you begin

Role required: admin

This step is performed for Verifi integrations. This requires:

-   A Verifi credential created from the procedure in [Set up a credential](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-credential.md).
-   A JWT provider created from the procedure in [Set up a JWT Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-provider.md).

See [Set up Verifi integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-oauth-for-card-data-security.md) for a list of other required values.

## Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select the **VerifiCardDataSecurity** record.

3.  In the Connections related list, select **New**.

4.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Credential**|&lt;The credential created from the procedure in [Set up a credential](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-credential.md)&gt;|
    |**Connection URL**|&lt;The tokenizer service endpoint URL&gt;|
    |**Issuer**|&lt;The Issuer ID provided by Verifi&gt;|
    |**JWT Provider**|&lt;The JWT Provider created from the procedure in [Set up a JWT Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-provider.md)&gt;|
    |**API Version**|&lt;The API version provided by Verifi, as necessary&gt;|

5.  Select **Submit**.


## Result

The **VerifiCardDataSecurity** record is set up with a dedicated connection alias for Card Data Security.

## What to do next

[Set up the API REST message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-the-vault-api-rest-message.md).

