---
title: Set up tokenized REST message record
description: To use tokenized data with a Third-Party System, update the endpoint URL for the Third-Party System's REST message entry in ServiceNow.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up tokenized REST message record

To use tokenized data with a Third-Party System, update the endpoint URL for the Third-Party System's REST message entry in ServiceNow.

## Before you begin

Set up your Third-Party System connections in our tokenizer service. For more information, see [Initial setup for Vault schema, Connections and Service Account for Card data security \(KB2830577\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2830577).

Install and set up integrations to the Third-Party Systems \(such as Visa Spoke or Mastercard Spoke\). Card Data Security requires these integrations to function correctly. For more information, see [Integrating with spokes](../../fso-common/concept/spokes.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message**.

2.  Open the Visa Resolve Online or Mastercom record.

    Create a new REST Message record if you don't see one for your Third-Party System. For more information, see Create a REST message.

3.  For the **Endpoint** field in the REST message form, enter the connection's base URI from the tokenizer service.

    ![Image showing the Endpoint field containing the connection base URL from the tokenizer service.](../image/rest-message-endpoint.png)

    The connection's base path can be viewed in the tokenizer service administration website by navigating to **Connections**, expanding the connection, and selecting **Sample Request** on a route. The base URL is the domain name of the value in the **Path** field.

    ![Image showing the location of the base URL.](../image/connection-base-path.png)


## What to do next

Repeat these steps for each REST message entry you need to set up.

