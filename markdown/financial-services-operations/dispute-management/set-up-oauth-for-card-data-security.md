---
title: Set up OAuth for Card Data Security
description: After you configure your tokenizer service, follow these steps to set up OAuth connectivity with your ServiceNow instance. This connection is required to get file metadata and download URLs from files hosted in the tokenizer service vault.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up OAuth for Card Data Security

After you configure your tokenizer service, follow these steps to set up OAuth connectivity with your ServiceNow instance. This connection is required to get file metadata and download URLs from files hosted in the tokenizer service vault.

## Token Authentication in Card Data Security

Card Data Security uses JSON Web Tokens \(JWT\) for authentication. It uses the following token types for authentication:

-   Regular tokens—used for authentication in backend connections.
-   Context-aware tokens—required for user interactions in the UI, such as viewing documents in the data vault.

## Overview of tasks to set up OAuth for Card Data Security

When you set up OAuth for Card Data Security, you will need to set up each connection type below.

<table id="table_a3r_h1y_g3c"><thead><tr><th>

Name

</th><th>

Connection Alias

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Token

</td><td>

CardDataSecurity.ServiceToken

</td><td>

For Vault API interactions and backend requests, such as retrieving file download URLs or external document metadata.Perform all steps below for this connection type.

</td></tr><tr><td>

Client Token

</td><td>

CardDataSecurity.ClientToken

</td><td>

For obtaining context-aware bearer tokens that are used in detokenization requests. Used for viewing files and revealing PAN values.Perform all steps below for this connection type.

</td></tr><tr><td>

Data Token Signer

</td><td>

CardDataSecurity.DataTokenSigner

</td><td>

Required for context-aware authorization. Signs data tokens that are used to make detokenization requests to the data vault. Used for revealing PAN values.**Note:** The steps below differ when setting up a data token signer. See [Set up a Token Signer](../task/set-up-a-token-signer.md) for specific steps on this connection type.

</td></tr></tbody>
</table>1.  [Create a JKS file](../task/create-a-jks-file.md)

    Generate a Java KeyStore \(JKS\) file for OAuth authentication setup.

2.  [Create an X.509 Certificate](../task/create-an-x-509-certificate.md)

    Create an X.509 certificate record by uploading a JKS file and configuring the certificate settings.

3.  [Set up a JWT key](../task/set-up-a-jwt-key.md)

    Configure a JSON Web Token \(JWT\) key by linking X.509 certificates with tokenizer service credentials.

4.  [Set up a JWT Provider](../task/set-up-a-jwt-provider.md)

    Configure a JWT Provider by setting up signing configurations and claim values.

5.  [Set up an OAuth Provider](../task/set-up-an-oauth-provider.md)

    Configure an OAuth provider to establish the necessary connection credentials and JWT configuration.

6.  [Set up the Connection &amp; Credential records](../task/set-up-the-vault-api-connection.md)

    Configure the Vault API connection to establish the endpoint URL and vault ID required for data tokenization operations.

7.  [Set up an OAuth Credential](../task/set-up-an-oauth-credential.md)

    Create an OAuth 2.0 credential to enable secure authentication for Card Data Security integrations.

8.  [Set up the OAuth Vault API REST message](../task/set-up-the-vault-api-rest-message.md)

    Configure the Data Security Vault API REST message with the correct endpoint URL and OAuth authentication profile.


