---
title: Set up the Connection &amp; Credential records
description: Configure the Connection &amp; Credential records for Card Data Security. This establishes the primary outbound connection that routes requests from ServiceNow to external APIs via the tokenizer service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/set-up-the-vault-api-connection.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [set up vault api connection, connection credential records, carddatasecurity servicetoken, carddatasecurity clienttoken, carddatasecurity datatokensigner, vault id, connection url, tokenuri, integration hub connections, credential aliases]
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up the Connection &amp; Credential records

Configure the Connection &amp; Credential records for Card Data Security. This establishes the primary outbound connection that routes requests from ServiceNow to external APIs via the tokenizer service.

## Before you begin

Role required: admin

For Verifi integration, this requires a JWT provider created from the procedure in [Set up a JWT Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-provider.md).

## Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select the Connection &amp; Credential Alias record.

    -   For card network integration, select **CardDataSecurity.ServiceToken**.
    -   For Verifi integration, select **Verifi**.
3.  In the Connections related list, select **New**.

4.  For card network integration, enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the HTTP\(s\) connection&gt;|
    |**Connection URL**|&lt;The tokenizer service endpoint URL i.e. the `tokenURI` value from the credentials JSON file&gt;|
    |**vault\_id Attribute**|&lt;The vault ID of the tokenizer service data vault&gt;|

    For Verifi integration, enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the HTTP\(s\) connection&gt;|
    |**Connection URL**|&lt;The tokenizer service endpoint URL designated for accessing Verifi APIs internally&gt;|
    |**Issuer**|&lt;The Issuer ID provided by Verifi&gt;|
    |**JWT Provider**|&lt;The JWT Provider created from the procedure in [Set up a JWT Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-provider.md)&gt;|
    |**API Version**|&lt;The API version provided by Verifi, as necessary&gt;|

5.  Select **Submit**.

6.  For card network integration, repeat steps 2 through 5 for the CardDataSecurity.ClientToken and CardDataSecurity.DataTokenSigner records.


## Result

The Card Data Security connection records are configured.

## What to do next

[Set up a credential](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-credential.md).

