---
title: Health Log Analytics severity mapping
description: Health Log Analytics \(HLA\) uses common severity values to identify severity labels in the Source Type Structure.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Health Log Analytics, HLA, severity words, severity values, log severity]
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Health Log Analytics severity mapping

Health Log Analytics \(HLA\) uses common severity values to identify severity labels in the Source Type Structure.

The **Log severity mapping** table illustrates how HLA identifies severity words from raw logs \(shown in the left column\), maps them to its own severity values \(middle column\), and then presents them in Event Management alerts \(right column\).

|Raw log severity|HLA log severity|Event Management alert severity|
|----------------|----------------|-------------------------------|
|TRACE|TRACE|Keywords-based|
|VERBOSE|TRACE|Keywords-based|
|FINE|TRACE|Keywords-based|
|FINER|TRACE|Keywords-based|
|FINEST|TRACE|Keywords-based|
|DEBUG|DEBUG|Keywords-based|
|DBG|DEBUG|Keywords-based|
|CONFIG|DEBUG|Keywords-based|
|INFORMATIONAL|INFORMATIONAL|Keywords-based|
|INFORMATION|INFORMATIONAL|Keywords-based|
|INF|INFORMATIONAL|Keywords-based|
|INFO|INFORMATIONAL|Keywords-based|
|UNKNOWN|UNKNOWN|Keywords-based|
|NOTICE|NOTICE|LOW|
|NOTIFICATION|NOTICE|LOW|
|WARNING|WARNING|MEDIUM|
|WARN|WARNING|MEDIUM|
|ERROR|ERROR|HIGH|
|ERR|ERROR|HIGH|
|CRITICAL|CRITICAL|CRITICAL|
|CRIT|CRITICAL|CRITICAL|
|FAT|CRITICAL|CRITICAL|
|FATAL|CRITICAL|CRITICAL|
|SEVERE|CRITICAL|CRITICAL|
|ALERT|ALERT|CRITICAL|
|EMERGENCY|EMERGENCY|CRITICAL|
|EMER|EMERGENCY|CRITICAL|

**Note:** If your raw log contains numerical severities or unrecognized words, map these values to the HLA Log Severity column by creating a conditional statement using the JS function in the Source Type Structure. For more information, see [Source type structure adjustment](../concept/hla-source-type-structure-adjustment.md).

**Parent Topic:**[Health Log Analytics reference](../concept/hla-reference.md)

