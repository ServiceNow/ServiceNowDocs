---
title: WS-Security reference
description: Support for WS-Security 1.1 in the form of WSS X.509 Token Profile and WSS Username Token Profile is available for incoming SOAP requests.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# WS-Security reference

Support for WS-Security 1.1 in the form of WSS X.509 Token Profile and WSS Username Token Profile is available for incoming SOAP requests.

The configuration to use WS-Security is separate from the requirement to enforce Basic Authentication, and is enforced when the SOAP envelope contains the WS-Security headers.

## WS Security Profiles

The **WS Security Profile** module lists the WS-Security profiles that are currently in effect. The **Order** of the profiles indicates the order of authentication that is checked, all profiles are checked during the incoming SOAP request, when a profile fails authentication, it does not execute the next one in order. The **Bind session** check box indicates which profile to use to assume the session's identity, there can only be one "bound" session.

## WSS X.509 Token Profile

Use the X.509 authentication framework as defined by the Web Services Security: SOAP Message Security specification. An X.509 certificate specifies a binding between a public key and a set of attributes that includes \(at least\) a subject name, issuer name, serial number, and validity interval. An X.509 certificate is used to validate a public key that is used to sign the incoming SOAP message. Upload the certificate in the **Certificate** module and reference it in the **X509 Certificate** field. If this is a bound session, select the user to impersonate when the WS-Security authentication succeeds.

