---
title: Validate file mime type in AttachmentCreator soap web service \[New in Security Center 1.3 and updated in 1.5\]
description: The glide.attachment.enforce\_security\_validation property determines whether Multipurpose internet Mail Extensions \(MIME\) files undergo validation.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Validate file mime type in AttachmentCreator soap web service \[New in Security Center 1.3 and updated in 1.5\]

The **glide.attachment.enforce\_security\_validation** property determines whether Multipurpose internet Mail Extensions \(MIME\) files undergo validation.

If **glide.attachment.enforce\_security\_validation** is not set to the recommended value of **true**, then there is no validation for MIME files, enabling malicious files to be uploaded with incorrect file extensions. When this property is set to **true**, files are uploaded with the correct file type extension.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.attachment.enforce\_security\_validation**

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

Category

</td><td>

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS score: High
-   Security risk details: If the property is set to false, there’s no validation for MIME files during uploads. This could enable malicious files to be disguised by changing their file extension.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics\_of\_HTTP/MIME\_types/Common\_types](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types/Common_types)

</td></tr><tr><td>

Functional impact

</td><td>

Set this hardening setting to true to run mime-type and file extension validations on uploaded file attachments. No validations are run if this property is set to false. This property is set to true by default.

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

