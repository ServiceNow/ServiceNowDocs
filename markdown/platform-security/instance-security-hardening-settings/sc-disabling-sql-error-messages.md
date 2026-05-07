---
title: Disable SQL error messages
description: Use the glide.db.loguser property to disable SQL error messages from rendering in a browser.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Disable SQL error messages

Use the **glide.db.loguser** property to disable SQL error messages from rendering in a browser.

If **glide.db.loguser** is not set to the recommended value of **false**, then sensitive server-side error messages could be displayed to end-users. Error messages can include stack traces and information about the structure of the database that could provide an attacker the knowledge needed to perform successful SQL Injection should the preconditions exist.

Ensure that the **glide.db.loguser** system property is set to **false**.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.db.loguser**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Error handling and logging](sc-error-handling-logging.md)|
|Purpose|To disable SQL error messages from displaying within the browser.|
|Type|Boolean|
|Recommended value|false|
|Default value|true|
|Security risk rating|3.1|
|Functional impact|This remediation disables rendering of SQL error messages. There is no impact to any functionality.|
|Security risk|\(Medium\) No sensitive SQL information that could help an attacker should appear as a part of error message on a web page.|

## More information

<table id="table_ajc_b43_3kc"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.db.loguser**

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.1
-   CVSS rating: Low
-   Security risk details: Messages can include stack traces and database structure details, which attackers can leverage to craft targeted SQL injection attacks if other vulnerabilities exist. Exposing internal error information increases the risk of exploitation.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)

