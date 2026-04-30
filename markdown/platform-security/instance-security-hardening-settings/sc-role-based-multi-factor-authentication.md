---
title: Activate role based multi-factor authentication \[Updated in Security Center 1.3\]
description: Use the glide.authenticate.multifactor property to enforce role-based multi-factor authentication \(MFA\) for all users assigned to specific roles.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Activate role based multi-factor authentication \[Updated in Security Center 1.3\]

Use the **glide.authenticate.multifactor** property to enforce role-based multi-factor authentication \(MFA\) for all users assigned to specific roles.

Enforce multi-factor authentication based on the roles assigned to the user. If a user has been assigned "admin", "security\_admin" or "user\_admin" roles in the multi-factor roles list, MFA will be enforced.

-   Set this property to **true** to enforce role-based multi-factor authentication for all users assigned to specific roles.
-   Set this property to **false** to disable role-based multi-factor authentication for all users assigned to specific roles.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.authenticate.multifactor**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](sc-authentication.md)|
|Purpose|Enforce role-based multi-factor authentication for all users assigned to specific roles.|
|Type|boolean|
|Recommended value|true|
|Default value|false|
|Security Dependencies|Activate **Role based multi-factor authentication** within the **Multi-factor Criteria table**.|
|Security risk rating|7.2|
|Functional Impact|Enabling this property improves the experience of the user. It acts as an extra layer of protection and security against compromised credentials.|
|Security risk|\(Moderate\) If this property is not enabled, there is a risk of unauthorized access to sensitive data.|
|References|[Configure role-based multi-factor criteria](../../../integrate/authentication/task/mfa-role-criteria.md)|

**Parent Topic:**[Authentication](sc-authentication.md)

