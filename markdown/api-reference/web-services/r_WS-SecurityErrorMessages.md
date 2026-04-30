---
title: WS-Security error messages
description: An instances produces one of the following error messages when it encounters an issue with a WS-security SOAP message.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# WS-Security error messages

An instances produces one of the following error messages when it encounters an issue with a WS-security SOAP message.

|Error|Description|
|-----|-----------|
|Invalid Security Policy Selected. Select an Inbound policy for Inbound Requests.|The default policy name is set to an outbound policy. [Set the default policy name](../task/t_SetTheSOAPDefaultSecurityPolicy.md) to an inbound security policy.|
|SOAP request not Signed. Policy requires signing.|The [SOAP security policy](../concept/c_SOAPWebService.md#SOAP-default-sec-policy) requires signing and the inbound SOAP request is not signed. Either specify a different SOAP security policy or provide the SOAP request with a proper signature.|
|No profiles to authenticate.|The selected Security policy either does not have any security profiles \(X509 or UserNameToken\) or the security profiles are inactive. Verify at least one security profile is active.|
|Unable to verify signed request.|The inbound SOAP request contains an invalid signature. The SOAP request changed after being signed.|
|Failed to extract principal\(s\) from request.|The SOAP request has either been tampered or was not well formed. ServiceNow cannot extract credentials to authenticate the request.|
|Failed to authenticate WS-security, unknown type.|The SOAP request contains an unsupported security profile. Resend the request with a supported [security profile type](../concept/c_SOAPWebService.md#WS-Security-profiles): X509 or UsernameToken.|
|Failed to authenticate WS-security.|ServiceNow failed to authenticate against the provided profile credentials. Verify that the SOAP request is using the proper credentials.|

**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

