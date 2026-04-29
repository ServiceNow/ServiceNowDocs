---
title: Enable antivirus scan
description: The com.glide.snap.enable\_scan property activates the antivirus scan functionality.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Enable antivirus scan

The **com.glide.snap.enable\_scan** property activates the antivirus scan functionality.

If **com.glide.snap.enable\_scan** isn't set to the recommended value of **true**, then antivirus scanning is disabled.

Set **com.glide.snap.enable\_scan** to the recommended value of **true** to enable antivirus scanning.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.snap.enable\_scan**

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

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.7
-   CVSS rating: High
-   Security risk details: Users may download malicious files leading to desktop and session compromise.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

