---
title: Create new connections in Card Data Security
description: Configure settings in our tokenizer service and your ServiceNow instance to set up new tokenized connections, routes, and methods in Card Data Security.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/dispute-management/creating-new-connections-in-card-data-security.html
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Administer, Card Data Security, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Create new connections in Card Data Security

Configure settings in our tokenizer service and your ServiceNow instance to set up new tokenized connections, routes, and methods in Card Data Security.

To create a new tokenized connection to another core system other than Visa and Mastercard, refer to the following task list.

<table id="table_w55_lxq_qfc"><thead><tr><th>

Task

</th><th>

Location

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Set up connections to the tokenizer service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/dispute-management/set-up-outbound-connections.md)

</td><td>

Tokenizer service

</td><td>

Use the Connections view in our tokenizer service website to set up a new connection to a Third-Party System.

 Use the Route view in our tokenizer service website to add or modify connection routes and field configurations.

 For more information, refer to the [tokenizer service documentation](https://docs.skyflow.com/).

</td></tr><tr><td>

[Set up integration with the Third-Party System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/fso-integrate-other-applications.md)

</td><td>

ServiceNow

</td><td>

Set up a new integration with the Third-Party System.

</td></tr><tr><td>

Create a request builder and response parser

</td><td>

ServiceNow

</td><td>

Create request builder and response parser actions for your new connection. Refer to other FSO banking application spokes for examples.

</td></tr><tr><td>

Create an "Enable Card Data Security" subflow in Workflow Studio for your Third-Party System

</td><td>

ServiceNow

</td><td>

Create a Card Data Security subflow to handle payloads from the Third-Party System.

 Refer to the default subflows in Card Data Security as examples, such as Enable Card Data Security for VROL and Enable Card Data Security for Mastercom.

</td></tr><tr><td>

[Add a decision table entry with API path and subflow mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio/using-decision-builder.md)

</td><td>

ServiceNow

</td><td>

Add a decision table entry to map to the card data security subflow.

</td></tr><tr><td>

[Create a REST message function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/dispute-management/set-up-a-rest-message-function.md)

</td><td>

ServiceNow

</td><td>

Create a new REST message function in **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message** for your Third-Party System.

</td></tr><tr><td>

[Define a REST message HTTP method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/web-services/t_DefineAnHTTPMethod.md)

</td><td>

ServiceNow

</td><td>

Define an HTTP method for each route in the connection.

</td></tr><tr><td>

[Add a mapping configuration record for each REST message function](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/dispute-management/manage-tokenizer-resource-configurations.md)

</td><td>

ServiceNow

</td><td>

In the Tokenizer Resource Configurations table, add an entry for each message function, and map the endpoint URL to the REST message function.

</td></tr></tbody>
</table>**Parent Topic:**[Managing Card data security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/dispute-management/managing-card-data-security.md)

