---
title: Login \(AuthnRequest\) process flow
description: SAML 2.0 specifies a Web Browser SSO Profile that involves exchanging information among an identity provider \(IdP\), a service provider \(SP\), and a principal \(user\) on a web browser.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [SAML 2.0 concepts, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Login \(AuthnRequest\) process flow

SAML 2.0 specifies a Web Browser SSO Profile that involves exchanging information among an identity provider \(IdP\), a service provider \(SP\), and a principal \(user\) on a web browser.

The identity provider can be any SSO service offering SAML authentication services \(for example SSOCircle\). The service provider is always an instance. The message flow begins with a request for a secured resource at the service provider.

## Request the target resource at the SP

The principal requests a target resource at the service provider:

https://instance.service-now.com/

The instance checks the request to see if the SAMLRequest and RelayState URL parameters are present. If they exist, the user has already validated with the IdP and can skip steps 2–6.

## Issue AuthnRequest to Identity Provider

The instance constructs an `AuthnRequest` to be sent to the IdP using the `SAMLRequest` value. The instance also constructs and sends a `RelayState` URL parameter value.

The `RelayState` token is an opaque reference to state information maintained at the service provider. The value of the `SAMLRequest` parameter is the deflated and base64 encoded value of the `<samlp:AuthnRequest>` element:

```
<samlp:AuthnRequest    xmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol"    xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion"    ID="identifier_1"    Version="2.0"    IssueInstant="2004-12-05T09:21:59Z"    AssertionConsumerServiceIndex="0"><saml:Issuer>https://sp.example.com/SAML2</saml:Issuer><samlp:NameIDPolicy      AllowCreate="true"      Format="urn:oasis:names:tc:SAML:2.0:nameid-format:transient"/></samlp:AuthnRequest>
```

The integration then URL-encodes the `<samlp:AuthnRequest>` element and sends it as the `SAMLRequest` URL parameter.

The SSO service processes the `<samlp:AuthnRequest>` element by URL-decoding, base64-decoding and inflating the request, in that order. It then performs a security check. If the user does not have a valid security context, the IdP identifies the user by prompting for login credentials. If the user is already logged in, the IdP simply responds with the `SAMLResponse<tt> and <tt>RelayState` URL parameters \(see step 3\).

## Respond with an SAMLResponse and RelayState

After collecting the required login credentials, the SSO service validates the request and responds with a document containing an XHTML form:

```
<formmethod="post"action="https://instance.service-now.com/navpage.do" ...><input type="hidden" name="SAMLResponse" value="response ..." /><input type="hidden" name="RelayState" value="token ..." />
    ...
    <input type="submit" value="Submit" /></form>
```

The value of the `RelayState` parameter comes from this step. The value of the `SAMLResponse` parameter is the base64 encoding of the following `<samlp:Response>` element:

```
<samlp:Responsexmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol"  ID="s2cdc74f37f923e26fe1aeec42b70a93d24230334f"  InResponseTo="90AA6073F01567BFB0DF194F596314E2"  Version="2.0"  IssueInstant="2010-04-29T23:21:51Z"  Destination="https://dloomac.service-now.com/navpage.do"><saml:Issuer xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion">http://idp.ssocircle.com</saml:Issuer><samlp:Status xmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol"><samlp:StatusCode xmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol"       Value="urn:oasis:names:tc:SAML:2.0:status:Success"></samlp:StatusCode></samlp:Status><saml:Assertion xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion"    ID="s23e536bfc51b8487d4d3299dec162d9c2e338823b"    IssueInstant="2010-04-29T23:21:51Z"    Version="2.0"><saml:Issuer>http://idp.ssocircle.com</saml:Issuer><Signature xmlns="http://www.w3.org/2000/09/xmldsig#">
 
...
      </Signature><saml:Subject><saml:NameID Format="urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress"            NameQualifier="http://idp.ssocircle.com"             SPNameQualifier="https://dloomac.service-now.com/navpage.do">david.loo@service-now.com</saml:NameID><saml:SubjectConfirmation Method="urn:oasis:names:tc:SAML:2.0:cm:bearer"><saml:SubjectConfirmationData              InResponseTo="90AA6073F01567BFB0DF194F596314E2"              NotOnOrAfter="2010-04-29T23:31:51Z"              Recipient="https://dloomac.service-now.com/navpage.do" /></saml:SubjectConfirmation></saml:Subject><saml:Conditions NotBefore="2010-04-29T23:11:51Z"        NotOnOrAfter="2010-04-29T23:31:51Z"><saml:AudienceRestriction><saml:Audience>https://dloomac.service-now.com</saml:Audience></saml:AudienceRestriction></saml:Conditions><saml:AuthnStatement AuthnInstant="2010-04-29T23:21:51Z"        SessionIndex="s2dbf89ab99001e0e8cdaed67266d9d4b21b968a04"><saml:AuthnContext><saml:AuthnContextClassRef>urn:oasis:names:tc:SAML:2.0:ac:classes:PasswordProtectedTransport</saml:AuthnContextClassRef></saml:AuthnContext></saml:AuthnStatement></saml:Assertion></samlp:Response>
```

## Validate SAMLResponse

The `SAMLResponse` value is base64 decoded and inflated to reveal the XML document in step 3. The login script extracts the XML value from the `//Subject/NameID` element and uses it to look up an existing user in the User table.

The login script also extracts the session ID from the `//AuthnStatement/@SessionIndex` element and stores it for the `LogoutRequest`.

