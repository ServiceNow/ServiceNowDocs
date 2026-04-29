---
title: Enforce Strict User Image Upload
description: Use the glide.security.strict.user\_image\_upload property to enable Access Control for the upload/update of a profile picture when performed on a user record.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce Strict User Image Upload

Use the **glide.security.strict.user\_image\_upload** property to enable Access Control for the upload/update of a profile picture when performed on a user record.

If the **glide.security.strict.user\_image\_upload** system property isn't set to the recommended value of **true**, then ACLs aren't enforced on image uploads to the Photo field. When the property is set to **true**, the table ACLs are enforced when uploading photos, only allowing authorized users to upload an image.

Ensure that the property **glide.security.strict.user\_image\_upload** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.strict.user\_image\_upload**

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

true

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS rating: Low
-   Security risk details: An unauthorized user may upload an image to another user's profile.

</td></tr><tr><td>

Functional impact

</td><td>

No functionality impact as authorized users are still able to upload images to their user profile.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

