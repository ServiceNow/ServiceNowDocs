---
title: Multi-SSO \(SAML 2.0\) errors and fixes
description: A list of common errors and associated fixes for a Multi-SSO \(SAML 2.0\) setup and configuration.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Test the SAML integration, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Multi-SSO \(SAML 2.0\) errors and fixes

A list of common errors and associated fixes for a Multi-SSO \(SAML 2.0\) setup and configuration.

<table id="table_y1c_2l1_qy"><thead><tr><th>

Error in instance logs

</th><th>

Test Connection Message

</th><th>

SAML property

</th><th>

Diagnosis

</th><th>

Fix

</th></tr></thead><tbody><tr><td>

NotAfter: &lt;Thu Jun 05 22:57:44 PDT 2014&gt;.

</td><td>

Ensure that the IDP x509 certificate is present, valid, and active.

</td><td>

N/A

</td><td>

The current certificate or the SAML assertion has expired.

</td><td>

-   Sync the SNC clock with the SAML IdP server clock.
-   Update the SAML 2.0 certificate record.

</td></tr><tr><td>

-   Unable to locate SAML 2.0 certificate.
-   Could not find a digital signature stored in the ServiceNow instance.

</td><td>

Ensure that the IDP x509 certificate is present, valid, and active

</td><td>

The PEM-formatted string should be entered into the PEM Certificate field.

</td><td>

The SAML certificate does not exist. It might be inactive.

</td><td>

Ensure that the correct PEM-formatted certificate is uploaded to the instance.

</td></tr><tr><td>

Certificates do not match. Expect: &lt;certStr&gt;, actual: &lt;inboundCert&gt;.

</td><td>

Ensure that the IDP x509 certificate is present, valid, and active.

</td><td>

N/A

</td><td>

The available certificate in SNC does not match the certificate in assertion. Causes include:-   The certificate is updated on the IdP but not in the ServiceNow instance.
-   The certificate is in the wrong format.

</td><td>

Confirm that the PEM-formatted string in the SAML 2.0 certificate record matches the X509 Certificate in the SAMLResponse for the user IdP.

</td></tr><tr><td>

Failure to check the validity of the certificate.

</td><td>

Ensure that the IDP x509 certificate is present, valid, and active

</td><td>

N/A

</td><td>

The current certificate might have expired.

</td><td>

Update the SAML 2.0 certificate record.

</td></tr><tr><td>

Failure to validate signature profile.

</td><td>

Ensure that the IDP x509 certificate is present, valid, and active.

</td><td>

N/A

</td><td>

The assertion might be signed with a different certificate.

</td><td>

Check if the IdP has the same certificate as the SNC instance.

</td></tr><tr><td>

InResponseTo attribute in SubjectConfirmationData mismatch. Expect: &lt;inResponseTo&gt;, actual: &lt;inResponseTo&gt;.

</td><td>

Subject confirmation validation failed.

</td><td>

N/A

</td><td>

This error appears if either of the following situations occurs:-   The IdP returns a SAMLResponse for a different SAMLRequest
-   A user bookmarks the URL with the SAMLRequest instead of just the instance URL
-   If a null value is expected, the response might be sent to a different node when the instance has multiple nodes.

</td><td>

The IdP admin should confirm that the expected SAMLReponse is being returned. This situation can be a load balancer or infrastructure issue.

</td></tr><tr><td>

SessionIndex value not found: &lt;message&gt;...

</td><td>

SessionIndex not valid.

</td><td>

N/A

</td><td>

The SessionIndex is required in the SNC instance. The IdP returns it in the SAML response to authenticate successfully.

</td><td>

The IdP admin should confirm that the SessionIndex is defined in the SAMLResponse.

</td></tr><tr><td>

No valid SubjectConfirmation found.

</td><td>

Subject confirmation validation failed.

</td><td>

N/A

</td><td>

Conditions could be missing due to an error on the IdP. The StatusCode in the response would contain Responder instead of the expected Success.

</td><td>

Review SAMLResponse to determine if Conditions are included in the SAMLResponse.

 The valid subject confirmation data could be expired or not for the right audience.

</td></tr><tr><td>

Assertion audience mismatch. Expect: &lt;propAudience&gt;, actual: &lt;audienceUri&gt;.

 or

 AudienceRestriction validation failed. No matching audience found.

