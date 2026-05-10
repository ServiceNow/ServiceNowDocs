---
title: Understanding Dictionary attributes for Antivirus Scanning
description: Dictionary attributes alter the behavior of the table or element that the dictionary record describes. As an administrator, you can set the values of dictionary attributes to modify the behavior of the default Antivirus Scanning configuration.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Antivirus Scanning]
---

# Understanding Dictionary attributes for Antivirus Scanning

Dictionary attributes alter the behavior of the table or element that the dictionary record describes. As an administrator, you can set the values of dictionary attributes to modify the behavior of the default Antivirus Scanning configuration.

|Name|Value|Target element|Description|
|----|-----|--------------|-----------|
|Exclude\_from\_antivirus\_scan|true/false|any table|If true, file attachments on the table are excluded from the antivirus scan. See [Configuring Antivirus Scanning](../task/configure-antivirus-protection.md)|
|Supress\_antivirus\_email\_notification|true/false|any table|If true, stops sending Platform-generated email notifications when a potentiality-infected file is identified.|
|Suppress\_antivirus\_ui\_notification|true/false|any table|If true, stops Platform-generated UI notifications when a potentially-infected file is identified.|

**Related topics**  


[Altering tables and fields using dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md)

