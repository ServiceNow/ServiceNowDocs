---
title: Set up tokenized HTTP connection and credentials
description: After configuring the connections for Card Data Security in our tokenizer service, you can define the connection and credentials in your ServiceNow instance. This enables you to communicate to the Third-Party System in your ServiceNow instance via our tokenizer service.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up tokenized HTTP connection and credentials

After configuring the connections for Card Data Security in our tokenizer service, you can define the connection and credentials in your ServiceNow instance. This enables you to communicate to the Third-Party System in your ServiceNow instance via our tokenizer service.

## Before you begin

Set up your Third-Party System connections in our tokenizer service. For more information, see [Set up connections to the tokenizer service](set-up-outbound-connections.md).

Install and set up integrations to the Third-Party Systems \(such as Visa Spoke or Mastercard Spoke\). Card Data Security requires these integrations to function correctly. For more information, see [Integrating with spokes](../../fso-common/concept/spokes.md).

Role required: admin

## About this task

You need to create new connection aliases to third-party services that use our tokenizer service. These are separate from your existing third-party service connection aliases.

## Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Create a Connection &amp; Credential alias for your third-party connection.

    For more information, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    You will see records for VROLCardDataSecurity or MastercomCardDataSecurity if Visa Spoke or Mastercard Spoke are installed.

3.  Select the card data security connection for the third-party service you want to modify.

4.  In the Related Links section, select **Connections** &gt; **New**.

5.  Follow the steps in [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) to create a new credential record for this connection.

    When selecting the type of credentials to create, select the credential type that match the authentication method you defined in our tokenizer service as part of the steps in [Set up connections to the tokenizer service](set-up-outbound-connections.md).

    |Tokenizer service authentication method|Credential type|
    |---------------------------------------|---------------|
    |**API key**|API Key Credentials|
    |**JWT**|OAuth 2.0 Credentials|

    In the new record form for the credential, use the API key or credentials data generated from our tokenizer service.

    ![For API key credentials, enter the API key from our tokenizer service into the API Key field for the record.](../image/api-key-credentials.png)


## What to do next

Repeat these steps for each route you need to set up.

