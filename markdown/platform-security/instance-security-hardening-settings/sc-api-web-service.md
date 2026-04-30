---
title: API and web service
description: The API and Web Service category ensures that applications have appropriate authentication, authorization and session management, validate all input that traverses a trust boundary and include security controls for all API types.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Hardening settings, Platform Security]
---

# API and web service

The API and Web Service category ensures that applications have appropriate authentication, authorization and session management, validate all input that traverses a trust boundary and include security controls for all API types.

Specific controls in this category address input validation by service type such as XDS schema validation for SOAP web services or Denial of Service protection for graphQL APIs.

-   **[Validate SOAP content type \[Updated in Security Center 1.3\]](sc-soap-content-type-checking.md)**  
Use the **glide.soap.require\_content\_type\_xml** property to enable validation of a content type as text/xml and protect against invalid SOAP requests.
-   **[Require authorization for pdf requests \[Updated in Security Center 1.3\]](sc-require-authorization-for-pdf-requests.md)**  
Use the **glide.basicauth.required.pdf** property to designate if incoming PDF requests should require basic authentication.
-   **[Require Authentication on Event Management HTTP Processor \[New in Security Center 1.3, Updated in 1.5, and removed in 2.0\]](sc-require-authentication-on-event-management-http-processor.md)**  
Learn how to establish secure basic authentication for inbound Amazon Simple Notification Service \(SNS\) requests when the Event Management plugin \(**com.glideapp.itom.snac**\) is enabled.
-   **[Require authorization for SOAP requests \[Updated in Security Center 1.3, 1.5, and 2.0\]](sc-soap-request-authorization.md)**  
Use the **glide.basicauth.required.soap** property to designate if incoming SOAP requests should require basic authorization.
-   **[Require authorization for unload requests \[Updated in Security Center 1.3\]](sc-require-authorization-for-unload-requests.md)**  
Use the **glide.basicauth.required.unl** \(useUnloadFormat\) property to designate if incoming unload requests should require basic authentication.
-   **[Require authorization for csv requests \[Updated in Security Center 1.3\]](sc-require-authorization-for-csv-requests.md)**  
Use the **glide.basicauth.required.csv** property to designate if incoming CSV \(Comma-Separated Values\) requests should require basic authentication.
-   **[Require authorization for excel requests \[Updated in Security Center 1.3\]](sc-excel-request-authorization.md)**  
Use the **glide.basicauth.required.excel** property to designate if incoming Excel requests should require basic authentication.
-   **[Require authorization for import requests \[Updated in Security Center 1.3\]](sc-import-request-authorization.md)**  
Use the **glide.basicauth.required.importprocessor** property to designate if incoming import requests should require basic authentication.
-   **[Require authorization for JSONv2 request \[Updated in Security Center 1.3\]](sc-jsonv2-request-authorization.md)**  
Use the **glide.basicauth.required.jsonv2** property to designate if incoming JSONv2 requests should require basic authorization.
-   **[Require authorization for WSDL request \[Updated in Security Center 1.3 and 1.5\]](sc-wsdl-request-authorization.md)**  
Use the **glide.basicauth.required.wsdl** property to designate if incoming WSDL \(Web Services Description Language\) requests should require basic authentication.
-   **[Require authorization for XML requests \[Updated in Security Center 1.3\]](sc-xml-request-authorization.md)**  
Use the **glide.basicauth.required.xml** property to designate if incoming XML requests should require basic authentication.
-   **[Require authorization for XML output requests \[Updated in Security Center 1.3\]](sc-xml-output-authorization.md)**  
Configure this property so that basic authorization is required for all inbound XMLOutputProcessor requests.
-   **[Require Authorization for XSD Requests \[Updated in Security Center 1.3\]](sc-xsd-request-authorization.md)**  
Use the **glide.basicauth.required.xsd** property to designate if incoming XSD \(XML Schema Definition\) requests should require basic authentication.
-   **[Require authorization for script requests \[Updated in Security Center 1.3\]](sc-script-request-authorization.md)**  
Use the **glide.basicauth.required.scriptedprocessor** property to designate if incoming script requests should require basic authentication.
-   **[Require authorization for SCHEMA requests \[Updated in Security Center 1.3\]](sc-schema-request-authorization.md)**  
Use the **glide.basicauth.required.schema** property to require basic authorization for all Inbound Table Schema Processor requests.
-   **[Require authorization for RSS requests \[Updated in Security Center 1.3\]](sc-rss-request-authorization.md)**  
Use the **glide.basicauth.required.rss** property to designate if incoming RSS requests should require basic authentication.
-   **[Require authorization for API requests \[Updated in Security Center 1.3\]](sc-api-request-authorization.md)**  
Use the **glide.basicauth.required.api** property to enhance security for basic authorization for incoming REST requests.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

