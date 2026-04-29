---
title: Set up a JWT key
description: Configure a JWT key to enable secure authentication for Card Data Security by linking X.509 certificates with tokenizer service credentials. This setup is required before creating a JWT provider for OAuth authentication workflows.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up a JWT key

Configure a JWT key to enable secure authentication for Card Data Security by linking X.509 certificates with tokenizer service credentials. This setup is required before creating a JWT provider for OAuth authentication workflows.

## Before you begin

Role required: admin

This task needs the following:

-   A X.509 certificate created for Card Data Security. See [Create an X.509 Certificate](create-an-x-509-certificate.md) for more information.
-   The key alias that was defined when generating the JKS file for Card Data Security. See [Create a JKS file](create-a-jks-file.md) for more information.
-   The credentials JSON file obtained from the tokenizer service.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Keys**.

2.  Select **New**.

3.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the JWT key&gt;|
    |**Signing Keystore**|&lt;The X.509 certificate created for Card Data Security&gt;|
    |**Signing Key**|&lt;The key alias defined when generating the JKS file&gt;|
    |**Key ID**|&lt;The `keyID` value from the credentials JSON file&gt;|

4.  Select **Submit**.


## Result

A JWT Key record is created.

## What to do next

[Set up a JWT Provider](set-up-a-jwt-provider.md).

