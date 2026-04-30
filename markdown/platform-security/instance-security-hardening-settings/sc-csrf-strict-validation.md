---
title: Prevent Users From Accepting Warning To Bypass CSRF Validation \[Updated in Security Center 1.3 and 1.5\]
description: Use the glide.security.csrf.strict.validation.mode property to enable CSRF token strict validation. If the CSRF token doesn't match, it prevents resubmission of the request.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Prevent Users From Accepting Warning To Bypass CSRF Validation \[Updated in Security Center 1.3 and 1.5\]

Use the **glide.security.csrf.strict.validation.mode** property to enable CSRF token strict validation. If the CSRF token doesn't match, it prevents resubmission of the request.

This property prevents users from being able to accept a warning which allows a potentially malicious request to be sent to the instance. This warning appears when a POST request fails due to having a mis-matched anti-CSRF token belonging to one of the victim's other active sessions. If **glide.security.csrf.strict.validation.mode** is not set to the recommended value of true, then an attacker can formulate a CSRF attack utilizing a leaked anti-CSRF token from a different active session belonging to the victim. A POST request to an instance contains an anti-CSRF token within "sysparm\_ck" or "X-UserToken" which matches the user's current session.

If the anti-CSRF token is instead tied to one of the user's other active sessions, the POST request will return a 302 redirection to security\_interceptor.do with a Continue button available to the user when this property is set to false. Clicking this button will re-submit the request to the instance, except it will now having a valid anti-CSRF token. When this property is set to true, the 302 redirection to the security\_interceptor.do page will not display a Continue button and the user will not be allowed to resubmit the request.A successful CSRF attack will allow an attacker to effectively perform any operation that the victim is able to perform.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.security.csrf.strict.validation.mode**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Access control](sc-access-control.md)|
|Purpose|To enforce strict validation of CSRF token, and prevents its reuse.|
|Data type|boolean|
|Recommended value|true|
|Default value|true|
|Security risk rating|\(Medium\) Cross site Request Forgery is a significant security risk that violates the integrity of the instance data. An attacker can launch the CSRF attack on any instance user by abusing the trust of the instance user. With the help of social engineering attacks, a user can submit a malformed request to the instance on behalf of the attacker.|
|Security risk rating|3.7|
|Functional impact|This remediation enables an extra validation step before the instance user submits a write request to the instance. It checks whether the current CSRF token has been used previously. If Yes, it prevents submission of further write requests.|
|Security risk|\(Medium\) Cross site Request Forgery is a significant security risk that violates the integrity of the instance data. An attacker can launch the CSRF attack on any instance user by abusing the trust of the instance user. With the help of social engineering attacks, a user can submit a malformed request to the instance on behalf of the attacker.|

Return to [Configure and upload your customer supplied key](../../key-management-framework/task/upload-customer-supplied-key.md) to upload your wrapped key.

**Parent Topic:**[Access control](sc-access-control.md)

