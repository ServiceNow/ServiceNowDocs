---
title: Disallow infected file download \[Updated in Security Center 1.5 and 2.0\]
description: Control whether users can download non-scanned attachments if the antivirus service is down or unreachable.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Disallow infected file download \[Updated in Security Center 1.5 and 2.0\]

Control whether users can download non-scanned attachments if the antivirus service is down or unreachable.

When the **com.glide.snap.infected\_download\_allowed** property is set to true, users can still download non-scanned attachments in the event that the antivirus service is down or unreachable. This situation potentially exposes users to the risk of downloading a malicious file, thereby risking the infection of their desktop, especially if there is no other endpoint protection installed on the device.

Ensure the property **com.glide.snap.infected\_download\_allowed** is set to false.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.snap.infected\_download\_allowed**

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

false

</td></tr><tr><td>

Category

</td><td>

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.7
-   CVSS score: Medium
-   Security risk details: Not setting this property to the recommended value of false could expose your instance to downloading malicious files.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

