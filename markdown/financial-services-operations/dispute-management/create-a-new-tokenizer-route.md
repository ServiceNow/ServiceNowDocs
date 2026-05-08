---
title: Set up tokenized HTTP connection &amp; credential aliases
description: Configure a connection in Card Data Security using an API key for authentication.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up tokenized HTTP connection &amp; credential aliases

Configure a connection in Card Data Security using an API key for authentication.

## Before you begin

Role required: admin

Define the authentication type when setting up a Service Account in the tokenizer service. API keys are long-lived, whereas JWT bearer tokens are time-limited. The tokenizer service generates an API key after you create a Service Account. For more information, see [Initial setup for Vault schema, Connections and Service Account for Card data security \(KB2830577\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2830577).

In ServiceNow, install and set up integrations to the Third-Party Systems \(such as Visa Spoke or Mastercard Spoke\). Card Data Security requires these integrations to function correctly. For more information, see [Integrating with spokes](../../fso-common/concept/spokes.md).

## About this task

You will see records for VROLCardDataSecurity or MastercomCardDataSecurity if Visa Spoke or Mastercard Spoke are installed. These are separate to your existing third-party service connection aliases. Modify these records as required.

## Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the VROLCardDataSecurity or MastercomCardDataSecurity record.

    If you require another third-party connection, create a new Connection &amp; Credential alias. For more information, see Create a Connection &amp; Credential alias.

3.  In the Related Links section, select **Connections** &gt; **New**.

4.  Follow the steps in Create an HTTP\(s\) connection to create a new credential record for this connection.

5.  Enter the following field value.

    |Tokenizer service authentication method|Credential type|
    |---------------------------------------|---------------|
    |**API key**|API Key Credentials|

6.  In the new record form for the credential, use the API key generated from our tokenizer service.

    ![For API key credentials, enter the API key from our tokenizer service into the API Key field for the record.](../image/api-key-credentials.png)


## What to do next

Repeat these steps for each route you need to set up.

