---
title: Common AI Data Explorer issues and fixes
description: Use Query Generation logs to inspect failed or incorrect queries and identify common issues with AI Data Explorer responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/ai-data-explorer-troubleshooting.html
release: australia
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 2
keywords: [troubleshooting, Query Generation logs, AI Data Explorer, semantic layer]
breadcrumb: [Configure, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Common AI Data Explorer issues and fixes

Use Query Generation logs to inspect failed or incorrect queries and identify common issues with AI Data Explorer responses.

Go to **Query Generation** &gt; **Administration** &gt; **Logs** to inspect failed or incorrect queries.

1.  Find the entry by user, date, or utterance.
2.  Check **Semantic Entities/Dimensions/Segments Count**
3.  Open **Query Constitutor Output** to see what was selected.
4.  Compare with **Semantic Filter Result** for raw semantic matches.

|Symptom|Likely cause|Fix|
|-------|------------|---|
|"Unable to understand" response|System cannot find a matching table|Improve entity description; rephrase with table name; verify AI search is running; verify that all Indexed Sources are fully processed.|
|Wrong table selected|Similar table names, no disambiguation|Add semantic usage instructions to differentiate.|
|Wrong table selected \(permissions\)|User lacks read access to the intended table or fields.|Verify and grant table and field read ACLs for the intended data.|
|"Error accessing table data" or "Scope access not granted" response|Some data is in protected application scopes that AI Data Explorer cannot access.|Create ACLs granting access to the scope for AI Data Explorer. Approve the subsequently generated Restricted Caller Access \(RCA\) records. For more information, see [Enabling access to protected scope applications for AI Data Explorer and Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/enable-aide-secure-scope-apps.md).|
|Missing field in results|Dimension turned off, unclear label, or field not in semantic layer|Check dimension is active; update label.|
|Related fields not pulled in|Referenced table missing from semantic layer or reference dimension turned off|Add and enable the referenced table entity; enable the reference dimension.|
|Wrong filter applied|Bad segment match|Fix segment name and description; disable the segment.|
|No filter when expected|No matching segment; phrasing too vague|Create a manual segment; rephrase question.|
|Segment from report is wrong|Auto-generated segment has stale or irrelevant filter|Disable the report segment source or the specific segment.|

**Parent Topic:**[Configure AI Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/configure-now-ass-explorer.md)

**Related topics**  


[Query Generation Health page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/querygen-health-page.md)

[Tuning the semantic layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/semantic-layer-tuning-overview.md)

[Query Generation logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/query-generation-logs.md)

[Configure record level analysis in AI Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/record-level-analysis.md)

[Roles and tables installed with AI Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/tables-now-assist-explorer.md)

