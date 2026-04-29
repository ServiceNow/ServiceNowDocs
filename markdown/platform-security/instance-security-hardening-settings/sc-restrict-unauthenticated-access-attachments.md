---
title: Restrict unauthenticated access to attachments
description: Restrict unauthenticated access to image attachments using a system property.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict unauthenticated access to attachments

Restrict unauthenticated access to image attachments using a system property.

Use the **glide.image\_provider.security\_enabled** property restrict unauthenticated access to image attachments. If set to `true`, images are visible to any authenticated user but no unauthenticated user. If set to `false`, images are visible to anyone with a URL to the attachment. Thumbnails of an attached image maintain the same policy as the original attached image and are accessible to the same set of users as the original attached image. When this property is enabled, more fine grained access control for unauthenticated users is obtained through entries in the Security Allow/Deny List Entities \[sys\_security\_restricted\_list\] table and through the declaration of public KB articles for those images attached to KB articles. These exceptions to the default policy for unauthenticated users when this property is `true` are applied in the following order.

**Note:** In these exceptions, "parent table" refers to the table of the original image attachment from which a thumbnail is generated.

1.  If the table of an attached image or parent table of a thumbnail image is deny-listed in the Security Allow/Deny List Entities \[sys\_security\_restricted\_list\] table, access is denied to the image/thumbnail.
2.  If the table of an attached image or parent table of a thumbnail image is allow-listed in the Security Allow/Deny List Entities \[sys\_security\_restricted\_list\] table, access is granted to the image/thumbnail.
3.  If the table of an attached image or parent table of a thumbnail image is included in a public KB article, access is granted to the image/thumbnail.

Ensure that the property **glide.image\_provider.security\_enabled** is set to `true`. If the property does not exist on the System Properties \[sys\_properties\] table, the default value is `false`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.image\_provider.security\_enabled**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Functional impact

</td><td>

If the property was previously `false` and then is set to `true`, unauthenticated users can no longer be able to access image attachments unless explicitly allowed using one of the exclusion procedures.

</td></tr><tr><td>

Security risk

</td><td>

-   Severity Score: 6.5
-   CVSS Rating: Medium
-   Security Risk Details:

If the property is set to `false`, image attachments are visible to anyone authenticated or unauthenticated with a URL to the attachment. This may lead to sensitive information leaks. To avoid these, set the property to `true` and ensure any exceptions to the default policy when the property is `true` are properly configured.


</td></tr><tr><td>

References

</td><td>

[Administering attachments](https://www.servicenow.com/docs/access?context=r_AdministeringAttachments&version=australia&pubname=australia-platform-administration&ft:locale=en-US) [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

