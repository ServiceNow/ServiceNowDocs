---
title: Set up a JWT key
description: Configure a JWT key to enable secure authentication for Card Data Security. This is used to sign the authentication tokens that ServiceNow sends to external systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/set-up-a-jwt-key.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [set up jwt key, jwt key, json web token key, signing keystore, signing key, key id, system oauth jwt keys, card data security jwt, configure jwt key, x509 certificate signing]
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up a JWT key

Configure a JWT key to enable secure authentication for Card Data Security. This is used to sign the authentication tokens that ServiceNow sends to external systems.

## Before you begin

Role required: admin

This task needs the following:

<table id="table_sfc_tyn_kjc"><tbody><tr><td>

Card network \(Visa, Mastercard\)

</td><td>

-   A X.509 certificate created for Card Data Security. See [Create an X.509 Certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/create-an-x-509-certificate.md) for more information.
-   The key alias that was defined when generating the JKS file for Card Data Security. See [Create a JKS file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/create-a-jks-file.md) for more information.
-   The credentials JSON file obtained from the tokenizer service.

</td></tr><tr><td>

Verifi

</td><td>

See [Set up Verifi integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-oauth-for-card-data-security.md) for a list of required values.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Keys**.

2.  Select **New**.

3.  For card network integrations, enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the JWT key&gt;|
    |**Signing Keystore**|&lt;The X.509 certificate created for Card Data Security&gt;|
    |**Signing Key**|&lt;The key alias defined when generating the JKS file&gt;|
    |**Key ID**|&lt;The `keyID` value from the credentials JSON file&gt;|

    For a Verifi integration, enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the JWT key&gt;|
    |**Signing Algorithm**|HMAC256, or the value specified by Verifi at the time of account creation|
    |**Signing Key**|&lt;The key alias defined when generating the JKS file&gt;|
    |**Key ID**|&lt;The `keyID` value from the credentials JSON file&gt;|

4.  Select **Submit**.


## Result

A JWT Key record is created.

## What to do next

[Set up a JWT Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-provider.md).

