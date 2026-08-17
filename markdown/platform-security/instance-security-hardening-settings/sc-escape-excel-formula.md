---
title: Escape Excel formulas \[Updated in Security Center 1.3\]
description: Use the glide.export.escape\_formulas property to prevent Excel Injection, also, known as formula injection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-escape-excel-formula.html
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-07-30"
reading_time_minutes: 1
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Escape Excel formulas \[Updated in Security Center 1.3\]

Use the **glide.export.escape\_formulas** property to prevent Excel Injection, also, known as formula injection.

Prevent malicious formula execution in Excel by escaping formulas in exported files. Excel injection occurs when websites embed untrusted entries inside Excel files. When you open a file in Microsoft Excel or LibreOffice Calc, any cells starting with +, -, =, or @ are treated as formulas. Malicious formulas can compromise your computer through code execution, even if the spreadsheet contains no sensitive data.

Set the **glide.export.escape\_formulas** system property to **true** to escape these formulas from executing.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.export.escape\_formulas**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Validation, sanitization, and encoding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/validation-sanitization-encoding.md)|
|Purpose|To prevent application against the Excel or formula injection.|
|Recommended value|true|
|Default value|true|
|Security risk rating|6.4|
|Functional impact|Maliciously crafted formulas can be used for hijacking the user's computer by exploiting vulnerabilities in the spreadsheet software.|
|Security risk|\(Moderate\) Malicious formulae pose a risk even when the embedding spreadsheet doesn't contain any sensitive information, as they can be used to compromise the viewer's computer.|
|Workaround|As an alternative consider stripping all trailing white spaces where possible, and limiting all client-supplied data to alpha-numeric characters.|
|References|[Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md)|

To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Parent Topic:**[Validation, sanitization, and encoding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/validation-sanitization-encoding.md)

