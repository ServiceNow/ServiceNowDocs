---
title: Activate role-based multi-factor authentication \[Updated in Security Center 1.3\]
description: Use the glide.authenticate.multifactor property to enforce role-based multi-factor authentication \(MFA\) for all users assigned to specific roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-activate-role-based-multi-factor-authentication.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Activate role-based multi-factor authentication \[Updated in Security Center 1.3\]

Use the **glide.authenticate.multifactor** property to enforce role-based multi-factor authentication \(MFA\) for all users assigned to specific roles.

Enforce multi-factor authentication based on the roles assigned to the user. If a user has been assigned "admin", "security\_admin" or "user\_admin" roles in the multi-factor roles list, MFA will be enforced.

-   Set this property to **true** to enforce role-based multi-factor authentication for all users assigned to specific roles.
-   Set this property to **false** to disable role-based multi-factor authentication for all users assigned to specific roles.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.authenticate.multifactor**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)|
|Purpose|Enforce role-based multi-factor authentication for all users assigned to specific roles.|
|Type|true/false|
|Recommended value|true|
|Security Dependencies|Activate **Role based multi-factor authentication** within the **Multi-factor Criteria table**.|
|Security risk rating|7.2|
|Functional impact|Enabling this property improves the experience of the user. It acts as an extra layer of protection and security against compromised credentials.|
|Security risk|\(Moderate\) If this property is not enabled, there is a risk of unauthorized access to sensitive data.|
|References|[Configure role-based multi-factor criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/mfa-role-criteria.md)|

To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Parent Topic:**[Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-authentication.md)

