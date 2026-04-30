---
title: Enhancing the CMDB with host data Health Log Analytics found in logs
description: When Health Log Analytics streams logs, it extracts host data from the log events. If host data is discovered that doesn't match the information in the Configuration Management Database \(CMDB\), the system creates a configuration item \(CI\) candidate for you to review based on the data it found in the logs.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer HLA, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Enhancing the CMDB with host data Health Log Analytics found in logs

When Health Log Analytics streams logs, it extracts host data from the log events. If host data is discovered that doesn't match the information in the Configuration Management Database \(CMDB\), the system creates a configuration item \(CI\) candidate for you to review based on the data it found in the logs.

After reviewing a CI candidate, you can choose to either add it to the CMDB or dismiss it as irrelevant. The **Log-Based CI Candidates** table lists all CI candidates that Health Log Analytics has created, sorted by system update time. The **Operation** column shows the suggested action to take on each CI candidate. You are automatically notified when there are new CI candidates for your consideration. For more information, see [Add log-based CIs to the CMDB in Health Log Analytics](../task/hla-cmdb-enrich.md).

For a description of the related system properties, see the "logsourceinfo \(CMDB\)" section in the [HLA System Properties \[KB0869842\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0869842) article in the Now Support Knowledge Base.

This feature is supported in the Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). You can use it on the ServiceNow AI Platform using the Rome Patch 6 release \(scheduled to be released on January 27, 2022\) or later.

-   **[Add log-based CIs to the CMDB in Health Log Analytics](../task/hla-cmdb-enrich.md)**  
Keep the Configuration Management Database \(CMDB\) updated with host data Health Log Analytics discovered in your logs by adding log-based configuration items \(CIs\) to the database.

**Parent Topic:**[Administering Health Log Analytics](hla-administer.md)

