---
title: Use of secure insert multiple operation within import set API \[New in Security Center 1.3\]
description: Use the com.glide.import\_set\_api.insert\_multiple\_optimize property to control whether GlideRecordSecure or GlideRecord is used for the Insert Multiple operation within the Import Set API.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Use of secure insert multiple operation within import set API \[New in Security Center 1.3\]

Use the **com.glide.import\_set\_api.insert\_multiple\_optimize** property to control whether GlideRecordSecure or GlideRecord is used for the Insert Multiple operation within the Import Set API.

If **com.glide.import\_set\_api.insert\_multiple\_optimize** is set to the recommended value of false, then GlideRecordSecure will be used to insert records, and table-level access control lists \(ACLs\) will be evaluated. If this property is set to true, GlideRecord will be used to insert records, and table-level ACLs will not be evaluated; In addition, you must ensure that Import Set API Insert Multiple REST Endpoint ACL \(sys\_id: 3101b770ff2211105cf343d0653bf182\) is active and that users have the role, import\_transformer.

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

boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

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
-   Security risk details: If this property is not set to false, a low-privileged user could insert data into tables outside the scope of their privileged roles.

</td></tr><tr><td>

Revertible behavior

</td><td>

Both safe override and No DB Override.

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

