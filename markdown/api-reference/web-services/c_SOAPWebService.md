---
title: SOAP web service
description: Simple Object Access Protocol \(SOAP\) is an XML-based protocol for accessing web services over HTTP.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Inbound, Web services, API implementation, API implementation and reference]
---

# SOAP web service

Simple Object Access Protocol \(SOAP\) is an XML-based protocol for accessing web services over HTTP.

You can use SOAP to access data on your instance. Available SOAP web services are WS-I compliant, as outlined in the WS-I Basic Profile 1.0.

## Web service provider

ServiceNow publishes its underlying table structures and associated data using the following web service methods:

-   [Direct web services](c_DirectWebServices.md): Use a URL query to request a table's WSDL.
-   [SOAP web service import sets](soap-web-service-import-sets.md): Use import tables and transform maps to automate web service requests for tables.
-   [Scripted SOAP web services](c_ScriptedWebServices.md): Use custom JavaScript to execute SOAP web services requests.

**Note:** SOAP messages are sent with the assumption that the recipient is XML compliant. No encoding is applied to a SOAP message. SOAP always decodes responses as UTF-8, the XML encoding header is not used.

## WSDL

All tables and import sets dynamically generate Web Service Definition Language \(WSDL\) XML documents that describe its table schema and available operations.

You can obtain a table's WSDL by issuing a URL call to your instance that contains the name of the table and the **WSDL** parameter. For example:

```
https://myinstance.service-now.com/incident.do?WSDL

```

All dynamically generated and served ServiceNow WSDLs accessible via HTTP are available for use under the terms defined in the Open Source Initiative OSI - Apache License, Version 2.0 license agreement.

## Long-running SOAP request support

The ServiceNow AI Platform supports long-running SOAP requests by preventing socket timeouts due to inactivity of the network connection while the requests are in process.

This functionality improves the efficiency of the ODBC driver when requesting large numbers of records, doing aggregate queries, or using order by expressions that require sorting.

By default, the system provides timeout protection for web services clients provided by ServiceNow such as the ODBC driver and the MID Server. You can add timeout protection to your custom web services with system properties.

## Timeout protection

Web services clients receive a 307-Temporary Redirect to keep long sessions alive and prevent a timeout due to socket inactivity. A 307-Temporary Redirect causes web services clients which support the status code to repeat their last request to the location specified in the HTTP location header. The value of the location header is the same URL that the web services client originally specified. The use of 307-Temporary Redirects is WS-I compliant.

A web service request that exceeds the timeout limit specified in **glide.soap.request\_processing\_timeout** can only receive a 307-Temporary Redirect when all of these conditions are met:

-   The value of **glide.soapprocessor.allow\_long\_running\_threads** is true.
-   The request includes a **redirectSupported=true** URL parameter.
-   The request is session-aware \(supports HTTP cookies\).
-   The number of redirects has not exceeded the value set by **glide.soap.max\_redirects**.

If any of these conditions is not met, the web service client receives a 408 Request Timeout error.

**Note:** To ensure that applications experience a socket timeout rather than a 408 Request Timeout, set the **glide.soap.request\_processing\_timeout** property to a value larger than the shortest socket timeout setting in effect for the connection between the application and the instance \(300 seconds for hosted instances\).

## SOAP web services security

An instance enforces web service security using a combination of basic authentication challenge/response over the HTTPS protocol and system-level access control lists \(ACLs\) using contextual security. Administrators can control what system resources web services users can access by granting them one of the SOAP roles.

## SOAP roles

To use SOAP web services, you must have the appropriate role for the operation you want to perform. Also, you must have any other roles required to access the target tables.

|Role|Description|
|----|-----------|
|soap|Can perform all SOAP operations.|
|soap\_create|Can insert new records.|
|soap\_delete|Can delete existing records.|
|soap\_ecc|Can query, insert, and delete records on the Queues `[ecc_queue]` table.|
|soap\_query|Can query record information.|
|soap\_query\_update|Can query record information and update records.|
|soap\_script|Can run scripts that specify a .do endpoint. This role is required for running scripted web services.|
|soap\_update|Can update records.|
|import\_admin|Can manage all aspects of import sets and imports. Required for access to the Import Set Row \[sys\_import\_set\_row\] table.|
|import\_transformer|Can manage import set transform maps and run transforms. Required for access to the Import Set Row \[sys\_import\_set\_row\] table.|

## Default web services role requirements

