---
title: Enable updated version of MultiSSO plugin \[Updated in Security Center 1.3 and 1.5\]
description: Verify that you're using v2 of the MultiSSO plugin and that it's set to true to reduce security vulnerabilities.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Enable updated version of MultiSSO plugin \[Updated in Security Center 1.3 and 1.5\]

Verify that you're using v2 of the MultiSSO plugin and that it's set to true to reduce security vulnerabilities.

If the MultiSSO plugin is enabled on your instance, the version should be v2 and the value should be set to **true**. The versions prior to MultiSSOv2, including SAML 1.1 and SAML 2.0 don't follow security standards because they use OpenSAML library versions with known common vulnerabilities and exposures \(CVEs\). If the known CVEs were security threats in outdated OpenSAML libraries, this could enable a bad actor to forge messages and bypass authentication through XML Signature wrapping attacks, impersonating entities, or allowing man-in-the-middle attackers to gain unauthorized access to an instance.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.multissov2\_feature.enabled**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.1
-   CVSS score: Medium
-   Security risk details: Setting the property value to **false** means that you're using previous versions of MultiSSOv2 which uses OpenSAML libraries with security vulnerabilities. This could enable bad actors to forge messages.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0756504](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0756504)

</td></tr></tbody>
</table>**Parent Topic:**[Configuration](sc-configuration.md)

