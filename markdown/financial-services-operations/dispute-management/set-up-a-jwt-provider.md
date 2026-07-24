---
title: Set up a JWT Provider
description: Configure a JWT Provider to enable secure token-based authentication for Card Data Security by setting up signing configurations and claim values. This provider generates JSON Web Tokens that authenticate requests to the tokenizer service using credentials from your tokenizer service JSON file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/set-up-a-jwt-provider.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [set up jwt provider, jwt provider, json web token provider, signing configuration, standard claims, custom claims, claim value, tokenuri, clientid, jwt bearer token, configure jwt provider]
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up a JWT Provider

Configure a JWT Provider to enable secure token-based authentication for Card Data Security by setting up signing configurations and claim values. This provider generates JSON Web Tokens that authenticate requests to the tokenizer service using credentials from your tokenizer service JSON file.

## Before you begin

Role required: admin

This task needs the following:

<table id="table_sfc_tyn_kjc"><tbody><tr><td>

Card network \(Visa, Mastercard\)

</td><td>

-   A JWT key created for Card Data Security. See [Set up a JWT key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-key.md) for more information.
-   The credentials JSON file obtained from the tokenizer service.

</td></tr><tr><td>

Verifi

</td><td>

A JWT key created for Card Data Security. See [Set up a JWT key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-key.md) for more information.See [Set up Verifi integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-oauth-for-card-data-security.md) for a list of required values.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Providers**.

2.  Select **New**.

3.  For card network integrations, enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the JWT provider&gt;|
    |**Expiry interval**|&lt;Life time of the token \(in seconds\)&gt;|
    |**Signing configuration**|&lt;The JWT key created for Card Data Security&gt;|

    For a Verifi integration, enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the JWT provider&gt;|
    |**Expiry interval**|&lt;Token expiry duration in seconds, as provided by Verifi&gt;|
    |**Signing configuration**|&lt;The Verifi JWT key created for Card Data Security&gt;|

4.  Select **Save**.

5.  Do the following in the **Standard Claims** related list.

<table id="choicetable_cxk_mzn_kjc"><tbody><tr><td id="d81116e323">

**Card network \(Visa, Mastercard\)**

</td><td>

1.  In the `aud` record, update the **Claim Value** with the `tokenURI` value from the tokenizer service credentials JSON file.
2.  In the `iss` record, update the **Claim Value** with the `clientID` value from the tokenizer service credentials JSON file.
3.  In the `sub` record, update the **Claim Value** with a descriptive name.


</td></tr><tr><td id="d81116e374">

**Verifi**

</td><td>

In the `iss` record, update the value to the Issuer ID provided by Verifi.

</td></tr></tbody>
</table>6.  For card network integrations, insert a new row in the **Custom Claims** related list and enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Claim Name**|key|
    |**Claim Value Type**|string|
    |**Claim Value**|&lt;The `keyID` value from the tokenizer service credentials JSON file&gt;|

7.  Select **Update**.


## Result

A JWT provider record is created with updated claim values.

## What to do next

For card network integrations, see [Set up an OAuth Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-provider.md).

For Verifi integrations, see [Set up the Connection &amp; Credential records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-the-vault-api-connection.md).

