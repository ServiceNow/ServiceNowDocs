---
title: Enable export debug logging
description: When the property glide.export.debug is true, the instance logs export processing including database query time and the time taken to write data to the file.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exporting data, Tables and data, Configure core features, Administer]
---

# Enable export debug logging

When the property glide.export.debug is true, the instance logs export processing including database query time and the time taken to write data to the file.

When the property glide.export.debug is true, the instance logs export processing including database query time and the time taken to write data to the file. Debug logs are indicated by the text Export API. Prolonged use of this property can affect performance, so it is best to use it while debugging export processing, and then set the property back to false.

```
7/17/14 15:53:48 (500) EB39A310EB022100C46AC2EEF106FED9 Maximum record count for this instance is: 10000: , request is for: 0 Cap the Record count to Maximum Record Count
07/17/14 15:53:48 (522) EB39A310EB022100C46AC2EEF106FED9 Export API - ExportProcessor : Processing EXCEL export request, ExportParameters:TableName=incident, Query=active=true, Limit=10000, SortBy=null
07/17/14 15:53:48 (527) EB39A310EB022100C46AC2EEF106FED9 Export API - ExportProcessor : Export using background thread
07/17/14 15:53:48 (528) EB39A310EB022100C46AC2EEF106FED9 #748 /poll_processor.do -- total transaction time: 0:00:03.357, total wait time: 0:00:00.000, session wait: 0:00:00.000, semaphore wait: 0:00:00.000, source: 0:0:0:0:0:0:0:1%0 
07/17/14 15:53:48 (550) SYSTEM Enabling elevated role: security_admin
07/17/14 15:53:48 (588) SYSTEM Export API - ExcelExporter : 29 rows retrieved from database duration_milliseconds=2
07/17/14 15:53:49 (534) NONE New transaction EB39A310EB022100C46AC2EEF106FED9 #751 /poll_processor.do
07/17/14 15:53:49 (544) EB39A310EB022100C46AC2EEF106FED9 #751 /poll_processor.do Parameters -------------------------
    sys_action=poll
    sysparm_processor=poll_processor
    job_id=a61a2314eb022100c46ac2eef106fe0a
07/17/14 15:53:49 (547) EB39A310EB022100C46AC2EEF106FED9 #751 /poll_processor.do -- total transaction time: 0:00:00.013, total wait time: 0:00:00.000, session wait: 0:00:00.000, semaphore wait: 0:00:00.000, source: 0:0:0:0:0:0:0:1%0 
07/17/14 15:53:49 (740) SYSTEM Export API - ExcelExporter : Rows written to file duration_milliseconds=1150
```

