---
title: Session debug
description: Enable session debugging to display debugging messages in the user interface.Display session debug logs to help diagnose script and application problems.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Debugging scripts, Scripting, API implementation, API implementation and reference]
---

# Session debug

Enable session debugging to display debugging messages in the user interface.

Troubleshooting slow performance with the Session Debug feature.

You can enable all areas for abundant logging on the bottom of each page load, or you can enable each module one by one, for more specific information about what is happening during this session, and specifically, for the previous transaction. Select session debug options under **System Diagnostics** &gt; **Session Debug**. When enabled, session debugging is active during the user session or until disabled. To view debug logs, see [Display debugging logs](c_SessionDebug.md#).

The system provides the following session debugging options.

|Debug option|Description|
|------------|-----------|
|Enable All|Displays all available debugging messages.|
|Disable All|Stops displaying all debugging messages.|
|Debug Business Rule|Displays debugging messages for business rules. If there are business rules from multiple applications affecting a table or record, the system displays which application the business rule comes from.|
|Debug Upgrade|Displays detailed information logged for records processed during the last family-to-family or patch version upgrade session. See [Debug Upgrade](https://www.servicenow.com/docs/access?context=debug-upgrade&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) .|
|Debug Business Rule \(Details\)|Displays debugging messages for business rules and any changes made by business rules. If there are business rules from multiple applications affecting a table or record, the system displays which application the business rule comes from.|
|Debug Log|Displays all log entries.|
|Debug NLQ|Displays debugging messages for Natural Language Query \(NLQ\) queries.|
|Debug Date/Time|Displays Date/Time failures when inputs do not match required formats.|
|Debug SQL|Displays debugging messages for SQL queries.|
|Debug SQL \(Detailed\)|Displays debugging messages for SQL statements and any changes made by SQL statements.|
|Debug Security|Displays debugging messages for access controls. If there are access controls from multiple applications affecting a table or record, the system displays which application the access controls comes from.|
|Debug Escalations|Displays debugging messages for SLA and SLO escalations.|
|Debug AI Search|Displays debugging messages for AI Search.|
|Debug Metric Statistics|Displays an aggregate view of performance data \(slow transactions, scripts, queries, events, and mutexes\). These aggregate metrics are sorted by transaction, to help identify items that affect page performance.|
|Debug Text Search|Displays debugging messages for search result relevance and indexing.|
|Debug UI Policies|Displays debugging messages for UI policies.|
|Disable UI Policies Debug|Stops displaying debugging messages for UI policies.|
|Debug UI Macro|Displays the start and end of the UI Macro in the DOM as HTML comments. The comments consist of table name and UI macro name.|
|Disable Debug UI Macro|Stops displaying the start and end of the UI Macro in the DOM as HTML comments.|
|Debug Data Policies|Displays debugging messages for data policies.|
|Debug Quotas|Displays debugging messages for transaction quotas.|
|Debug Homepage Render|Displays debugging messages for homepages.|
|Debug Scopes|Displays debugging messages for entering or exiting application scopes when running script objects.|

**Parent Topic:**[Debugging scripts](script-debug-overview.md)

## Display debugging logs

Display session debug logs to help diagnose script and application problems.

### Before you begin

Role required: none

### Procedure

1.  Navigate to **All** &gt; **Session Debug** and select **Enable All**.

2.  Under **Session Debug**, select **Debug Log**.

    The Debug log displays.


