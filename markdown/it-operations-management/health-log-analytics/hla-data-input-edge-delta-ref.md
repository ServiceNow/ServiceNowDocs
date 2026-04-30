---
title: Edge Delta data input configuration fields
description: Description of the fields on the Edge Delta data input configuration form.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data input configuration field descriptions, Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Edge Delta data input configuration fields

Description of the fields on the Edge Delta data input configuration form.

<table id="table_c4h_ldt_sdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data input name

</td><td>

Name of the new data input. This field is required.

</td></tr><tr><td>

Description

</td><td>

Description of the data input.

</td></tr><tr><td>

Transport

</td><td>

The Edge Delta destination used for streaming log messages to the ServiceNow instance. The options are:-   TCP - Frequently used for handling large volumes of log data.

If you select TCP, you must provide the MID Server and port.

When choosing the TCP transport option, create a TCP destination in Edge Delta to send log data to the instance from any source, using the same MID Server host and port you have configured for the Edge Delta data input.

**Note:** For TCP, TLS/SSL is not supported.

-   HTTP: Frequently used for sending smaller logs via RESTful APIs, HTTP, or HTTPS for secure transmission.

**Note:** For the HTTP protocol, authentication is used.

If you select HTTP, you must provide the MID Web Server that is running on the MID Server. The system then populates the MID Server and port fields automatically, based on the provided MID Web Server.

Depending on the MID Web Server configuration, you can send logs using either HTTP or HTTPS. If the **Secure Connection** check box on the MID Web Server extension form is clear, use HTTP. If it is selected, use HTTPS. For more information, see [Event Management MID Web Server extension form](../../event-management/reference/configure-midwebserver-extension-form.md). In addition, if the **Authentication Type** on the MID Web Server extension form is Basic, provide Basic authentication details in the Authorization header. If the **Authentication Type** is API Key, provide the key as “Key Api\_Key".

When choosing the HTTP transport option, create an HTTP destination in Edge Delta and enter the Endpoint URL in the following format: http://\{MID\_SERVER\_IP\}:\{MID\_WEB\_SERVER\_PORT\}/api/mid/hla/raw. In Advanced Settings, create two headers to be attached to the HTTP request:

    -   An Authorization header with the MID Web Server API key value or basic credentials as MID Web Server configured.
    -   A Content-Type header named with the application/json value.

</td></tr><tr><td>

MID web server

</td><td>

The MID Web Server to which the log data is streamed.

</td></tr><tr><td>

MID server

</td><td>

The MID Server to which the Edge Delta logs are streamed.This field is required. If you selected HTTP in the **Transport** field, this field is populated automatically based on the selected MID Web Server.

</td></tr><tr><td>

Port

</td><td>

The port on the MID Server used for listening to logs.Choose a port within the suggested range from the array. In the case of TCP transport, the port must not be occupied by another process. Make sure that your organization’s security team opens the selected port.

This field is required. If you selected HTTP in the **Transport** field, this field is populated automatically based on the selected MID Web Server.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data. This field is required.Choosing the service instance enables HLA to correlate CIs and service instances in the CMDB for root cause analysis.

**Note:** If no relevant service instance exists, [Create an service instance](https://www.servicenow.com/docs/access?context=create-it-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and add CIs to it. Set the status of the new service instance to Operational.

</td></tr></tbody>
</table>**Parent Topic:**[Data input configuration field descriptions](../concept/hla-data-input-config-fields.md)

