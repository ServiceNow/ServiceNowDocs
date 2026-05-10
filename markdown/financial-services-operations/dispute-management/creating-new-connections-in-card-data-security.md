---
title: Create new connections in Card Data Security
description: Configure settings in our tokenizer service and your ServiceNow instance to set up new tokenized connections, routes, and methods in Card Data Security.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Create new connections in Card Data Security

Configure settings in our tokenizer service and your ServiceNow instance to set up new tokenized connections, routes, and methods in Card Data Security.

To create a new tokenized connection to another core system other than Visa and Mastercard, refer to the following task list.

<table id="table_w55_lxq_qfc"><thead><tr><th>

Task

</th><th>

Description

</th><th>

Where to perform

</th></tr></thead><tbody><tr><td>

[Configure the tokenizer service](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2830577)

</td><td>

Use the tokenizer service website to set up a new connections and service accounts for a Third-Party System.

</td><td>

Tokenizer service

</td></tr><tr><td>

[Set up integration with the Third-Party System](../../fso-common/concept/fso-integrate-other-applications.md)

</td><td>

Set up a new integration with the Third-Party System.

</td><td>

ServiceNow

</td></tr><tr><td>

Create a request builder and response parser

</td><td>

Create request builder and response parser actions for your new connection. Refer to other FSO banking application spokes for examples.

</td><td>

ServiceNow

</td></tr><tr><td>

Create an "Enable Card Data Security" subflow in Workflow Studio for your Third-Party System

</td><td>

Create a Card Data Security subflow to handle payloads from the Third-Party System.

 Refer to the default subflows in Card Data Security as examples, such as Enable Card Data Security for VROL and Enable Card Data Security for Mastercom.

</td><td>

ServiceNow

</td></tr><tr><td>

[Add a decision table entry with API path and subflow mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/using-decision-builder.md)

</td><td>

Add a decision table entry to map to the card data security subflow.

</td><td>

ServiceNow

</td></tr><tr><td>

[Create a REST message function](../task/set-up-a-rest-message-function.md)

</td><td>

Create a new REST message function in **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message** for your Third-Party System.

</td><td>

ServiceNow

</td></tr><tr><td>

[Define a REST message HTTP method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_DefineAnHTTPMethod.md)

</td><td>

Define an HTTP method for each route in the connection.

</td><td>

ServiceNow

</td></tr><tr><td>

[Add a mapping configuration record for each REST message function](manage-tokenizer-resource-configurations.md)

</td><td>

In the Tokenizer Resource Configurations table, add an entry for each message function, and map the endpoint URL to the REST message function.

</td><td>

ServiceNow

</td></tr></tbody>
</table>**Parent Topic:**[Managing Card data security](managing-card-data-security.md)

