---
title: Enable relay state in SAML requests to prevent replay attacks
description: Reduce the risk of replay attacks by enabling relay state in SAML requests to help prevent replay attacks.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-02-07"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable relay state in SAML requests to prevent replay attacks

Reduce the risk of replay attacks by enabling relay state in SAML requests to help prevent replay attacks.

Protect against SAML replay attacks using the **glide.authenticate.sso.saml2.enable\_relay\_state\_with\_id** system property. When this property is set to **true**, the relay state parameter contains the sys\_id of a record in the MultiSSO Request Parameters \[multisso\_request\_parameter\] table, which the relay state URL redirects to.

Set the system property **glide.authenticate.sso.saml2.enable\_relay\_state\_with\_id** to **true**. This helps prevent attackers who have gained access to a SAML request from accessing your instance by resubmitting a valid request.

## More information

<table id="table_zyc_nlf_32c"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Technical configuration name

</td><td>

glide.authenticate.sso.saml2.enable\_relay\_state\_with\_id

</td></tr><tr><td>

Plugin applicability

</td><td>

Multi-Provider SSO plugin \(com.snc.integration.sso.multi.installer\)

</td></tr><tr><td>

Security risk

</td><td>

The relay state enabled by this system property helps protect your instance against replay attacks. Enabling the property helps prevent attackers who have gained access to a SAML request from accessing your instance by resubmitting a valid request.

</td></tr><tr><td>

Common Vulnerability Scoring System \(CVSS\) score

</td><td>

3.8

</td></tr><tr><td>

Common Vulnerability Scoring System \(CVSS\) rating

</td><td>

Low

</td></tr><tr><td>

Functional impact

</td><td>

When this property is set to true, the relay state in a SAML request contains the sys\_id of a record in the MultiSSO Request Parameters \[multisso\_request\_parameter\] table, which contains relay state URL to redirect to.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Base system value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Authentication](sc-authentication.md)

