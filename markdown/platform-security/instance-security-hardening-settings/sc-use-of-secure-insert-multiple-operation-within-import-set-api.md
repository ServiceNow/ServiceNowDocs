---
title: Use of secure insert multiple operation within import set API
description: Use the com.glide.import\_set\_api.insert\_multiple\_optimize property to control whether GlideRecordSecure or GlideRecord is used for the Insert Multiple operation within the Import Set API.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Use of secure insert multiple operation within import set API

Use the **com.glide.import\_set\_api.insert\_multiple\_optimize** property to control whether GlideRecordSecure or GlideRecord is used for the Insert Multiple operation within the Import Set API.

The **com.glide.import\_set\_api.insert\_multiple\_optimize** system property controls whether GlideRecordSecure or GlideRecord is used for the Insert Multiple operation within Import Set API.

If this property is set to **false**, then GlideRecordSecure will be used to insert records and Table level ACLs will be evaluated.

If this property is set to **true**, then GlideRecord will be used to insert records and Table level ACLs will not be evaluated.

Ensure that the property **com.glide.import\_set\_api.insert\_multiple\_optimize** is set to **false**.

**Note:** If this property must be set to **true**, then you must ensure that the **Import Set API Insert Multiple** REST Endpoint ACL \(sys\_id: 3101b770ff2211105cf343d0653bf182\) is active and also audit user's who have the **import\_transformer** role.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.import\_set\_api.insert\_multiple\_optimize**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS score: Medium
-   Security risk details: If this property is not set to the recommended value of **false**, then a low privilege user may be able to insert data into tables outside the scope of their privileged roles.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property optimizes the performance of Import Set API by using GlideRecord to save data. When the parameter is set, it requires an integration user to have the import\_transformer role to access the API.

</td></tr><tr><td>

References

</td><td>

[https://developer.servicenow.com/blog.do?p=/post/gliderecord-vs-gliderecordsecure](https://developer.servicenow.com/blog.do?p=/post/gliderecord-vs-gliderecordsecure)

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

