---
title: Connector domain metadata
description: Override push connector default domain metadata values installed with Event Management with the values in the event HTTP request, including the URL, headers, request body \(payload\), and connector parameters. Override pull connector domain metadata values with connector parameters only.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Connector domain metadata

Override push connector default domain metadata values installed with Event Management with the values in the event HTTP request, including the URL, headers, request body \(payload\), and connector parameters. Override pull connector domain metadata values with connector parameters only.

## Domain metadata parameters

<table id="table_dyj_4jg_1yb"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Overrides System Property

</th></tr></thead><tbody><tr><td>

**connectorDomainInfoTableName**

</td><td>

Name of the table containing the records with the domain information.

</td><td>

evt\_mgmt.connector\_domain\_info\_table\_name-   **Type**: string
-   **Default value**: core\_company

</td></tr><tr><td>

**connectorDomainInfoColumnName**

</td><td>

Name of the column that has a value that should be matched with the domain identifier. For example, you might want to identify a record in the Domain Info table that has a matching value in the **company\_name** field.

</td><td>

evt\_mgmt.connector\_domain\_info\_column\_name-   **Type**: string
-   **Default value**: name

</td></tr><tr><td>

**connectorDomainIdColumnName**

</td><td>

Name of the table column that stores the domain ID.

</td><td>

evt\_mgmt.connector\_domain\_id\_column\_name-   **Type**: string
-   **Default value**: sys\_domain

</td></tr><tr><td>

**connectorDomainPathColumnName**

</td><td>

Name of the table column that stores the domain path.

</td><td>

evt\_mgmt.connector\_domain\_path\_column\_name-   **Type**: string
-   **Default value**: sys\_domain\_path

</td></tr></tbody>
</table>## Order of preference for accessing domain metadata

You must provide domain metadata to configure personalized push connector domains. The metadata in preferred accessing order are:

1.  Push connector parameters
2.  URL query parameters
3.  HTTP headers
4.  Request body \(payload\)
5.  Default system properties

## URL query parameters

Push connectors have the following URL syntax:

-   Instance Type: `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=<connector-source>`
-   MID Server type: `http://<MID_Server_IP>:<MID_Web_Server_Port>/api/mid/em/inbound_event?Transform=<connector-transform-script-name>`

You can include domain metadata as additional query parameters in the ServiceNow push connector webhook URL. For example, if the domain information source is the sys\_user table, the URL could be `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=<connector-source>&connectorDomainInfoTableName=sys_user`

## Request headers

Any of the domain metadata properties can be passed as part of HTTP request headers. Check the documentation from your third-party monitoring tool for information about how request headers are set.

## Request body \(payload\)

You can reference domain metadata from the request body \(JSON payload\) by setting the metadata parameters as root-level keys in the payload. The following example shows how the **connectorDomainInfoTableName** and **connectorDomainInfoColumnName** parameters might be passed as part of the request body:

-   **\{**

    “source”: “Azure Monitor”,

    “host”: “127.0.0.1”,

    “company”: “ServiceNow”,

    “connectorDomainInfoTableName”: “sys\_user”,

    “connectorDomainInfoColumnName”: “first\_name”

    \}


**Note:** For information on connector parameters, see [Personalize domains for push connector events to use in event creation](../task/personalize-domain-separation-push-connectors.md).

**Parent Topic:**[Event Management reference](event-management-reference.md)

