---
title: Using a load balancer with the Edge proxy server
description: You can use a load balancer to balance the load across the proxy servers in your Edge Encryption proxy setup. If the load balancer and proxy servers are using different ports, specify the host name and HTTPS port of the load balancer to enable users to view responses on their browser.If the load balancer and proxy servers are using different ports, specify the host name and HTTPS port of the load balancer to enable users to view responses on their browser.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# Using a load balancer with the Edge proxy server

You can use a load balancer to balance the load across the proxy servers in your Edge Encryption proxy setup. If the load balancer and proxy servers are using different ports, specify the host name and HTTPS port of the load balancer to enable users to view responses on their browser.

**Important:** All production environments should include at least two Edge Encryption proxy servers for redundancy.

## Edge request processing without a load balancer

If you are not using a load balancer, a request is processed as described below.

1.  The user issues a request from a browser.
2.  The browser sends the request to the Edge proxy server.
3.  The proxy server sends the request to the ServiceNow instance.
4.  The ServiceNow instance returns the response to the proxy server.
5.  The proxy server adds its own port number in the response header before returning the response to the user's browser.

The request is completed successfully because the user can view the response from the proxy server at the port number specified in the response header.

## Edge request processing with a load balancer

However, if you are using a load balancer, the user's browser communicates directly with the load balancer, not with the proxy server. A request is processed as described below.

**Note:** The following example uses `1025` as the proxy server port number.

1.  The user issues a request from a browser.
2.  The browser sends the request to a load balancer Virtual IP \(VIP\), also known as a Virtual Server.
3.  The VIP is configured to point to the proxy server \(for example, `10.2.200.148:1025`\), so the load balancer forwards the request to the proxy server.
4.  The proxy server sends the request to the ServiceNow instance.
5.  The ServiceNow instance returns the response to the proxy server.
6.  The proxy server rewrites the location header in the response with values configured in the properties for `risk-servicenow.dev.echonet:1025`.
    -   **Host**: `edgencryption.proxy.host`
    -   **HTTP port**: `edgeencryption.proxy.http.port`
    -   **HTTPS port**: `edgeencryption.proxy.https.port`
7.  The proxy server forwards the response to the load balancer with the location header pointing to the proxy server port.

The outcome depends on whether the load balancer and proxy servers are using the same port.

-   If the load balancer and proxy servers are using the same port, the request succeeds because the user receives the response from the same port identified in the response header.
-   If the load balancer and proxy servers are using different ports, the request fails because the user's browser communicates only with the load balancer, but the response is on the proxy server.

## Solution

You could resolve the issue by simply using the load balancer and all Edge proxy servers on the same port, but this is not an ideal solution. A better solution is to enable the system to know which port the load balancer uses.

The following properties enable the Edge proxy server to reroute response messages to the load balancer if the proxy server and load balancer are using different ports.

-   **edgeencryption.proxy.rewrite.location.host** specifies the host name used to access ServiceNow through the load balancer.
-   **edgeencryption.proxy.rewrite.location.https.port** specifies the HTTPS port used to access ServiceNow through the load balancer.

**Parent Topic:**[Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md)

## Configure the load balancer

If the load balancer and proxy servers are using different ports, specify the host name and HTTPS port of the load balancer to enable users to view responses on their browser.

### Before you begin

Roles required:

-   local or domain administrator on a Windows host
-   service user with full file system access on a Linux host

### Procedure

1.  Login to the proxy server host as admin, domain admin, or a service user.

2.  Navigate to the installation directory for the Edge proxy and select `conf/edgeencryption.properties`.

3.  Set the following properties:

<table id="table_ezb_gdx_c2b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

edgeencryption.proxy.rewrite.location.host

</td><td>

If your Edge configuration includes a load balancer to balance the load among proxy servers, rewrites responses to the load balancer so requests can be completed.-   If there is a load balancer in the proxy setup, specify the host name used to access ServiceNow through the load balancer.
-   Optional: If there is no load balancer in the proxy setup, you can set this value to the host name used by the proxy server.


</td></tr><tr><td>

edgeencryption.proxy.rewrite.location.https.port

</td><td>

If your Edge configuration includes a load balancer to balance the load among proxy servers, specifies the HTTPS port used to access ServiceNow through the load balancer.-   If there is a load balancer in the configuration, specify the HTTPS port used to access ServiceNow through the load balancer.
-   Optional: If there is no load balancer in the configuration, you can set this value to the HTTPS port used by the proxy server.


</td></tr></tbody>
</table>4.  Save the file.


### Result

Requests can be completed because users can now view responses on their browser.

