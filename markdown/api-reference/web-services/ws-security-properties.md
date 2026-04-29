---
title: WS-Security properties
description: These properties control the behavior of WS-Security X.509 tokens.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# WS-Security properties

These properties control the behavior of WS-Security X.509 tokens.

<table id="table_thq_3vj_wy"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.soap.msg\_digest.algorithm

</td><td>

Specifies the method digest algorithm. Possible values are SHA-1, SHA-256, and SHA-512.

-   Type: String
-   Default value: SHA-1
-   Location: Add to the System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.soap.signature.algorithm

</td><td>

Specifies the signature algorithm. Possible values are RSA-SHA-1, RSA-SHA-256, and RSA-SHA-512.-   Type: String
-   Default value: RSA-SHA-1
-   Location: Add to the System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.soap.canonical.algorithm

</td><td>

Specifies the cannonicalization algorithm. Possible values are Canonical xml 1.0, Canonical xml 1.0 with Comments, Exclusive Canonical xml 1.0, and Exclusive Canonical xml 1.0 with Comments.-   Type: String
-   Default value: Exclusive Canonical xml 1.0
-   Location: Add to the System Property \[sys\_properties\] table

</td></tr></tbody>
</table>Each possible value for these properties represents a standard WS-Security algorithm.

|Value|Algorithm|
|-----|---------|
|Method digest algorithms|
|SHA-1|http://www.w3.org/2000/09/xmldsig\#sha1|
|SHA-256|http://www.w3.org/2001/04/xmlenc\#sha256|
|SHA-512|http://www.w3.org/2001/04/xmlenc\#sha512|
|Signature algorithms|
|RSA-SHA-1|http://www.w3.org/2000/09/xmldsig\#rsa-sha1|
|RSA-SHA-256|http://www.w3.org/2001/04/xmldsig-more\#rsa-sha256|
|RSA-SHA-512|http://www.w3.org/2001/04/xmldsig-more\#rsa-sha512|
|Cannonicalization algorithms|
|Canonical xml 1.0|http://www.w3.org/TR/2001/REC-xml-c14n-20010315|
|Canonical xml 1.0 with Comments|http://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments|
|Exclusive Canonical xml 1.0|http://www.w3.org/2001/10/xml-exc-c14n\#|
|Exclusive Canonical xml 1.0 with comments|http://www.w3.org/2001/10/xml-exc-c14n\#WithComments|

**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

