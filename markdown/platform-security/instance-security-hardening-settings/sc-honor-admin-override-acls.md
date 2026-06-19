---
title: Honor Admin Override ACLs
description: The glide.security.admin.override.accessterm property controls admins to be unable to override ACL evaluation even where the override should be in effect.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-honor-admin-override-acls.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Honor Admin Override ACLs

The **glide.security.admin.override.accessterm** property controls admins to be unable to override ACL evaluation even where the override should be in effect.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.security.admin.override.accessterm**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-access-control.md)|
|Purpose|Controls admins to be unable to override ACL evaluation.|
|Data type|Boolean|
|Recommended value|True|
|Default value|True|
|Security risk|\(Low\) ACLs are evaluated cumulatively. If there are number of ACLs on any given field and the Admin Overrides option is false \(not selected\) on one of them, then the effective admin overrides for all the ACLs are considered to be false.|
|Security risk rating|3.8|
|References|[Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/access-control/access-control-rules.md)|

To learn more about adding or creating a system property, see .

**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-access-control.md)

