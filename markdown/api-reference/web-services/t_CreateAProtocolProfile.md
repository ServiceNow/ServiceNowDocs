---
title: Create a protocol profile
description: You can create a custom HTTPS protocol profile to specify the credentials and certificates used for outbound web services. For example, you can create a custom HTTPS protocol profile to enable mutual authentication.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Outbound web service mutual authentication, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Create a protocol profile

You can create a custom HTTPS protocol profile to specify the credentials and certificates used for outbound web services. For example, you can create a custom HTTPS protocol profile to enable mutual authentication.

## Before you begin

-   Role required: admin
-   [Uploading a certificate to an instance](https://www.servicenow.com/docs/access?context=t_UploadACertificateToAnInstance&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) to authenticate the client certificate of the instance.
-   [Uploading a trusted server certificate](https://www.servicenow.com/docs/access?context=t_UploadATrustedServerCertificate&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) to authenticate the server certificate of the web service provider.

## About this task

Mutual authentication causes the web service provider and consumer to authenticate with each other before communicating. You must configure a REST or SOAP message to support mutual authentication.

-   Outbound REST: Create a REST message using basic authentication.
-   Outbound SOAP: Create a SOAP message using mutual authentication.

**Note:** Mutual authentication is not available when making outbound web service calls through a MID Server.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Protocol Profiles**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_jxy_gsm_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Protocol

</td><td>

Enter a unique name to identify this HTTPS protocol, such as `mauth`. The protocol name allows you to differentiate between normal HTTPS connections and HTTPS connections that use this protocol profile. The name you enter becomes the protocol name in the URL. For example, `mauth://endpoint.service.com`**Note:**

-   Don't include upper case letters or special characters in the protocol name.
-   You can't create a custom protocol with an existing protocol name such as HTTPS.


</td></tr><tr><td>

Default port

</td><td>

Enter the port number for connections that use this protocol.

</td></tr><tr><td>

Check box

</td><td>

Select the client certificate the protocol uses to authenticate itself with the web service provider. The certificate must have a **Type** value of Java Key Store or PKCS12 Key Store.

</td></tr></tbody>
</table>
**Parent Topic:**[Outbound web service mutual authentication](../concept/c_OutboundWebServicesMutualAuth.md)

