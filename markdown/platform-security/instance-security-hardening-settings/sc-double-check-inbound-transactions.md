---
title: Double check inbound transactions \[Updated in Security Center 1.3\]
description: Use the glide.security.strict.updates property to enable double-checking of security on inbound transactions during form submission. When you set this property to true, it adds an extra layer of table validation before a form renders in the browser.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Double check inbound transactions \[Updated in Security Center 1.3\]

Use the **glide.security.strict.updates** property to enable double-checking of security on inbound transactions during form submission. When you set this property to **true**, it adds an extra layer of table validation before a form renders in the browser.

Ensure the property **glide.security.strict.updates** exists in the sys\_properties table and is set to true.

## More information

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

|Attribute|Description|
|---------|-----------|
|Property name|**glide.security.strict.updates**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Access control](sc-access-control.md)|
|Purpose|To ensure an added layer of verification of user permissions before presenting the form in the browser.|
|Data type|Boolean|
|Recommended value|true|
|Default value|true|
|Security risk rating|8.1|
|Functional impact|This remediation adds an extra layer of validation to check for user permissions on the target table/page on the instance. As long as the access controls are set appropriately on the customer instance, there should be no impact.|
|Security risk|\(High\) You should always check access request when transactions happen between two zones. This operation checks for permissions when the form is requested and before form rendering happens.|
|References||

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

