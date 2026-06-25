---
title: Automated cleanup of duplicate records from same source
description: The TISC application includes automated logic to manage records that were received repeatedly from the same source. When identical or matching records are ingested multiple times from same source, the application ensures that the most recent record remains active while previously stored instances are identified as duplicates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/duplicate-handling-of-records-from-the-same-source.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [tisc, dupilcate records, observable, indicator, deduplication, object]
breadcrumb: [TISC Data archival and cleanup, Use, Threat Intelligence Security Center, Security Operations]
---

# Automated cleanup of duplicate records from same source

The TISC application includes automated logic to manage records that were received repeatedly from the same source. When identical or matching records are ingested multiple times from same source, the application ensures that the most recent record remains active while previously stored instances are identified as duplicates.

## Impact of duplicate records

When duplicate records from the same source are retained in the application:

-   The deduplication jobs must evaluate a larger number of records during execution.
-   Increased record volume can extend job runtime.
-   Processing latency may occur as the system identifies and resolves redundant entries.

Table cleaners are implemented for the Observable Source \[sn\_sec\_tisc\_observable\_source\], Indicator Source \[sn\_sec\_tisc\_indicator\_source\], and Object Source \[sn\_sec\_tisc\_object\_source\] tables.

These cleaners remove records from the respective tables based on the following condition.

Records where the processing **Status** is set to **Duplicate** and **Duplicate of Record from Same Source** flag is set to **true** and the record was last updated more than 7 days ago.

Navigate to **System Maintenance** &gt; **Table Cleanup** view and manage table cleaners.

**Related topics**  


[Observables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/observables.md)

[Indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/indicator.md)

[TISC Data Processing Functional Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-data-processing-functional-flow.md)

[TISC Data archival and cleanup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/data-archival-process.md)

