---
title: Enforce oauth state parameter validation
description: Configure the glide.oauth.state.parameter.required property to prevent your instance from cross-site request forgery \(CSRF\) attacks.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce oauth state parameter validation

Configure the **glide.oauth.state.parameter.required** property to prevent your instance from cross-site request forgery \(CSRF\) attacks.

The **glide.oauth.state.parameter.required** system property enables the **State** parameter to be required in an OAuth request for authorization code flow. Beginning in the Madrid release, the system property **glide.oauth.state.parameter.required** adds a **State** parameter for an OAuth request. For zbooted instances, the property is **true**. For upgraded instances, the property is not present, so the **State** parameter is not enabled. The **State** parameter is a string value, and should not contain special characters. The State parameter cannot be empty or " ". Not setting the **State** parameter to **true** ensures that an attacker cannot perform CSRF attacks during authentication can allow an attacker to perform operations as the victim.

Ensure that the property **glide.oauth.state.parameter.required** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.oauth.state.parameter.required**

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS rating: Medium
-   Security risk details: Not enabling the **glide.oauth.state.parameter.required** property in OAuth authorization code flow increases the risk of Cross-Site Request Forgery \(CSRF\) attacks, potentially allowing attackers to impersonate users and perform unauthorized actions.

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

