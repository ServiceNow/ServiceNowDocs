---
title: Manage the card vault table and connections in our tokenizer service
description: You may modify the card vault table and connection properties in our tokenizer service. Manage the vault columns and properties, and customize the data sent and received from the Third-Party System, such as additional routes and field values.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Manage the card vault table and connections in our tokenizer service

You may modify the card vault table and connection properties in our tokenizer service. Manage the vault columns and properties, and customize the data sent and received from the Third-Party System, such as additional routes and field values.

For more details on these topics, refer to the [tokenizer service documentation](https://docs.skyflow.com/).

## Managing the card vault table

Refer to the [tokenizer service documentation](https://docs.skyflow.com/) for more information on managing the card vault table, including:

-   Creating or deleting columns.
-   Modifying column properties \(such as the name, input format, token settings, redaction, and encryption\).
-   Using SQL to query the vault.
-   Reviewing vault table properties.

**Note:** You must use the included tokenizer service's card vault table in Card Data Security to enable tokenization for Dispute Cases and Dispute Transactions.

## Change the connection properties

Use the Connection view to updating the connection name, description, and outbound base URL.

## Change the third-party connection configuration

Use the Advanced Configuration view in the tokenizer service administration site to manage the outbound base URL and outbound authentication details for the Third-Party System.

## Modifying connection routes and fields

To add or modify connection routes, use the Route view. You may edit an existing route to modify values such as:

-   API path
-   HTTP method
-   Content type
-   Request header fields and tokenization actions
-   Request body fields and tokenization actions
-   Response header fields and tokenization actions
-   Response body fields and tokenization actions
-   URL parameters

**Parent Topic:**[Managing Card data security](managing-card-data-security.md)

