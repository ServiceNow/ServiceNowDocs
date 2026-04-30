---
title: Restrict downloadable MIME types \[Updated in Security Center 1.3 and 2.0\]
description: The glide.ui.attachment.download\_mime\_types property will force the specified list of dangerous file types to be downloaded to the client and not viewed inline in the browser.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-02-12"
reading_time_minutes: 2
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Restrict downloadable MIME types \[Updated in Security Center 1.3 and 2.0\]

The **glide.ui.attachment.download\_mime\_types** property will force the specified list of dangerous file types to be downloaded to the client and not viewed inline in the browser.

If the property **glide.ui.attachment.force\_download\_all\_mime\_types** is set to true, then the **glide.ui.attachment.download\_mime\_types** property will be overridden so that all MIME types will be downloaded rather than rendered by the browser. For example, downloading text/html forces an HTML file to be downloaded to the client as a file rather than viewed inline in the browser, preventing a XSS attack. XSS can lead to easily attained privilege escalation to higher roles such as admin where more lateral movement can be taken.

New remediation: Ensure the property **glide.ui.attachment.force\_download\_all\_mime\_types** is set to true. If the property does not exist in the sys\_properties table, the default value is false.

**Note:** The security\_admin role is required to edit the property.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.ui.attachment.download\_mime\_types**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Purpose

</td><td>

Maintaining the list properly of dangerous file types that cannot be viewed in the browser will prevent cross site scripting attacks \(XSS\).

</td></tr><tr><td>

Recommended value

</td><td>

List of applicable MIME types or the recommended value: `text/html,image/svg,image/svg+xml,application/xml`

</td></tr><tr><td>

Default value

</td><td>

List of applicable MIME types for the default value: `text/html,image/svg,image/svg+xml,application/xml`

</td></tr><tr><td>

Configuration type

</td><td>

String: any comma separated values of application mime types.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces performance of validation checks before performing an action when you click an attachment in a ServiceNow AI Platform application. There is no potential impact, but the user experience is altered.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) Attackers can abuse MIME types and place unintended script content in the attachment on the victim's side to capture sensitive information. The ability to have XSS can lead to easily attained privilege escalation to higher roles, such as admin, where more lateral movement can be taken.In the current context, populate the property with a list of comma-separated attachment MIME types that should not render inline in the browser.

</td></tr><tr><td>

Security risk rating

</td><td>

6.4

</td></tr><tr><td>

Related properties

</td><td>

-   **glide.ui.attachment.force\_download\_all\_mime\_types**
-   **glide.ui.attachment.tables\_ignore\_force\_download**

</td></tr><tr><td>

References

</td><td>

[Define restricted downloadable MIME types \[Updated in Security Center 1.3, 1.5, and 2.0\]](sc-downloadable-mime-types.md).

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

