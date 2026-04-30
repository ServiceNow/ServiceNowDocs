---
title: Enable a deny-list password validation check
description: Manage the deny-list passwords in the Excluded Password table.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable a deny-list password validation check

Manage the deny-list passwords in the Excluded Password table.

Use the **glide.enable.blacklist\_password** property to monitor deny-list passwords. When the property is set to **True**, the user's password is checked against a list of the deny-list passwords to prevent them from using a password from a set of breached passwords. The administrator can maintain the list by inserting passwords into the Excluded Password table.

## More information

|Attribute|Description|
|---------|-----------|
|Configuration name|**glide.enable.blacklist\_password**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Data type|boolean|
|Recommended value|true|
|Default value|false|
|Category|[Authentication](sc-authentication.md)|
|Dependencies and prerequisites|None|
|References|[Excluding passwords through password policies on your instance](../../../integrate/authentication/task/blacklist-passwords.md)|

**Parent Topic:**[Authentication](sc-authentication.md)

