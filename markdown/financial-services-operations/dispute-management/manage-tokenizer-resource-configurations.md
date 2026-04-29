---
title: Manage Tokenizer Resource Configurations
description: The Tokenizer Resource Configurations table contains entries for each endpoint that sends and receives tokenized data. It defines which REST message function Card Data Security uses based on the API path, HTTP method, and target system.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administer, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Manage Tokenizer Resource Configurations

The Tokenizer Resource Configurations table contains entries for each endpoint that sends and receives tokenized data. It defines which REST message function Card Data Security uses based on the API path, HTTP method, and target system.

Each endpoint entry has an associated REST message function. These REST messages are defined in the REST Message table. See [Set up tokenized REST message record](../task/set-up-a-rest-message-function.md) for more information.

**Note:** Card Data Security includes REST messages for Visa Resolve Online \(VROL\) and Mastercom.

## Accessing Tokenizer Resource Configurations

To access Tokenizer Resource Configurations, navigate to **All** &gt; **Card Operations** &gt; **Card Data Security** &gt; **Tokenizer Resource Configurations**.

## List of fields

|Field|Description|
|-----|-----------|
|Name|Name of the tokenizer resource configuration record.|
|HTTP method|The HTTP method of the request \(e.g. GET, POST, PUT, PATCH, or DELETE\).|
|Path|Path of the API \(e.g. /mastercom/v6/claims/\{claim-id\}\).|
|Target system|The Third-Party System the method is connecting to \(e.g. Visa Resolve Online \(VROL\), Mastercom\).|
|REST message function|The REST message function, which is defined in the REST message record. See [Set up tokenized REST message record](../task/set-up-a-rest-message-function.md) for more information.|
|Security system|The name of the tokenizer service being used.|

-   **[Create a tokenizer resource configuration entry](../task/create-tokenizer-resource-configuration-entry.md)**  
If you create a new HTTP method for a REST Message entry, you need to create an entry in the tokenizer resource configuration entry table. This maps the REST message function to the tokenization service endpoint.

**Parent Topic:**[Managing Card data security](managing-card-data-security.md)

