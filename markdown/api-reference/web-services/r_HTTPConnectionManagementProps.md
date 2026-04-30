---
title: HTTP Connection Management Properties
description: Connection pooling is controlled by three properties.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage connection pooling, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# HTTP Connection Management Properties

Connection pooling is controlled by three properties.

The default values for these properties are appropriate for most customers. The Glide properties are dynamic, meaning that changes to these properties will take effect immediately. No outage or restart is required to update the values.

<table id="simpletable_kpz_2gp_lq"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

glide.http.connection\_mgr.max\_connections

</td><td>

Controls the total number of permitted HTTP\(S\) connections outbound from the base system instance. This is an instance-wide value.

</td><td>

20

</td></tr><tr><td>

glide.http.connection\_mgr.max\_connections\_per\_host

</td><td>

Controls how many of the `glide.http.connection_mgr.max_connections` can communicate in parallel with any particular host. If the maximum setting for any of these values is reached during normal operations, a script or background thread may have to wait briefly to obtain a connection.

</td><td>

4

</td></tr><tr><td>

glide.http.outbound.max\_timeout

</td><td>

The max timeout in seconds to wait for SOAPMessageV2 and RESTMessageV2 when using executeAsync method. The maximum value allowed is 30 seconds. If this value is set to something higher than 30 seconds, it will default to 30 seconds. To set a value greater than 30 seconds, see the **glide.http.outbound.max\_timeout.enabled** property.

</td><td>

30

</td></tr><tr><td>

glide.http.outbound.max\_timeout.enabled

</td><td>

Determines whether a configurable hard maximum wait time is enforced for SOAPMessageV2 and RESTMessageV2 when using executeAsync method. If this property is set to false, the default response timeout is five minutes.

If this property is set to true, the value of **glide.http.outbound.max\_timeout** is used unless a value is also passed in the waitForResponse\(\) method, in which case the lower value of the two is used.

You can set max response timeouts greater than 30 seconds by setting this property to false and configuring the following additional properties:

-   RESTResponseV2: Set **glide.rest.outbound.ecc\_response.timeout** to the required system default response timeout \(in seconds\).
-   SOAPResponseV2: Set **glide.soap.outbound.ecc\_response.timeout** to the required system default response timeout \(in seconds\).

Then, you can use the waitForResponse\(\) method for custom response timeouts.

</td><td>

true

</td></tr><tr><td>

glide.http.use\_connection\_mgr

</td><td>

Switches connection pooling on and off. To disable the new behavior \(not recommended\) set `glide.http.use_connection_mgr` to **false**.

</td><td>

true

</td></tr></tbody>
</table>**Parent Topic:**[Manage connection pooling](r_HTTPClientConnectionManagement.md)

