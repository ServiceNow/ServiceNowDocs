---
title: Enable ACLs to Control Live Profile Details \[Updated in Security Center 1.3\]
description: Use the glide.live\_profile.details property to designate whether a user should be able to view all detail fields, such as company name and phone numbers, in a live profile.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable ACLs to Control Live Profile Details \[Updated in Security Center 1.3\]

Use the **glide.live\_profile.details** property to designate whether a user should be able to view all detail fields, such as company name and phone numbers, in a live profile.

Depending on the setting of the **glide.live\_profile.details** property, the following occur:

-   If the value is set to Show, access to the live profile information is granted, regardless of the ACLs created for the user profile.
-   If the value is set to ACL, access to the live profile information is restricted, as per the ACLs created for the user profile.
-   If the value is set to Hide, access to the live profile information is restricted, regardless of the ACLs created for the user profile.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.live\_profile.details**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Access control](sc-access-control.md)|
|Purpose|The purpose is to enable only authorized users to access the details of a Live Profile \(such as Company name, Phone numbers\)|
|Data type|choicelist|
|Recommended value|ACL|
|Default value|ACL|
|Security risk rating|4.3|
|Functional impact|If property is not enabled, unauthorized users can access the Live profile details of all other users.|
|Security risk|\(Moderate\) API requests should always honor table ACLs. Restriction must be applied to prevent unauthorized users accessing details of a Live Profile.|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

