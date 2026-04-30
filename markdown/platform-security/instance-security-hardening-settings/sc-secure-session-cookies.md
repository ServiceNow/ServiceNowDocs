---
title: Enforce strict security of session cookies \[Updated in Security Center 1.3\]
description: Use the glide.ui.secure\_cookies property to require properly formatted cookies
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enforce strict security of session cookies \[Updated in Security Center 1.3\]

Use the **glide.ui.secure\_cookies** property to require properly formatted cookies

When you set the property is to true, your instance will reject a session if the associated cookie is not in the expected format.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.ui.secure\_cookies**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Validation, sanitization, and encoding](validation-sanitization-encoding.md)|
|Purpose|To achieve more secure session authentication.|
|Recommended value|true|
|Default value|true|
|Security risk rating|8.8|
|Functional impact|When the property is set to true, improperly formatted cookies are rejected. When such a cookie is rejected, the user must login again.|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

