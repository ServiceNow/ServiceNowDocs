---
title: Qualys API field mappings
description: Lists the additional fields introduced in newer Qualys API versions and their corresponding mappings in ServiceNow tables.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: reference
last_updated: "2026-03-02"
reading_time_minutes: 1
breadcrumb: [REST messages, Qualys, Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Qualys API field mappings

Lists the additional fields introduced in newer Qualys API versions and their corresponding mappings in ServiceNow tables.

When Qualys integrations are upgraded to newer API versions, the API responses include additional fields. The following table lists these fields and shows where they map in ServiceNow.

|Integration|Table name|ServiceNow field|Qualys field|
|-----------|----------|----------------|------------|
|Host Detection|sn\_vul\_entry|Qualys\_vulnerability\_detection\_sources \(Qualys scope\)|VULNERABILITY\_DETECTION\_SOURCES|
|Host List|sn\_sec\_cmn\_src\_ci|source\_data|\{ VM\_AUTH\_INSUFFICIENT\_PRIVILEGE: &lt;value&gt;\} \(appended to existing values\)|
|PC Controls|sn\_vulc\_test|active|IS\_ACTIVE|
|Qualys PC Policies|sn\_vulc\_policy|active|status|
|Qualys PCRS Test Results|sn\_sec\_cmn\_src\_ci|source\_data|CloudMetaData|

