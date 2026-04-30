---
title: Restrict uploaded MIME types \[Updated in Security Center 1.3 and 2.0\]
description: Use the glide.security.file.mime\_type.validation property to activate MIME type checking for uploads. You can enable \(set the property to true\) or disable \(set it to false\) MIME type validation for file attachments.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Restrict uploaded MIME types \[Updated in Security Center 1.3 and 2.0\]

Use the **glide.security.file.mime\_type.validation** property to activate MIME type checking for uploads. You can enable \(set the property to **true**\) or disable \(set it to **false**\) MIME type validation for file attachments.

## Prerequisites

Before setting this property, set the **glide.attachment.extensions** property. Only those extensions specified in **glide.attachment.extensions** are checked for MIME type during upload. To learn more, see [Restrict file extensions](https://www.servicenow.com/docs/access?context=restrict-file-extensions&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Ensure the Glide Property **glide.ui.jelly.js\_interpolation.protect\_nested\_expressions** exists and is set to the value true. If the property does not appear in the sys\_properties table, add a new record.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.security.file.mime\_type.validation**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Validation, sanitization, and encoding](validation-sanitization-encoding.md)|
|Purpose|To enforce checking of MIME type / magic bytes during file uploads.|
|Recommended value|true|
|Default value|true|
|Security risk rating|5.4|
|Functional Impact|This remediation enables MIME type verification on the attachments to the application. No functionality impact, unless there is a malicious intent in uploading the files as this validation is merely checking for mis-sync between the MIME type and the data.|
|Security risk|\(Medium\) To reduce vulnerabilities such as file inclusion and malicious file uploads, MIME type verification should be enabled.|
|References|[Administering attachments](https://www.servicenow.com/docs/access?context=r_AdministeringAttachments&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)|

See  for details on configuring properties for hardening.

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