See the following document: [http://www.oasis-open.org/committees/download.php/16785/wss-v1.1-spec-os-x509TokenProfile.pdf](http://www.oasis-open.org/committees/download.php/16785/wss-v1.1-spec-os-x509TokenProfile.pdf)

## WSS Username Token Profile

In addition to specifying the X.509 Token Profile, a UsernameToken can also be supplied in the SOAP request. A UsernameToken is used as a means of identifying the requester by "username", and optionally using a password \(or shared secret, or password equivalent\) to authenticate that identity to the instance. The UsernameToken profile cannot be used independent of the X.509 Token Profile currently.

1.  Authenticate using the Username of the incoming SOAP request to lookup a User by the specified **User field to match UserName** value. The password value in the incoming Username Token is used to authenticate the request. When the **Bind session** option is selected, the user that authenticates successfully is used for the session.
2.  Authenticate using a separate pair of user name / password that is unrelated to users in the User table. When the **Bind session** option is selected, the user that is specified in the **Run as user** field is used for the session.

## Example WS-Security SOAP Envelope Headers

**Note:**

This sample has been formatted with line returns to fit the content into the frame.

```
<SOAP-ENV:Header><wsse:Securityxmlns:wsse = "http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"SOAP-ENV:mustUnderstand = "1" ><wsse:BinarySecurityTokenxmlns:wsu = "http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd"EncodingType = "http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-message-security-1.0#Base64Binary"ValueType = "http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-x509-token-profile-1.0#X509v3"wsu:Id = "CertId-2D914AB929A6719E7F13068829874641"xmlns:wsse = "http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd" >
			MIIEgzCCA2ugAwIBAgILAQAAAAABLOZQMtEwDQYJKoZIhvcNAQ
			EFBQAwQDEXMBUGA1UEChMOQ3liZXJ0cnVzdCBJbmMxJTAjBg
			NVBAMTHEN5YmVydHJ1c3QgU3VyZWNyZWRlbnRpYWwgQ0Ew
			HhcNMTAxMjE0MTgyMjU1WhcNMTECMjE0MTgyMjU1WjB3MQsw
			CQYDVQQGEwJVUzEUMBIGA1UEChMLU2VydmljZS1Ob3cxKDA
			mBgkqhkiG9w0BCQEWGWRhdmlkLmxvb0BzZXJ2aWNlLW5vdy5jb
			20xKDAmBgNVBAMTH1NlcnZpY2UtTm93IFBhcn3uZXIgRGV2ZWx
			vcG1lbnQwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIB
			AQCvtcRIb6zkGnN9uyhtcSDNSIuCW6FgnTbTDUvw2nGlNA9y9iEV
			wTp5TG3eELOOFBCuRLeY5x28lN+cJ72v+zCwi/rZcbEPj8oWyLVA
			OqJThgrzhDabj0vDM/zU8bvAXcw6FoCUDFKkc64WC7Y4HpBdfW4
			JT7FBgDQ3LEudq80Up+TfETiGwrEA3jRgy9fF92TKD7MN3Vkyhz2
			xZLOFiN5HJixl9juNJmLWugqqIG04yZSuCutc1gjCy0U+f0NXKgh0Q
			rRheNpwcqWbbJvLbR9Ybso6l3UAYCQ09hrRnI7VaPvfiueUvuLopap
			o4Kel6iL8aMUAfEUDtkf1AbqRIIQ5AgMBAAGjggFFMIIBQTAfBgNVH
			SMEGDAWgBRJTJILzUojts557p5VM2taRMAClTA7BgNVHR8ENDA
			yMDCgLqAshipodHRwOi8vY3JsLm9tbmlyb290LmNvbS9TdXJlQ3JlZ
			GVudGlhbC5jcmwwHQYDVR0OBBYEFB+OqlvcdiYmq0enW6mgaV
			wZp9eaMA8GA1UdEwEB/wQFMAMCAQAwDgYDVR0PAQH/BAQD
			AgTwMBEGCWCGSAGG+EIBAQQEAwIFoDBJBg3rBgEFBQcBA1Q
			9MDswOQYIKwYBBQUHMAKGLWh0dHA6Ly9jYWNlcnQub21uaXJv
			b3QuY29tL3N1cmVjcmVkZW50aWFsLmNydDAkBgNVHREEHTAbg
			RlkYXZpZC5sb29Ac2VydmljZS1ub3cuY29tMB0GA1UdJQQWMBQG
			CCsGAQUFBwMCBggrBgEFBQcDBDANBgkqhkiG9w0BAQUFAAO
			CAQEAmeoP0Bgtx2JN1ldLnnK6WLEqDk25zaHP5wTxqVlFxzJy1zi6
			A0lk5U0T5LKYjjGWRIOoSeK8iBU0p7Mq4PE8QCETkjYNyuWJd9zm
			7GPCHdOoL18rQHQRsU8pTDHA10zG+i3zdxAMrHl/H673E4myzvU
			DkJnxNAZdw4h4Ba/Y1+VFCWhOm2GwZdXtzklyZaKtMp+31qmf3bG
			OSU34M/dW40pXgfLDqdGD+6YDQPg25aYeCqcNhwg6VlAWG566g
			aWXYxRaVj0qotSDMdaK8b+7Vlo7KhGGaE62v7f44OSekJeBvTfZCR
			7zRSK8N+0qUpqP/n8vgDkmYIE5IQrRE0rEWA==
		</wsse:BinarySecurityToken><ds:Signature xmlns:ds = "http://www.w3.org/2000/09/xmldsig#"Id = "Signature-2" ><ds:SignedInfo xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" ><ds:CanonicalizationMethodAlgorithm = "http://www.w3.org/2001/10/xml-exc-c14n#" xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" /><ds:SignatureMethod Algorithm = "http://www.w3.org/2000/09/xmldsig#rsa-sha1"xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" /><ds:Reference URI = "#Timestamp-1" xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" ><ds:Transforms xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" ><ds:Transform Algorithm = "http://www.w3.org/2001/10/xml-exc-c14n#"xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" /></ds:Transforms><ds:DigestMethod Algorithm = "http://www.w3.org/2000/09/xmldsig#sha1"xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" /><ds:DigestValue xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" >NIS5sizg8wttGL+aWFQ4003TpPg=</ds:DigestValue></ds:Reference><ds:Reference URI = "#id-3" xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" ><ds:Transforms xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" ><ds:Transform Algorithm = "http://www.w3.org/2001/10/xml-exc-c14n#"xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" /></ds:Transforms><ds:DigestMethod Algorithm = "http://www.w3.org/2000/09/xmldsig#sha1"xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" /><ds:DigestValue xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" >/rXB+nhBT5BXtDErIUIBOyhoh8Y=</ds:DigestValue></ds:Reference></ds:SignedInfo><ds:SignatureValue xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" >
				fwjxJRiDNrNxbVsKoHZflsmKlYADldJf0BoN3R2Fx9rjpszFXI2Gp92eXsP+Sl6rmbPXIdKb8lLl
				+dv8upl8WYPrKJP61KeJ0ZsKNDX474NYC2XEzdJcXbZNktmqY0dSmKwJZzi8rJtmGrbOUAaH51GK
				oXV2FLJ0AqILoZMyP/SPWKbOUNUCpssY7vRA+tX8ZmrjTwMUvpOZbo+KInPmwfpZ6n/uarOh5zjL
				NaYJylTCjuuqXDKPZLvDqy48yrsGAWczB901KwLLrE8C+6aPucFrTBytX91vIhaWiLZuba8Nouaz
				vUkjUk7LM5o87MGrSFx3OwxbaOD7/cMtdg2bxA==
                        </ds:SignatureValue><ds:KeyInfo Id = "KeyId-2D914AB929A6719E7F13068829875022"xmlns:ds = "http://www.w3.org/2000/09/xmldsig#" ><wsse:SecurityTokenReferencexmlns:wsu = "http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd"wsu:Id = "STRId-2D914AB929A6719E7F13068829875053"xmlns:wsse = "http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd" ><wsse:Reference URI = "#CertId-2D914AB929A6719E7F13068829874641"ValueType = "http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-x509-token-profile-1.0#X509v3"xmlns:wsse = "http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd" /></wsse:SecurityTokenReference></ds:KeyInfo></ds:Signature><wsu:Timestampxmlns:wsu = "http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd"wsu:Id = "Timestamp-1" ><wsu:Created>2011-05-31T23:03:07.454Z</wsu:Created><wsu:Expires>2011-05-31T23:08:07.454Z</wsu:Expires></wsu:Timestamp><wsse:UsernameToken><wsse:Username>test_user</wsse:Username><wsse:Password>xxxxxx</wsse:Password></wsse:UsernameToken></wsse:Security></SOAP-ENV:Header>
```

**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

