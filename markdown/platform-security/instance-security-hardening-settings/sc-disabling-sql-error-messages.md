---
title: Disable SQL Error Messages \[Updated in Security Center 1.3 and 1.5\]
description: Use the glide.db.loguser property to disable SQL error messages from rendering in a browser.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Disable SQL Error Messages \[Updated in Security Center 1.3 and 1.5\]

Use the **glide.db.loguser** property to disable SQL error messages from rendering in a browser.

If **glide.db.loguser** is not set to the recommended value of false, then sensitive server-side error messages could be displayed to end-users. Error messages can include stack traces and information about the structure of the database that could provide an attacker the knowledge needed to perform successful SQL Injection should the preconditions exist. As defense in depth, these error messages should not be displayed to the end user.

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

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)

