---
title: LongRunningSOAPRequestProps
description: The following properties are available for long-running SOAP requests.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# LongRunningSOAPRequestProps

The following properties are available for long-running SOAP requests.

<table id="table_b2f_t4h_kp"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.http.connection\_timeout**

</td><td>

Specify the maximum number of milliseconds an outbound HTTP request \(such as Web Services\) will wait to establish a connection.-   Type: integer
-   Default value: 10000 \(10 seconds\)
-   Location: system properties \[sys\_properties\] table

</td></tr><tr><td>

**glide.http.timeout**

</td><td>

Specifies the maximum number of milliseconds to wait before an outbound transaction times out.-   Type: integer
-   Default value: 175000 \(175 seconds\)
-   Location: Add to system properties \[sys\_properties\] table

</td></tr><tr><td>

**glide.soap.max\_redirects**

</td><td>

Specifies the maximum number of redirects the server sends to the client before the soap request is timed out.-   Type: integer
-   Default value: 20
-   Location: system properties \[sys\_properties\] table

</td></tr><tr><td>

**glide.soap.request\_processing\_timeout**

</td><td>

Specify the maximum number of seconds an inbound SOAP request has to finish processing before the connection times out. This property computes a default value from the value of the property **glide.http.timeout** divided by 1000. This property accepts values 5–1200 seconds \(20 minutes\).

 Customers might have network infrastructure \(such as proxy servers\) in place which implement a shorter timeout. In this case, a socket timeout may occur unless this property is set to a shorter value. Set this property to a value several seconds less than the shortest socket inactivity timeout in effect anywhere in the network path between the client application and the instance.

 -   Type: integer
-   Default value: 60
-   Location: system properties \[sys\_properties\] table

</td></tr><tr><td>

**glide.soapprocessor.allow\_long\_running\_threads**

</td><td>

Enables or disables a 307-Temporary Redirect when the request includes a **redirectSupported=true** parameter. The default setting is **true** \(enabled\).

</td></tr><tr><td>

**glide.soapprocessor.max\_long\_running\_threads**

</td><td>

Controls the maximum number of long-running SOAP threads which can run at any one time. The default value for this property is determined dynamically based on the number of SOAP semaphores configured. It should not be necessary to change this value.

</td></tr></tbody>
</table>**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

