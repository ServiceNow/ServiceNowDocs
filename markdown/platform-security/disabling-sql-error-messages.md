---
title: Disabling SQL error messages \(instance security hardening\)
description: Use the glide.db.loguser property to disable SQL error messages from rendering in a browser.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Logging, auditing, and errors, Logs, Platform Security]
---

# Disabling SQL error messages \(instance security hardening\)

Use the **glide.db.loguser** property to disable SQL error messages from rendering in a browser.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|glide.db.loguser|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Configurable in Instance Security Center|No|
|Purpose|To disable SQL error messages from displaying within the browser.|
|Type|true\|false|
|Recommended value|false|
|Functional impact|\(Low\) This remediation disables rendering of SQL error messages. There is no impact to any functionality.|
|Security risk|\(Medium\) No sensitive SQL information that could help an attacker should appear as a part of error message on a web page.|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Logging, auditing, and errors \(instance security hardening\)](logging-auditing-errors-instance-security-hardening.md)

