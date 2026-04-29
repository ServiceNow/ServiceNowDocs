---
title: Set up an OAuth Provider
description: Configure an OAuth provider to enable secure authentication between ServiceNow and a third-party tokenizer service for Card Data Security. This setup establishes the necessary connection credentials and JWT configuration required for secure data tokenization operations.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up an OAuth Provider

Configure an OAuth provider to enable secure authentication between ServiceNow and a third-party tokenizer service for Card Data Security. This setup establishes the necessary connection credentials and JWT configuration required for secure data tokenization operations.

## Before you begin

Role required: admin

This task requires the following:

-   A JWT provider created for Card Data Security. See [Set up a JWT Provider](set-up-a-jwt-provider.md) for more information.
-   The credentials JSON file obtained from the tokenizer service.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  Select **Connect to a third party OAuth Provider - Outbound**.

4.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the OAuth provider&gt;|
    |**Default Grant Type**|JWT Bearer|
    |**Send credentials**|As Private Key JWT|
    |**JWT Provider**|&lt;The JWT provider created for Card Data Security&gt;|
    |**Token URL**|&lt;The tokenizer service endpoint URL i.e. the `tokenURI` value from the credentials JSON file&gt;|
    |**Client ID**|&lt;The `clientID` value from the credentials JSON file&gt;|
    |**OAuth API script**|OAuthDataSecurityUtil|

5.  Select **Save**.

6.  In the **OAuth Entity Profiles** related list, select the default profile.

7.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**JWT Provider**|&lt;The JWT provider created for Card Data Security&gt;|

8.  Select **Update**.


## Result

The JWT provider record is created.

## What to do next

[Set up the Connection &amp; Credential records](set-up-the-vault-api-connection.md).

