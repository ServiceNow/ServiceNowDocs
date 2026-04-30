---
title: Configure ODBC to use proxy servers
description: The ODBC driver can be configured to route its HTTP SOAP requests via an HTTP proxy server.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure ODBC to use proxy servers

The ODBC driver can be configured to route its HTTP SOAP requests via an HTTP proxy server.

## Before you begin

You must have administrator-level access for the Windows computer on which you want to configure ODBC to use proxy servers.

## About this task

Setting up a proxy server gives you the option to control access to the ServiceNow instance from the proxy server, and potentially allows a network configuration that can monitor usage statistics. However, because the proxy server intercepts the ODBC driver's requests to your ServiceNow instance, it will degrade the performance of the driver.

**Note:** This feature is recommended for use with ODBC driver builds dated 7/15/2011 or later.

To enable the use of proxy servers, the custom properties for proxy server settings must be defined first for the data source. After that, these properties can be overridden by specific ODBC DSNs.

## Procedure

1.  In Windows, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC** &gt; **Management Console**.

2.  Expand the Console Root tree to: `ServiceNow ODBC Manager\Manager\<installation location>\Services\ServiceNow_ODBC\Data Source Settings\ServiceNow\IP Parameters`.

3.  Double-click the **DataSourceIpCustomProperties** attribute.

    ![ODBC proxy](../image/OdbcProxy.png "ODBC proxy")

4.  Set the following custom properties to configure the ODBC proxy server.

    |Property name|Description|Example|
    |-------------|-----------|-------|
    |proxy\_host|The proxy server host name or IP address.|proxy.company.com|
    |proxy\_port|The proxy server port number.|8080|
    |proxy\_user\_name|The proxy server user name or id, used in an authenticating proxy configuration.|odbc\_user|
    |proxy\_user\_password|The proxy server user password, used with the proxy\_name value in an authenticating proxy configuration.|\*\*\*\*\*|


**Parent Topic:**[Configuring the ODBC driver](../concept/configuring-odbc.md)

