---
title: Set up a JWT Provider
description: Configure a JWT Provider to enable secure token-based authentication for Card Data Security by setting up signing configurations and claim values. This provider generates JSON Web Tokens that authenticate requests to the tokenizer service using credentials from your tokenizer service JSON file.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up a JWT Provider

Configure a JWT Provider to enable secure token-based authentication for Card Data Security by setting up signing configurations and claim values. This provider generates JSON Web Tokens that authenticate requests to the tokenizer service using credentials from your tokenizer service JSON file.

## Before you begin

Role required: admin

This task needs the following:

-   A JWT key created for Card Data Security. See [Set up a JWT key](set-up-a-jwt-key.md) for more information.
-   The credentials JSON file obtained from the tokenizer service.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Providers**.

2.  Select **New**.

3.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the JWT provider&gt;|
    |**Expiry interval**|&lt;Life time of the token \(in seconds\)&gt;|
    |**Signing configuration**|&lt;The JWT key created for Card Data Security&gt;|

4.  Select **Save**.

5.  Do the following in the **Standard Claims** related list.

    1.  In the `aud` record, update the **Claim Value** with the `tokenURI` value from the tokenizer service credentials JSON file.

    2.  In the `iss` record, update the **Claim Value** with the `clientID` value from the tokenizer service credentials JSON file.

    3.  In the `sub` record, update the **Claim Value** with a descriptive name.

6.  Insert a new row in the **Custom Claims** related list.

7.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Claim Name**|key|
    |**Claim Value Type**|string|
    |**Claim Value**|&lt;The `keyID` value from the tokenizer service credentials JSON file&gt;|

8.  Select **Update**.


## Result

A JWT provider record is created with updated claim values.

## What to do next

[Set up an OAuth Provider](set-up-an-oauth-provider.md).

