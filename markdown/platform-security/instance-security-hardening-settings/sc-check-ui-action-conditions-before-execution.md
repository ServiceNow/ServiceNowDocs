---
title: Check UI action conditions before execution
description: Use the glide.security.strict.actions property to enable checking of UI actions conditions in forms and lists before they execute. When you set this property to true, it adds an extra layer of validation on the table UI actions before they are executed.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Check UI action conditions before execution

Use the **glide.security.strict.actions** property to enable checking of UI actions conditions in forms and lists before they execute. When you set this property to true, it adds an extra layer of validation on the table UI actions before they are executed.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.security.strict.actions**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Access control](sc-access-control.md)|
|Purpose|To ensure an extra layer of validation on the table UI actions before they are executed.|
|Data type|boolean|
|Recommended value|true|
|Default value|true|
|Security risk rating|3.3|
|Functional impact|This remediation only adds an extra layer of validation to check for UI actions on the target table/page on the instance. As long as the access controls are set appropriately on the customer instance, there should not be an impact here.|
|Security risk|\(Low\) Access request is always checked when transactions happen between two zones. This operation validates any UI actions before the form renders for the end user.|
|References|High security plugin|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

