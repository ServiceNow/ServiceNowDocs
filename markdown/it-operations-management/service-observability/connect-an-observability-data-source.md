---
title: Connect a Service Observability data source
description: Connect Service Observability to an external observability system. Service Observability displays metrics in the Service Operations Workspace \(SOW\) from that observability instance.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Connect a Service Observability data source

Connect Service Observability to an external observability system. Service Observability displays metrics in the Service Operations Workspace \(SOW\) from that observability instance.

## Before you begin

You must enter a connection URL and credentials for your observability vendor. You can either use an existing connection or create one. Note the following for specific vendors:

<table id="table_i4m_bwf_yfc"><thead><tr><th>

Observability Vendor

</th><th>

Connection information

</th></tr></thead><tbody><tr><td>

AWS

</td><td>

The connection URL must be specific to the region to be monitored, for example, `https://monitoring.us-east-2.amazonaws.com`.

</td></tr><tr><td>

Azure

</td><td>

The connection URL should be `https://management.azure.com`.

</td></tr><tr><td>

Splunk Observability

</td><td>

The connection URL must include the Realm, for example, https://stream.\[REALM\].signalfx.com

</td></tr><tr><td>

Zabbix

</td><td>

The connection URL must be the IP on which the Zabbix server is hosted

</td></tr></tbody>
</table>If you're using existing credentials, you need the credential name. If you're creating credentials, collect the following information.

<table id="table_kfv_f5t_rfc"><thead><tr><th>

Observability vendor

</th><th>

Credential type

</th><th>

Information needed

</th></tr></thead><tbody><tr><td>

AppDynamics

</td><td>

OAuth 2.0

</td><td>

-   OAuth Client ID
-   OAuth Client secret
-   OAuth token URL
-   AppDynamics account name

</td></tr><tr><td>

Azure

</td><td>

OAuth 2.0

</td><td>

-   OAuth Client ID
-   OAuth Client secret
-   OAuth token URL
-   Subscription ID

</td></tr><tr><td>

AWS

</td><td>

AWS credentials

</td><td>

-   Access key
-   Secret key

 If the user associated with this key is restricted to specific permissions, they must include the following, scoped to all resources:

 -   `cloudwatch:Describe` scoped to all resources

-   `cloudwatch:Get` scoped to all resources

-   `cloudwatch:List` scoped to all resources

-   `cloudtrail:LookupEvents`

-   `tag:GetResources`

-   `tag:GetTagKeys`

-   `tag:GetTagValues`

-   `apigateway:Get`


</td></tr><tr><td>

Datadog

</td><td>

API

</td><td>

-   API key
-   Application key

 If an application key is restricted to a specific scope, those scopes are required for the following endpoints:

-   https://api.datadoghq.com/api/v2/catalog/entity
-   https://api.datadoghq.com/api/v1/hosts
-   https://api.datadoghq.com/api/v1/query
-   https://api.datadoghq.com/api/v2/query/timeseries

</td></tr><tr><td>

Dynatrace SaaS Classic

</td><td>

API

</td><td>

API Tenant Access TokenThe token must have `entities.read` and `metrics.read` scope permissions.

</td></tr><tr><td>

Dynatrace SaaS Grail

</td><td>

API

</td><td>

API Platform TokenThe token must have `storage:metrics.read` and `storage:bucket.read` scope permissions.

</td></tr><tr><td>

Dynatrace on-premise

</td><td>

API

</td><td>

-   API key. The key must be an environment scoped token.
-   The name of the MID Server your Dynatrace instance is hosted on

</td></tr><tr><td>

New Relic

</td><td>

API

</td><td>

-   Account ID
-   API key

</td></tr><tr><td>

Prometheus on-premise

</td><td>

Basic Auth

</td><td>

-   Basic Auth credential user name
-   Basic Auth credential password
-   The name of the MID Server your Prometheus instance is hosted on

</td></tr><tr><td>

SolarWinds

</td><td>

Basic Auth

</td><td>

-   Basic Auth credential user name
-   Basic Auth credential password
-   The name of the MID Server your SolarWinds instance is hosted on

</td></tr><tr><td>

Splunk Enterprise

</td><td>

API

</td><td>

Bearer Token

</td></tr><tr><td>

Splunk Observability

</td><td>

API

</td><td>

Access token

</td></tr><tr><td>

ThousandEyes

</td><td>

API

</td><td>

API key

</td></tr><tr><td>

Zabbix

</td><td>

Basic Auth

</td><td>

-   Basic Auth credential user name
-   Basic Auth credential password
-   The name of the MID Server your Zabbix instance is hosted on. The MID Server must be in an active state.

</td></tr></tbody>
</table>Role required: sn\_sow\_svcobs.admin

## About this task

The first step to ingesting observability data is to create a connection to the observability instance.

Service Observability supports the following observability vendors:

-   Amazon CloudWatch
-   AppDynamics
-   Cisco ThousandEyes synthetic tests
-   Datadog
-   DynatraceSaaS and on-premise \(both Classic and Grail environments\)
-   Microsoft Azure Monitor
-   New Relic
-   Prometheus on-premise
-   SolarWinds on-premise
-   Splunk Observability and logs from Splunk Enterprise
-   Zabbix on-premise

## Procedure

1.  Navigate based on your version of Service Observability.

    -   Version 1.5.0: Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**, then navigate to **Service Observability Management** &gt; **Manage Observability** &gt; **Data sources**
    -   Version 1.6 or later: Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**, then navigate to **Service Observability** &gt; **Data sources**.
2.  Select your observability vendor.

3.  On the **Add connection** form, fill in the fields.

    You can use an existing HTTP or HTTPs connection and an existing credential or create one.

4.  Select **Save**.


## Result

A new connection appears in the list of observability data sources. You use this connection when you create a data mapping.

## What to do next

Map your connection to the services that you want to monitor in Service Observability. See [Create and manage data mappings](create-and-manage-observability-data-mappings.md).

**Parent Topic:**[Configuring Service Observability](../concept/configuring-service-observability.md)

