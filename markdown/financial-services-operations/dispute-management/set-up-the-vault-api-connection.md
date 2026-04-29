---
title: Set up the Connection &amp; Credential records
description: Configure the Connection &amp; Credential records to enable secure communication between ServiceNow and the tokenizer service for Card Data Security. This connection establishes the endpoint URL and vault ID required for data tokenization operations.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up OAuth for Card Data Security, Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up the Connection &amp; Credential records

Configure the Connection &amp; Credential records to enable secure communication between ServiceNow and the tokenizer service for Card Data Security. This connection establishes the endpoint URL and vault ID required for data tokenization operations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select the CardDataSecurity.ServiceToken record.

3.  In the Connections related list, select **New**.

4.  Enter the following field values.

    |Field|Value|
    |-----|-----|
    |**Name**|&lt;Name of the HTTP\(s\) connection&gt;|
    |**Connection URL**|&lt;The tokenizer service endpoint URL i.e. the `tokenURI` value from the credentials JSON file&gt;|
    |**vault\_id Attribute**|&lt;The vault ID of the tokenizer service data vault&gt;|

5.  Select **Submit**.

6.  Repeat steps 2 through 5 for the CardDataSecurity.ClientToken and CardDataSecurity.DataTokenSigner records.


## Result

The Card Data Security connection records are configured.

## What to do next

[Set up an OAuth Credential](set-up-an-oauth-credential.md).

