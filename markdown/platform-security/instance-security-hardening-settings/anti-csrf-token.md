---
title: Anti-CSRF token \(instance security hardening\)
description: Use the glide.security.use\_csrf\_token property to ensure the use of a secure token to identify and validates incoming requests, which in turn are used to prevent these attacks.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Anti-CSRF token \(instance security hardening\)

Use the **glide.security.use\_csrf\_token** property to ensure the use of a secure token to identify and validates incoming requests, which in turn are used to prevent these attacks.

Cross-Site Request Forgery \(CSRF\) is an attack that forces an end user to execute unwanted actions on a web application in which they're currently authenticated. CSRF attacks specifically target state-changing requests, not theft of data, since the attacker has no way to see the response to the forged request.

**Note:** By default, the **glide.security.use\_csrf\_token** property is set to `true` for zBoot instance.

The following properties can be enabled for added controls over CSRF token:

-   **glide.security.csrf\_previous.time\_limit**
-   **glide.security.csrf\_previous.allow**
-   **glide.security.csrf.strict.validation.mode**

## More information

|Attribute|Description|
|---------|-----------|
|Property name|glide.security.use\_csrf\_token|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Configure in Instance Security Center|Yes|
|Purpose|To protect the application from potential CSRF attack.|
|Recommended value|true|
|Functional impact|\(Low\) This remediation enables an extra validation step before the instance user submits a write request to the instance. Every write request contains a CSRF token \(i.e a validation/CSRF ID tied to the user session\). When the user session expires, the secure token expires with it.|
|Security risk|\(High\) Cross Site Request Forgery is a significant security risk that violates the integrity of the instance data. An attacker can launch the CSRF attack by abusing the trust of an instance user. With the help of social engineering attacks, a user can submit a malformed request on behalf of the attacker on the instance.|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](../../security-center/reference/sc-authentication.md)

