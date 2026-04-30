---
title: Configure SOAP security
description: Administrators can configure web service security for inbound SOAP requests made to the ServiceNow instance.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Configure SOAP security

Administrators can configure web service security for inbound SOAP requests made to the ServiceNow instance.

## Before you begin

Role required: admin

## About this task

You can also set up web service security to use different certificates for different web service clients. By enabling web service security, you can prevent man-in-the-middle attacks.

**Note:** After you configure a WS-security profile or a security policy, validation is performed on all incoming SOAP requests, including from the MID Server or ODBC driver. Disable validation for these types of requests by [marking the service accounts as internal integration users](t_MarkSvcAcctsAsInternalIntegUsers.md).

## Procedure

1.  [Upload a certificate to an instance](https://www.servicenow.com/docs/access?context=t_UploadACertificateToAnInstance&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

2.  [Create a WS-security profile](t_CreateANewWS-SecurityProfile.md).

3.  [Create a security policy](t_CreateANewSecurityPolicy.md).

    Security policies define which WS-security profiles are used to evaluate a particular web service request. If no policy is defined, all WS-security profiles are used to evaluate all requests.

4.  Set the value of the property `glide.soap.default_security_policy` to the name of the new security policy.


**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

