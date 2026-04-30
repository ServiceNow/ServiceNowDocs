---
title: Set Allowed MIME Child Types \[New in Security Center 2.0\]
description: Learn how to configure the glide.security.mime.type.allowed\_child\_types property to a secure setting so that file types will not pass the Multipurpose Internet Mail Extensions \(MIME\) type checking. This reduces the risk of remote code execution on an uploaded file.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [File and resources, Hardening settings, Platform Security]
---

# Set Allowed MIME Child Types \[New in Security Center 2.0\]

Learn how to configure the **glide.security.mime.type.allowed\_child\_types** property to a secure setting so that file types will not pass the Multipurpose Internet Mail Extensions \(MIME\) type checking. This reduces the risk of remote code execution on an uploaded file.

The **glide.security.mime.type.allowed\_child\_types** property defines the MIME file types that may have a file extension not matching the data within an uploaded file. This allows such file types to bypass MIME type checking. The property accepts a comma-separated list of file type pairs, such as **application/zip=application/java-archive**. In this example, if the property is set to such a value, files with a `.zip` extension that are technically `.jar` files are allowed to pass MIME type checking despite the inconsistency. If not set properly, this bypass can lead to remote code execution of an uploaded file. Therefore, it should always be set to an empty string \(""\) unless a valid use case arises. For instance, if a certain MIME type must be allowed under a different file extension and is valid as per the Tika configuration, then those key-value pairs will be updated as part of this property value.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.mime.type.allowed\_child\_types**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

""

</td></tr><tr><td>

Default value

</td><td>

""

</td></tr><tr><td>

Category

</td><td>

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.6
-   CVSS score: Medium
-   Security risk details: Not setting this property to the secure value could cause files with incorrect configurations to lead to remote code execution of an uploaded file.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Yes, when **glide.security.mime.type.detection.allow\_child\_types** is set to true, the values of this property will be used to validate against the configured list of allowed MIME child types.

</td></tr><tr><td>

Functional impact

</td><td>

To support MIME types whose file extensions do not match the content of the files but are valid according to the Tika sub-type configurations in **tika-mimetypes.xml**.

</td></tr></tbody>
</table>**Parent Topic:**[File and resources](sc-file-resources.md)

