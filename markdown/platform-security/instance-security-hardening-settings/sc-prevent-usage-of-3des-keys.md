---
title: Prevent usage of 3DES keys \[New in Security Center 7.0\]
description: Disable the use of 3DES static keys on your instance with a system property.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Stored cryptography, Hardening settings, Platform Security]
---

# Prevent usage of 3DES keys \[New in Security Center 7.0\]

Disable the use of 3DES static keys on your instance with a system property.

Use the **glide.security.3des.static\_keys\_usable** system property to disable the usage of 3DES static keys on your instance. This property should be set automatically by a scheduled job, the status of which can be checked via the property **glide.security.3des.removal\_job\_status**. In cases where this property isn’t configured to **false**, after the scheduled job runs and the status is `KEYS_DEACTIVATED`, the scheduled job waits until this property is configured to **false** before proceeding with deletion of the 3DES static keys.

Ensure the **glide.security.3des.static\_keys\_usable** exists on the System Properties \[sys\_properties\] table and is set to a value of **false**. Review [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=78789f8347019a50f64de825126d43ad) for further information on 3DES deprecation.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.3des.static\_keys\_usable**

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

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Stored cryptography](sc-stored-cryptography.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5
-   CVSS score: Medium
-   3DES is deprecated, and the use of 3DES and 3DES static keys outside of temporary backwards compatibility isn’t recommended. Continued use may lead to situations of sensitive information disclosure if a user were to obtain access to encrypted data.

</td></tr><tr><td>

Functional impact

</td><td>

When set to **false**, there may be unlikely situations where code and data residing on the instance still relied on by 3DES static keys are now inaccessible.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Stored cryptography](sc-stored-cryptography.md)

