---
title: Configure the connection and credential aliases
description: Configure the two connection and credential aliases with the SupplyOn host and subscription keys for your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplyon-configure-connection-aliases.html
release: zurich
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [Configuring the Supplyon integration, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure the connection and credential aliases

Configure the two connection and credential aliases with the SupplyOn host and subscription keys for your environment.

## Before you begin

SupplyOn has issued two APIM subscription keys, one for the orders product and one for the demand-response product. You have the SupplyOn gateway host URL for your environment.

Role required: admin

## About this task

The integration defines two connection and credential aliases. Configure the connection URL and API key on each alias for your environment. These values are runtime data and aren't stored in source.

|Alias|Name on the instance|Purpose|Base path|
|-----|--------------------|-------|---------|
|supplyOnOrders|SupplyOn Product SCC Interfaces for Customer subscription|Outbound POST /purchaseorder|/scc/order/v1|
|supplyOnDemandResponse|SupplyOn Product SCC Public APIs subscription|Inbound GET /demandresponse and /demandresponse-summaries|/scc/demandresponse/v1|

|Field|Value|
|-----|-----|
|Connection type|HTTP connection \(http\_connection\)|
|Host|The SupplyOn gateway host for the environment \(a separate host is used for PRD\).|
|Credential type|API key \(api\_key\_credentials\)|
|Auth header|Ocp-Apim-Subscription-Key \(both aliases, two distinct key values\).|
|Setup wizard|SupplyOn PO, API Key. Prompts for connection name, connection URL, and API key.|
|Secret storage|Credential store only. No key values are committed to source.|

## Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the **supplyOnOrders** alias.

    Use the setup wizard to enter the connection name, the connection URL \(the SupplyOn gateway host for your environment\), and the orders subscription key. The key is stored in the credential store.

3.  Open the **supplyOnDemandResponse** alias and enter the same connection settings and the demand-response subscription key.

4.  Test the connection through the orders alias.

    A test `POST /purchaseorder` through the orders alias returns HTTP 201 on success.


## What to do next

**Note:** Both aliases reference the out-of-box Default HTTP Retry Policy. See [SupplyOn error handling and retry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplyon-error-handling.md).

