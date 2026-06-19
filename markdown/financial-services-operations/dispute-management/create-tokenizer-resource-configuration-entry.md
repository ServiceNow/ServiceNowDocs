---
title: Create a tokenizer resource configuration entry
description: If you create a new HTTP method for a REST Message entry, you need to create an entry in the tokenizer resource configuration entry table. This maps the REST message function to the tokenization service endpoint.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/create-tokenizer-resource-configuration-entry.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [create tokenizer resource configuration entry, tokenizer resource configuration table, add tokenizer resource, rest message function mapping, target system configuration, card data security configuration entry, tokenization service endpoint mapping]
breadcrumb: [Manage Tokenizer Resource Configurations, Administer, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Create a tokenizer resource configuration entry

If you create a new HTTP method for a REST Message entry, you need to create an entry in the tokenizer resource configuration entry table. This maps the REST message function to the tokenization service endpoint.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Card Operations** &gt; **Card Data Security** &gt; **Tokenizer Resource Configurations**.

2.  Select **New**.

3.  Complete the following fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Enter a descriptive name for this configuration entry.|
    |**Target system**|Select the Third-Party System.|
    |**REST message function**|Enter the new HTTP method in the REST message entry.|
    |**Security system**|Select the tokenization service.|

4.  Select **Submit**.


**Parent Topic:**[Manage Tokenizer Resource Configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/manage-tokenizer-resource-configurations.md)

