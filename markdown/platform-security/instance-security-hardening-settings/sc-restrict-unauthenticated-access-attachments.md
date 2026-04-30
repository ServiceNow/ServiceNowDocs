---
title: Restrict unauthenticated access to attachments
description: Use the glide.image\_provider.security\_enabled property to control the security settings for images. If set to true, images are visible only to authenticated and authorized users. If set to false, images are visible to anyone with a URL to the attachment.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-05-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict unauthenticated access to attachments

Use the **glide.image\_provider.security\_enabled** property to control the security settings for images. If set to **true**, images are visible only to authenticated and authorized users. If set to **false**, images are visible to anyone with a URL to the attachment.

Secure the images on your instance to prevent sensitive information leak. Images on your instance are accessible via urls that end in `.iix`.

Set the **glide.image\_provider.security\_enabled** system property to **true** to prevent access to your images via these URLs.

**Note:**

This property is not honored for images from the attachment table if the origin table is one of:

-   Stationeries \[sysevent\_email\_style\]
-   Welcome Page Sections \[sys\_home\]
-   System Properties \[sys\_properties\]

Restriction should be applied for unauthenticated users as some attachments might contain sensitive information.

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

Purpose

</td><td>

To prevent unauthenticated access of attachment when rendered using the `.iix`format.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Functional impact

</td><td>

No significant impact on the functionality. User experience might be affected a bit because the user who formerly directly accessed .iix must go through authentication.

</td></tr><tr><td>

Security risk

</td><td>

-   Severity Score: 6.5
-   Security Risk Details: Restriction must be applied for unauthenticated users as some attachment might contain sensitive information.

</td></tr><tr><td>

References

</td><td>

[Administering attachments](https://www.servicenow.com/docs/access?context=r_AdministeringAttachments&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

