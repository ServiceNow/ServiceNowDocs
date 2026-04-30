---
title: Add connection form
description: Field descriptions for the Add connection form when connecting an observability data source. Add a data connection for Service Observability to ingest data from New Relic or Dynatrace. You can create a connection and API key, or choose to use existing ones.
locale: en-US
release: xanadu
product: Service Observability
classification: service-observability
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Observability reference, Service Observability, ITOM Health, IT Operations Management]
---

# Add connection form

Field descriptions for the **Add connection** form when connecting an observability data source. Add a data connection for Service Observability to ingest data from New Relic or Dynatrace. You can create a connection and API key, or choose to use existing ones.

## Create a connection

<table id="table_d3j_xy3_xdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the connection. The name is used in the Observability data source \[sn\_sow\_svcobs\_data\_source\] table.

</td></tr><tr><td>

Connection URL

</td><td>

URL for the connection. This URL is added to the HTTP\(s\) connections \[http\_connection\] table.

</td></tr><tr><td>

User name

</td><td>

User name for the connection. If you're using an existing API key, confirm it's the name entered in the API Key Credentials \[api\_key\_credentials\] table. If you're creating a connection, this name is entered in that table.**Note:** For New Relic, the User name field should be the New Relic account ID.

</td></tr></tbody>
</table>## Create an API Key credential

|Field|Description|
|-----|-----------|
|API Key|API key for this connection. This key creates an entry in the API Key Credentials \[api\_key\_credentials\] table.|

## Use an existing connection

<table id="table_lcr_gx3_xdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use an existing HTTP\(s\) connection

</td><td>

Option to search for an existing connection.Select the **HTTP Connection** field to see all your valid connections.

</td></tr></tbody>
</table>## Use an existing API key

<table id="table_ylh_fy3_xdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use an existing API Key credential

</td><td>

Option to search for an existing API Key credential.Select the **API Key** field to see all your valid credentials.

</td></tr></tbody>
</table>**Parent Topic:**[Service Observability reference](service-observability-reference.md)