</td><td>

Ensure that the 'Audience URI' field is set correctly

</td><td>

The audience URI that accepts the SAML2 token. \(Normally, it is your instance URI. For example: `https://demo.service-now.com`.\)

</td><td>

The SNC instance configured audience URI must match the value in the IdP.

</td><td>

Locate &lt;saml2:Audience&gt; in the SAMLResponse in the logs and verify that the value matches the one on the instance.

</td></tr><tr><td>

Assertion issuer is invalid. Expect: &lt;value on instance&gt;, actual: &lt;value returned by IdP&gt;

</td><td>

Assertion issuer is invalid.

</td><td>

The Identity Provider URL that issues the SAML2 security token with user info.

</td><td>

The IdP entity id \(issuer\) does not match the value defined in the SNC instance.

</td><td>

-   Check if IdP or SP is not configured properly.
-   Confirm that the SAML property \(the Identity Provider URL that issues the SAML2 security token with user info\) is set correctly.

</td></tr><tr><td>

Subject is valid in the future. Now: &lt;now&gt;, NotBefore: &lt;notBefore&gt;

 or

 Subject is expired. Now: &lt;now&gt;, NotOnOrAfter: &lt;notOnOrAfter&gt;

</td><td>

Subject validation confirmation failed.

</td><td>

The number in seconds before notBefore constraint, or after notOnOrAfter constraint, to consider still valid.

</td><td>

The IdP clock is not synced with SP clock.

</td><td>

Update the SAML property glide.authenticate.sso.saml2.clockskew to a larger value. The default is 180 seconds. Some cases require a setting of 300 or higher. You may also need to check the time on your IdP server.

</td></tr><tr><td>

Assertion is valid in the future, now: &lt;now&gt;, notBefore: &lt;notBefore&gt;

 or

 Assertion is expired, now: &lt;now&gt;, notOnOrAfter: &lt;notOnOrAfter&gt;

</td><td>

Assertion is invalid.

</td><td>

The number in seconds before notBefore constraint, or after notOnOrAfter constraint, to consider still valid.

</td><td>

IdP clock is not synced with SP clock

</td><td>

Update the SAML property to a larger value. Default of 60 seconds. Some cases require a setting of 300 or higher. You may also need to check the time on your IdP server.

</td></tr></tbody>
</table><table id="table_m5f_13t_wx"><thead><tr><th>

Error or Symptom

</th><th>

Diagnosis

</th><th>

Fix

</th></tr></thead><tbody><tr><td>

Login requests generate an infinite loop between the system and the IdP when High Security is active.

</td><td>

-   Typically the URL endpoint is an error page or logout page.
-   The logout\_redirect.do might create this loop when you define **glide.security.url.whitelist** without adding the IdP host name to the property value.

**Note:** To learn more about this property, see [Enforce URL allowlist check](../../../administer/security-center/reference/sc-enforce-url-allowlist-check.md) in Instance Security Hardening Settings.


</td><td>

Set \(or create\) the system property glide.authenticate.failed\_redirect to redirect failed authentication requests to this URL.

</td></tr><tr><td>

The token used to authenticate the user or the request is signed with the signature algorithm http://www.w3.org/2001/04/xmldsig-more\#rsa-sha256 which is not the expected signature algorithm http://www.w3.org/2000/09/xmldsig\#rsa-sha1.

</td><td>

Check the Alert Context tab for event details.

</td><td>

Navigate to the Advanced tab of the Relying Party Trust configuration dialog and verify that the algorithm is set to SHA-1 and not SHA-256.

</td></tr><tr><td>

The error message `urn:oasis:names:tc:SAML:2.0:status:Requester` appears in your system log \(syslog\) table.

</td><td>

When your IdP \(e.g. ADFS\) responds with a status of `oasis:names:tc:SAML:2.0:status:Requester`, it means the IdP rejected the login because of an issue with the request sent to it. Unfortunately, the SAML response received from the IdP in most cases does not provide further details for the error.

</td><td>

Review the SAML request sent to the IDP, and work with your IDP administrator to update your instance SAML settings to avoid the error. You may need to contact your IDP provider understand the reason for the login failure.

</td></tr></tbody>
</table>