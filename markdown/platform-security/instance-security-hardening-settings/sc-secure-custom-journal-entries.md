---
title: Restrict access to custom journal entries \[Updated in Security Center 1.3 and removed in 2.0\]
description: Use the glide.live\_feed.custom\_journal.acl\_check\_enabled property to respect ACL's on custom journal fields.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict access to custom journal entries \[Updated in Security Center 1.3 and removed in 2.0\]

Use the **glide.live\_feed.custom\_journal.acl\_check\_enabled** property to respect ACL's on custom journal fields.

If **glide.live\_feed.custom\_journal.acl\_check\_enabled** is not set to the recommended value of true, then all users to be able to see all journal entries within the life feed feature. Setting property to true will respect ACL's on custom journal fields which is a good to have feature.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.live\_feed.custom\_journal.acl\_check\_enabled**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Access control](sc-access-control.md)|
|Purpose|To control which users see which journal entries based on ACLs.|
|Recommended value|true|
|Default value|true|
|Configuration type|Boolean.|
|Security risk|\(Moderate\) When set to true, only the custom journal entries which pass ACL will be shown in Live Feed, otherwise, all users will be able to see all journal entries.|

To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Access control](sc-access-control.md)

