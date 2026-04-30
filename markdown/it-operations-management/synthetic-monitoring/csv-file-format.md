---
title: CSV file format
description: CSV files must include a header row followed by data rows.
locale: en-US
release: yokohama
product: Synthetic Monitoring
classification: synthetic-monitoring
topic_type: reference
last_updated: "2026-02-24"
reading_time_minutes: 1
breadcrumb: [Synthetic monitoring reference, Synthetic monitoring, ITOM AIOps, IT Operations Management]
---

# CSV file format

CSV files must include a header row followed by data rows.

## CSV header

```csv
name,method,description,interval,cmdb_ci,enabled,should_create_alert,alert_severity,locations,headers,alert_tags,valid_http_code_type,valid_http_code,max_latency_ms,query_string,credential,body,body_condition,parent_service_sys_id,support_group_sys_id
```

## CSV example

```csv
name,method,description,interval,cmdb_ci,enabled,should_create_alert,alert_severity,locations,headers,alert_tags,valid_http_code_type,valid_http_code,max_latency_ms,query_string,credential,body,body_condition,parent_service_sys_id,support_group_sys_id
"My Monitor","GET","Health check",1,"0bd58579ff1232109a07ffffffffff72",true,true,1,"10eb9e1cffa2f2109a07ffffffffff27","[]","{}","equals","200","5000","","","","","81d847959f030200fe2ab0aec32e7031","2156c3a80b982300cac6c08393673a7e"
```

## CSV special formatting

-   **locations**: Pipe-separated sys\_ids \(example, `loc1_sys_id|loc2_sys_id`\)
-   **headers**: JSON array string \(example, `[{"name":"Authorization","value":"Bearer xxx"}]`\)
-   **alert\_tags**: JSON object string \(example, `{"env":"prod","team":"api"}`\)
-   **body\_condition**: Colon-separated type:expression \(example, `jsonpath:$.status`\)
-   **Boolean values**: `true`, `false`, `1`, `0`, `yes`, `no`

**Parent Topic:**[Synthetic monitoring reference](synthetic-monitoring-reference.md)

