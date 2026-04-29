---
title: Set up a Token Signer
description: Configure a token signer to enable secure JWT-based authentication for tokenizer service integration. This task involves creating an OAuth entity profile with JWT Bearer grant type, setting up OAuth credentials, and establishing a connection alias that links to your tokenizer service endpoint.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up a Token Signer

Configure a token signer to enable secure JWT-based authentication for tokenizer service integration. This task involves creating an OAuth entity profile with JWT Bearer grant type, setting up OAuth credentials, and establishing a connection alias that links to your tokenizer service endpoint.

## Before you begin

Role required: admin

Complete set up for context-aware authorization in the tokenizer service. See [Initial setup for Vault schema, Connections and Service Account for Card data security \(KB2830577\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2830577) for more information.

Perform the following set up tasks for the token signer:

-   [Create a JKS file](create-a-jks-file.md)
-   [Create an X.509 Certificate](create-an-x-509-certificate.md)
-   [Set up a JWT key](set-up-a-jwt-key.md)
-   [Set up a JWT Provider](set-up-a-jwt-provider.md)

**Note:** Ensure you are using the Token Signing credentials JSON file from the tokenizer service when performing the above set up tasks.

## Procedure

1.  Navigate to **All** &gt; **oauth\_entity\_profile.do**.

2.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Grant type**|JWT Bearer|
    |**OAuth provider**|&lt;The OAuth provider for the client bearer token&gt;|
    |**JWT Provider**|&lt;The Token Signing JWT Provider created from the task [Set up a JWT Provider](set-up-a-jwt-provider.md)&gt;|

3.  Select **Submit**.

4.  In the OAuth Entity Profiles list, verify **Is default** is set to `false`.

5.  [Set up an OAuth Credential](set-up-an-oauth-credential.md).

    In the **OAuth entity profile** field, select the OAuth entity profile created earlier in this procedure.

6.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

7.  Select the **CardDataSecurity.DataTokenSigner** record.

8.  In the Connections related list, select **New**.

9.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the HTTP\(s\) connection&gt;|
    |**Connection URL**|&lt;The tokenizer service endpoint URL i.e. the `tokenURI` value from the token signing credentials JSON file&gt;|
    |**Credential**|&lt;The OAuth Credential created earlier in this procedure&gt;|
    |**Connection alias**|sn\_data\_sec.CardDataSecurity\_DataTokenSigner|
    |**vault\_id Attribute**|&lt;The vault ID of the tokenizer service data vault&gt;|


## Result

The token signing JWT Provider is configured.

