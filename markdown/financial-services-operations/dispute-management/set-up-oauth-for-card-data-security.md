---
title: Set up OAuth for Card Data Security
description: After you configure your tokenizer service, follow these steps to set up OAuth connectivity with your ServiceNow instance. This connection is required to get file metadata and download URLs from files hosted in the tokenizer service vault.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/set-up-oauth-for-card-data-security.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [set up oauth card data security, oauth authentication, jwt authentication, json web token, context-aware token, service token, client token, data token signer, carddatasecurity servicetoken, carddatasecurity clienttoken, carddatasecurity datatokensigner, tokenizer service authentication]
breadcrumb: [Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up OAuth for Card Data Security

After you configure your tokenizer service, follow these steps to set up OAuth connectivity with your ServiceNow instance. This connection is required to get file metadata and download URLs from files hosted in the tokenizer service vault.

## Token Authentication in Card Data Security

Card Data Security uses JSON Web Tokens \(JWT\) for authentication. It uses the following token types for authentication:

-   Regular tokens—used for authentication in backend connections.
-   Context-aware tokens—required for user interactions in the UI, such as viewing documents in the data vault.

## Set up card network integration

When you set up OAuth for card network integration, set up each following connection type.

|Name|Connection Alias|Description|Procedure|
|----|----------------|-----------|---------|
|Service Token|CardDataSecurity.ServiceToken|For Vault API interactions and backend requests, such as retrieving file download URLs or external document metadata.|Perform all the following steps for this connection type.|
|Client Token|CardDataSecurity.ClientToken|For obtaining context-aware bearer tokens that are used in detokenization requests. Used for viewing files and revealing PAN values.|Perform all the following steps for this connection type.|
|Data Token Signer|CardDataSecurity.DataTokenSigner|Required for context-aware authorization. Signs data tokens that are used to make detokenization requests to the data vault. Used for revealing PAN values.|Refer to [Set up a Token Signer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-token-signer.md) for specific steps on this connection type.|

1.  [Create a JKS file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/create-a-jks-file.md)
2.  [Create an X.509 Certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/create-an-x-509-certificate.md)
3.  [Set up a JWT key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-key.md)
4.  [Set up a JWT Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-provider.md)
5.  [Set up an OAuth Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-provider.md)
6.  [Set up the Connection &amp; Credential records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-the-vault-api-connection.md)
7.  [Set up a credential](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-credential.md)
8.  [Set up the API REST message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-the-vault-api-rest-message.md)

## Set up Verifi integration

Prepare the following values before you set up this integration. Obtain these values from your Verifi onboarding documentation or account manager, and from your tokenizer service connection setup procedure.

-   Signing algorithm: typically HMAC256 \(confirm with Verifi\).
-   JWT Signing Key: a unique key provided by Verifi.
-   JWT Expiry Interval: value in seconds, provided by Verifi.
-   Issuer ID: provided by Verifi.
-   API Version: provided by Verifi.
-   Tokenizer service connection URL: URL used to route requests to Verifi's APIs.
-   Tokenizer service API key: provided by the tokenizer service during connection setup.

Perform the following tasks:

1.  [Set up a JWT key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-key.md)
2.  [Set up a JWT Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-a-jwt-provider.md)
3.  [Set up the Connection &amp; Credential records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-the-vault-api-connection.md)
4.  [Set up a credential](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-an-oauth-credential.md)
5.  [Set up the Verifi Connection &amp; Credential Alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-verifi-connection-credential-alias.md)
6.  [Set up the API REST message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/set-up-the-vault-api-rest-message.md)

