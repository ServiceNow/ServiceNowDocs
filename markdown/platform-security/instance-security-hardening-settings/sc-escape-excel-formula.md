---
title: Escape Excel Formulas \[Updated in Security Center 1.3\]
description: Use the glide.export.escape\_formulas property to prevent Excel Injection, also, known as formula injection.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Escape Excel Formulas \[Updated in Security Center 1.3\]

Use the **glide.export.escape\_formulas** property to prevent Excel Injection, also, known as formula injection.

Excel injection occurs when websites embed untrusted entries inside Excel files. When you use a spreadsheet application such as Microsoft Excel, or LibreOffice Call, to open a file, any cells starting with +, -, =, or @ are interpreted as a formula. When you set the **glide.export.escape\_formulas** property to **true**, string values starting with +, -, =, or @ are prepended with a single apostrophe when you export to CSV, XLS, or XLSX files.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.export.escape\_formulas**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Validation, sanitization, and encoding](validation-sanitization-encoding.md)|
|Purpose|To prevent application against the Excel or formula injection.|
|Recommended value|true|
|Default value|false|
|Security risk rating|6.5|
|Functional impact|Maliciously crafted formulas can be used for hijacking the user's computer by exploiting vulnerabilities in the spreadsheet software.|
|Security risk|\(Moderate\) Malicious formulae pose a risk even when the embedding spreadsheet doesn't contain any sensitive information, as they can be used to compromise the viewer's computer.|
|Workaround|As an alternative consider stripping all trailing white spaces where possible, and limiting all client-supplied data to alpha-numeric characters.|
|References|[Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

