---
title: Enable policy based session access for mobile \[New in Security Center 1.5\]
description: Use the The Zero Trust- Policy Based Session Access plugin to control if users authenticating through a mobile app will have their roles reduced.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable policy based session access for mobile \[New in Security Center 1.5\]

Use the The Zero Trust- Policy Based Session Access plugin to control if users authenticating through a mobile app will have their roles reduced.

The Zero Trust- Policy Based Session Access plugin enables security admins to reduce user access in a session based on parameters such as IP address, location, identify provider attributes, and user attributes with adaptive authentication policies. When this plugin is enabled or set to true, users authenticating through a mobile device will have their roles restricted according to the plugin's policies. Instance admins may wish to restrict high privileged access when users authenticate through a mobile device as it could indicate an unsafe environment for sensitive operations.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.session\_access.mobile.enabled**

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

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.7
-   CVSS score: Medium
-   Security risk details: If this hardening setting is set to true, then policy based session access is enforced on the instance for mobile logins, and users that are not coming from a trusted environment, or are not using trusted devices will have their roles with reduced privileges. True is the secure setting. If this setting is configured to false, then policy based session access is disabled, and users will continue to have full roles including the high privileged roles like admin all the time.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

If admin has configured the session access policy on the instance, then users will have their roles reduced after mobile login if they are not coming from a trusted environment or using a trusted device.

</td></tr><tr><td>

References

</td><td>

[Adaptive authentication](../../../integrate/authentication/concept/adaptive-authentication.md)

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