By default, a set of processor ACL rules require users to have the soap\_query role to make WSDL, XSD, and XML schema requests.

If you want to change these role requirements, you can deactivate the ACL rules.

![Access controls table.](../image/WebServiceProcessorACLs.png "Web service processor ACLs")

## Basic authentication

To enforce basic authentication for the user associated with the instance for each WSDL or SOAP message request, administrators can set the property `glide.basicauth.required` to **true**.

When enabled, each WSDL and SOAP request must contain an "Authorization" header as specified in the [Basic Authentication](http://www.w3.org/Protocols/HTTP/1.0/draft-ietf-http-spec.html#BasicAA) protocol.

Because web services requests are non-interactive, the **Authorization** header is always required during a request.

**Note:** If configured, basic authentication refers to local credentials or LDAP authentication.

Supplying basic authentication information with every request \(whether or not it is required\) has the added advantage that the user supplied in the basic authentication credentials can be associated web service invocation. For example, when creating an Incident record, the journal field lists the user ID contained in the basic authentication header instead of the default guest user.

## SOAP security policies

The Enhanced Web Service Provider - Common plugin adds the SOAP Security Policies module to the System Web Services application. This module allows administrators to set the following security policies:

-   Enable or disable signing SOAP requests when consuming an external web service
-   Specify the authentication requirements SOAP requests must meet when communicating over WS-Security.

To know more about SOAP access policy, see [SOAP API access policies](https://www.servicenow.com/docs/access?context=soap-api-access-policies&version=australia&pubname=australia-platform-security&ft:locale=en-US).

![The SOAP Security Policies module is selected in the All menu.](../image/SOAPSecurityPolicies.png "SOAP security policies")

## Certificates required for signed SOAP requests

To sign SOAP requests for WS-Security communications, the following certificates are required:

-   X.509 certificate from the requester
-   X.509 CA certificate of the certificate authority who signed the requester's certificate

## SOAP default security policy

Administrators can specify the SOAP security policy an instance uses with the system property `glide.soap.default_security_policy`. The `glide.soap.default_security_policy` system property specifies the name of the SOAP security policy the instance uses when enforcing Web Services-Security \(WSS\) for inbound requests.

|Field|Description|
|-----|-----------|
|Type|String|
|Default value|Default Security Policy|
|Location|[Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Properties \[sys\_properties\] table|

## WS-Security

You can validate signed web services requests using WS-security. Enable WS-Security to:

-   Verify that SOAP messages originate from a known sender
-   Verify that SOAP messages have not been altered in transit

ServiceNow supports [WS-Security 1.1](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=wss) to validate signed web services requests.

**Note:** WS-Security is not used as an encryption mechanism, HTTPS protocol is used to encrypt all communications.

WS-Security is intended to work with basic authentication. When an instance receives a SOAP message, it reviews the basic authentication header to determine if the SOAP user has rights to the instance. It reviews the WS-Security header to determine the validity of the incoming message. Requests affected by attacks, such as a man-in-the-middle attack, have an invalid WS-Security header and are blocked.

## WS-Security profiles

A WS-security profile determines how a web services message is authenticated when WS-security is enabled. The following mechanisms can be used to authenticate web services requests:

|Authentication mechanism|Description|
|------------------------|-----------|
|Certificate verification|Verifies the certificate associated with the request. Verifying the request's certificate requires uploading the requester's certificate and certificate authority.|
|User credentials|Authenticates the web services request by verifying the user credentials associated with the request. This type of authentication can either verify that the request's credentials match an existing user's credentials or that the request's credentials match a user name and password provided in the profile record.|

Specify the authentication mechanism you want to use when you [create a new WS-security profile](../task/t_CreateANewWS-SecurityProfile.md).

The WS-Security Profiles module lists the WS-Security profiles that are currently in effect.

![WS Security Profiles table is populated with X509 and Username record types.](../image/WS-SecurityProfilesModule.png "WS-Security Profiles module")

## WS-Security error logging

The `glide.processor.debug.SOAPProcessor` system property allows error messages about WS-security to be displayed in the transaction log.

The system property `glide.processor.debug.SOAPProcessor` enables \(true\) or disables \(false\) debugging messages for SOAP processing such as certificate and keystore checks.

|Field|Description|
|-----|-----------|
|Type|true \| false|
|Default value|false|
|Location|[Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) to the System Properties \[sys\_properties\] table|

## WSS X.509 Token Profile

Use the X.509 framework for a WSS X.509 security profile. An X.509 certificate is used to validate a public key that is then used to sign the incoming SOAP message. It specifies a binding between a public key and a set of attributes that includes at least the following:

-   subject name
-   issuer name
-   serial number
-   validity interval

Use the [X.509 authentication framework](https://www.oasis-open.org/committees/download.php/16785/wss-v1.1-spec-os-x509TokenProfile.pdf) as defined by the [Web Services Security: SOAP Message Security specification](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=wss).

Upload the certificate and reference it in the **X509 Certificate** field. If a bound session, select the user to impersonate when the WS-Security authentication succeeds.

![WS Security Profile form is populated with a user type, order, and certificate.](../image/WSSX509SecurityProfile.png "WSS X.509 Security Profile")

## WSS UsernameToken Profile

When specifying the X.509 Token Profile, you can also supply a UsernameToken in the SOAP request.

A UsernameToken is used as a means of identifying the requester by "user name", and optionally using a password, shared secret, or password equivalent, to authenticate that identity.

There are two ways to authenticate a UsernameToken.

1.  Authenticate with existing user credentials.

    ![WS Security Profile form is populated with Username type and the profile action set to 'authenticate with user'.](../image/AuthenticateWithExistingServiceNowUserCredentials.png "Authenticate with existing user credentials")

    Use the user name of the incoming SOAP request to look up a user by the specified **User** field to match the **UserName** value. The system uses the password value in the incoming UsernameToken to authenticate the request. When the **Bind session** option is selected, the user that authenticates successfully is used for the session.

2.  Authenticate with specified user credentials.

    ![WS Security Profile form is populated with the username type, user, and profile information.](../image/AuthenticateWithSpecifiedUserCredentials.png "Authenticate with specified user credentials")

    Authenticate using login credentials unrelated to users in the User table. When the **Bind session** option is selected, the user that is specified in the **Run as user** field is used for the session.


**Note:** The [UsernameToken Profile](https://www.oasis-open.org/committees/download.php/16782/wss-v1.1-spec-os-UsernameTokenProfile.pdf) cannot be used independent of the X.509 Token Profile.

## Strict security for web services

By default, basic authentication for web services only determines whether a user is authorized to access the instance with a SOAP connection. Once authorized, any user can access any table published as a web service.

The system property **Enforce strict security on incoming SOAP requests** changes this behavior and requires that users meet [Contextual Security Manager](https://www.servicenow.com/docs/access?context=r_ContextualSecurity&version=australia&pubname=australia-platform-security&ft:locale=en-US) requirements to access instance resources from web services.

With this property enabled, only users that have the proper SOAP role and also meet the ACL conditions the table and operation can perform that operation from a SOAP connection.

## Mutual authentication for web services

Mutual authentication is supported for outbound web services.

## SOAP session management and reporting

A SOAP session is a Glide session established with an instance by any external SOAP client, such as a web services client application, a ServiceNow MID Server, or the ServiceNow ODBC driver. SOAP sessions are included in the list of user sessions at **User Administration** &gt; **Logged in users**. The `?SOAP` URLs identify SOAP sessions.

## SOAP session properties

Certain properties control how SOAP sessions are maintained.

<table id="table_bdx_vly_25"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.soap.invalidate\_session\_timeout

</td><td>

Duration, in seconds, that an active session remains open. After this duration is reached, the instance deactivates the session and reclaims any system resources. If the client sends another request after the timeout duration is reached, the instance establishes a new session.This property accepts values from 5 to 1200 seconds \(20 minutes\).

 -   Type: integer
-   Default value: 60
-   Location: Add to the System Properties `[sys_properties]` table

</td></tr></tbody>
</table>**Note:** To learn more about properties that affect SOAP web services processing, see the following topics in Instance Security Hardening Settings:

-   [Access control \(instance security hardening\)](https://www.servicenow.com/docs/access?context=sc-access-control&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [Basic auth: SOAP requests](https://www.servicenow.com/docs/access?context=sc-soap-request-authorization&version=australia&pubname=australia-platform-security&ft:locale=en-US)

-   **[Scripted SOAP web services](c_ScriptedWebServices.md)**  
Scripted SOAP web services allow a ServiceNow administrator to create custom SOAP web services.
-   **[Direct web services](c_DirectWebServices.md)**  
A direct web service is available for any table in the system if the correct access control list is configured.
-   **[SOAP web service import sets](soap-web-service-import-sets.md)**  
Web service import sets complement direct web services and scripted SOAP web services by providing a web service interface to import sets tables.
-   **[AttachmentCreator SOAP web service](../reference/r_AttachmentCreatorSOAPWebService.md)**  
Attach documents to records in ServiceNow by sending a SOAP message targeting the ecc\_queue table.
-   **[Override a SOAP endpoint](c_OverridingTheSOAPEndpoint.md)**  
The SOAP endpoint address where the SOAP message is posted is consistent with the endpoint of the WSDL.
-   **[Enable HTTP compression](c_EnablingHTTPCompression.md)**  
By default, the SOAP request is accepted un-compressed and the result of the request is returned un-compressed.
-   **[Prevent empty elements in SOAP messages](c_PreventEmptyElementSOAPMsgs.md)**  
By default, an instance does not omit empty elements, elements with NULL or NIL values, from SOAP messages.
-   **[Insert related records using SOAP](../task/t_InsertRelatedRecordsUsingSOAP.md)**  
Support is available for inserting hierarchical data into tables or web service import set tables. The hierarchical data in the Insert API is automatically mapped to related records of the targeted table.
-   **[Specify requirement for signed SOAP requests](../task/t_SpecifyReqForSignedSOAPRequests.md)**  
Use a SOAP security policy to specify whether the instance requires signed SOAP requests for all inbound SOAP traffic.
-   **[Activate the Enhanced Web Service Provider - Common plugin](../task/t_ActivateEnhancedWSPPlugin.md)**  
Administrators can activate the Enhanced Web Service Provider - Common plugin to enable unsigned WS-Security requests and specify what authentication requirements SOAP requests have.
-   **[Configure SOAP security](../task/t_ConfigureSOAPSecurity.md)**  
Administrators can configure web service security for inbound SOAP requests made to the ServiceNow instance.
-   **[Set the SOAP default security policy](../task/t_SetTheSOAPDefaultSecurityPolicy.md)**  
Set the SOAP default security policy.
-   **[Create a new security policy](../task/t_CreateANewSecurityPolicy.md)**  
Administrators can specify which security profiles WS-Security communications must meet by creating a new security policy.
-   **[Create a new WS-Security profile](../task/t_CreateANewWS-SecurityProfile.md)**  
Create a new WS Security profile to define how to authenticate a web services message when WS-Security is enabled.
-   **[Enforce strict security for inbound SOAP](../task/t_EnforceStrictSecurityWebSvcConns.md)**  
Strict security for web services requires that users meet Contextual Security requirements to access instance resources.
-   **[Enable WS-Security verification](../task/t_EnableWS-SecurityVerification.md)**  
Administrators can enable Web Services Security \(WSS\) verification from the Web Services system properties.
-   **[Debug incoming SOAP envelope](c_DebuggingIncomingSOAPEnvelope.md)**  
To capture incoming SOAP envelope XML in the system log, add the property **glide.processor.debug.SOAPProcessor** with a value of **true**.
-   **[View a SOAP session log](../task/t_ViewingASOAPSessionReport.md)**  
You can view a user's log from a SOAP session.
-   **[Basic authentication code samples](../reference/r_BasicAuthenticationExamples.md)**  
Samples of basic authentication code for several programming languages and versions.
-   **[Example: WS-Security SOAP envelope header](../reference/r_SmplWSSecSOAPEnvHeader.md)**  
An example of a valid WS-Security SOAP envelope header.
-   **[WS-Security properties](../reference/ws-security-properties.md)**  
These properties control the behavior of WS-Security X.509 tokens.
-   **[WS-Security error messages](../reference/r_WS-SecurityErrorMessages.md)**  
An instances produces one of the following error messages when it encounters an issue with a WS-security SOAP message.
-   **[WS-Security reference](../reference/ws-security-reference.md)**  
Support for WS-Security 1.1 in the form of WSS X.509 Token Profile and WSS Username Token Profile is available for incoming SOAP requests.
-   **[Long-running SOAP request properties](../reference/LongRunningSOAPRequestProps.md)**  
The following properties are available for long-running SOAP requests.
-   **[Retrieve a large number of records using SOAP](../../examples/concept/c_RtvLrgNmbrRcrdSOAP.md)**  
By default, a single SOAP request can retrieve a maximum of 250 records.

**Parent Topic:**[Inbound web services](../../web-services/concept/inbound-web-services.md)

