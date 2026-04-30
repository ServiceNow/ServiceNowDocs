---
title: Enable HTML Sanitizer within Virtual Agent \[Updated in Security Center 1.3 and 1.5\]
description: Use the com.glide.cs.html.sanitizer.enabled property to enable HTMLSanitizerService.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enable HTML Sanitizer within Virtual Agent \[Updated in Security Center 1.3 and 1.5\]

Use the **com.glide.cs.html.sanitizer.enabled** property to enable HTMLSanitizerService.

This property controls the whether the HtmlSanitizerService is enabled. If **com.glide.cs.html.sanitizer.enabled** is not set to true, then a Stored Cross-Site Scripting \(XSS\) attack is possible in the VA web client.

## More information

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

|Attribute|Description|
|---------|-----------|
|Property name|**com.glide.cs.html.sanitizer.enabled**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Validation, sanitization, and encoding](validation-sanitization-encoding.md)|
|Purpose|Prevents application against cross site scripting and HTML injection attacks.|
|Recommended value|true|
|Default value|true|
|Security risk rating|8|
|Functional Impact|This remediation enforces HTML-output encoding mechanism before the user data is rendered back to the user. If customer has any customization that involves rendering of the HTML attribute or content data, then there is a functionality impact.|
|Security risk|\(High\) User input should be securely treated when the data is being stored and processed on the application. This reduces client-side cross-site scripting attacks by output encoding the data.|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

