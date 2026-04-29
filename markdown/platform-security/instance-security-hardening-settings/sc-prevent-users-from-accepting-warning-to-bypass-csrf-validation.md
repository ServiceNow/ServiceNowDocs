---
title: Prevent users from accepting warning to bypass CSRF validation
description: Reduce the risk of Cross-Site Request Forgery \(CSRF\) by preventing users from accepting warning to bypass CSRF validation.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Prevent users from accepting warning to bypass CSRF validation

Reduce the risk of Cross-Site Request Forgery \(CSRF\) by preventing users from accepting warning to bypass CSRF validation.

The **glide.security.csrf.strict.validation.mode** system property prevents users from being able to accept a warning, which allows a potentially malicious request to be sent to the instance. This warning appears when a POST request fails due to having a mismatched anti-CSRF token belonging to one of the victim's other active sessions. If **glide.security.csrf.strict.validation.mode** isn't set to the recommended value of **true**, then an attacker can formulate a CSRF attack utilizing a leaked anti-CSRF token from a different active session belonging to the victim.

A POST request to an instance contains an anti-CSRF token within "sysparm\_ck" or "X-UserToken" which matches the user's current session. If the anti-CSRF token is instead tied to one of the user's other active sessions, the POST request will return a 302 redirection to security\_interceptor.do with a **Continue** button available to the user when this property is set to **false**.

Clicking this button will re-submit the request to the instance, except it will now having a valid anti-CSRF token. When this property is set to **true**, the 302 redirection to the security\_interceptor.do page will not display a **Continue** button and the user isn't allowed to resubmit the request.

Ensure that the property **glide.security.csrf.strict.validation.mode** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.csrf.strict.validation.mode**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

 

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS rating: Low
-   Security risk details: A successful CSRF attack will allow an attacker to effectively perform any operation that the victim is able to perform.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

