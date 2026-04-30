---
title: Enforce HTML Sanitization \[Updated in Security Center 1.3\]
description: Use the com.glide.security.check\_unsanitized\_html property to enforce sanitization behavior of translated\_html fields on a global level for field assignments.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Enforce HTML Sanitization \[Updated in Security Center 1.3\]

Use the **com.glide.security.check\_unsanitized\_html** property to enforce sanitization behavior of translated\_html fields on a global level for field assignments.

HTML is one of the types that can be assigned to the dictionary fields. Assigning HTML fields to any field type provides the functionality to format content using HTML tags \(for example, `<p>`, `<a href>`, `<b>`, `<font>`, `<img>`\). To prevent malicious activity, certain HTML tags can be disallowed using a block list. This property will prevent disallowed tags from being used in translated\_html fields on your instance.

-   Set this property to **enforce** to enforce sanitization behavior of translated\_html fields.
-   Set property to **disable** to turn off the html sanitization to allow blocked html tags on translated\_html fields.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**com.glide.security.check\_unsanitized\_html**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Validation, sanitization, and encoding](validation-sanitization-encoding.md)|
|Purpose|Prevents the use of insecure HTML tags to protect against attacks such as cross-site scripting.|
|Type|String|
|Recommended value|enforce|
|Default value|enforce|
|Security risk rating|7.3|
|Functional impact|This remediation enforces HTML sanitization to occur on the UI and renders translated html fields to the user. It can have an impact on readability and formatting.|
|Security risk|\(High\) Input validation must occur on the application to defend against cross-site scripting attacks. These attacks enable foreign scripts to execute on user sessions in the logged in browser's context. Attackers can use it to steal session information and sensitive data.|
|References|[HTML sanitizer](../../security/concept/c_HTMLSanitizer.md)|

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

