---
title: Enable scoped admin application ACLs \[Updated in Security Center 1.3\]
description: The glide.security.scoped\_administration.honor\_global\_acl determines whether an application administration app can inherit global access control list \(ACL\) rules.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable scoped admin application ACLs \[Updated in Security Center 1.3\]

The **glide.security.scoped\_administration.honor\_global\_acl** determines whether an application administration app can inherit global access control list \(ACL\) rules.

This property is especially useful when there are no scoped admin application ACLs defined for the record scope.

Set **glide.security.scoped\_administration.honor\_global\_acl** to true to prevent a low privileged user with permissions to the application to potentially access sensitive records.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.security.scoped\_administration.honor\_global\_acl**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Access control](sc-access-control.md)|
|Purpose|Controls ACL access rule in scoped admin application.|
|Recommended value|True|
|Default value|True|
|Configuration type|Boolean|
|Security risk|\(Low\) When the property value is true and there are no scoped admin application ACLs defined for the record scope, the global ACLs will be honored. If set to false, with no scoped admin application ACLs defined for the record scope, ACL checks will be ignored.|
|Security risk rating|3.8|
|References|[Access control rules in application administration apps](https://www.servicenow.com/docs/access?context=ACL-access-checks&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|

To learn more about activating a plugin, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

**Parent Topic:**[Access control](sc-access-control.md)

