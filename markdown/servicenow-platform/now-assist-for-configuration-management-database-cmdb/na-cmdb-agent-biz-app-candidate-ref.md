---
title: Business application candidate agent reference
description: Reference information for the Business application candidate agent, including system properties, configuration limits, table names, role requirements, and operational constraints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-biz-app-candidate-ref.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 4
keywords: [system properties, configuration, limits, reference, Business application candidate agent, ServiceNow Otto for CMDB]
breadcrumb: [Reference, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Business application candidate agent reference

Reference information for the Business application candidate agent, including system properties, configuration limits, table names, role requirements, and operational constraints.

## System properties

All agent configuration properties use the prefix `sn_sm_gen_ai.business_app_matching.*`. You can configure the properties to control job behavior, filtering, performance, and AI confidence thresholds.

Scope and filtering

The following properties control which app services and business applications are included in processing.

|Property|Default|Description|
|--------|-------|-----------|
|`supported_app_service_classes`|\(empty\)|Comma-separated list of app service subclasses to include. Empty \(with empty unsupported list\) means all classes are included.|
|`unsupported_app_service_classes`|\(empty\)|Comma-separated list of app service subclasses to exclude.|
|`app_service_skip_criteria`|`operational_status=2`|Encoded query — app services that match this criterion are skipped during processing. Default skips inactive services.|
|`business_app_skip_criteria`|`operational_status=2`|Encoded query — business applications that match this criterion are excluded from matching. Default excludes inactive applications.|

Job cadence

The following properties control how frequently the Data Synchronization and Processing jobs run.

|Property|Default|Description|
|--------|-------|-----------|
|`sync_interval_in_seconds`|604800 \(7 days\)|How often the Data Sync job re-runs after completing a full synchronization cycle.|
|`batch_interval_in_seconds`|3600 \(1 hour\)|How often the Processing job re-fires after completing a batch of recommendations.|
|`retry_interval_in_seconds`|1800 \(30 min\)|How often the Processing job polls while waiting for synchronization to finish or AI Search indexing to complete.|

Processing tuning

The following properties tune AI inference and recommendation generation.

|Property|Default|Description|
|--------|-------|-----------|
|`batch_size`|1000|Number of app services processed per job execution. Hard cap: 10,000. Adjust this setting for performance on instances with very large numbers of app services.|
|`similar_max_entries`|100|Maximum number of similar app service results returned by AI search per inference. Limits AI context and processing time.|
|`negative_feedback_max_entries`|50|Maximum number of rejected recommendations used as negative feedback per inference. Limits the number of past rejections the AI considers when learning.|

Confidence thresholds

The following properties control the minimum confidence levels required to generate and auto-accept recommendations.

<table id="table_confidence_thresholds"><thead><tr><th>

Property

</th><th>

Default

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`business_app_confidence_minimum_rating`

</td><td>

3 \(Medium\)

</td><td>

Minimum AI confidence rating \(1=Very Low, 5=Very High\) required to create a recommendation. Recommendations with confidence lower than this threshold are silently skipped. Increase this value to see only high-confidence recommendations; decrease to see more candidates.

</td></tr><tr><td>

`relationship_confidence_minimum_rating`

</td><td>

3 \(Medium\)

</td><td>

Minimum confidence rating required to create a CI relationship candidate when a business application match is found. Affects which related application service links are proposed.

</td></tr><tr><td>

`auto_accept_confidence_minimum_rating`

</td><td>

\(empty\)

</td><td>

If set, recommendations where all confidence scores meet or exceed this value are automatically accepted without human review. Leave empty to require manual review for all recommendations. **Tip:** Use this setting only when you feel confident after many manual reviews.

</td></tr></tbody>
</table>User group context

The following property controls whether the AI includes additional user and group context when analyzing app services.

|Property|Default|Description|
|--------|-------|-----------|
|`use_all_user_groups_info`|false|When true, the agent gathers all user group and user values from the app service record \(expanding user fields into their assignment groups\) and includes them in the AI prompt. When false, only the `managed_by_group` value is used. Enable this property for richer context when your services have varied ownership fields populated.|

## Operational constraints

|Limit|Value|
|-----|-----|
|Maximum supported app services|250,000|
|Recommendation retention|2 years|

If your app service count exceeds 250,000, the synchronization job deactivates itself and sets its state to `unsupported`. This indicates that your data volume exceeds the maximum supported scale. If this occurs, contact support for guidance on data partitioning or alternative approaches.

Recommendations older than two years are automatically removed from the system to manage storage and improve performance.

## Table references

The agent uses the following tables in the CMDB and internal processing system:

|Table Name|Purpose|
|----------|-------|
|`sn_sm_gen_ai_app_service_processing`|Work queue for app service processing jobs. Rows advance through states: ready → in\_progress → processed.|
|`sn_sm_gen_ai_processing_entry`|Key/value run state table. Stores `data_synchronization_state` and per-batch processing statistics.|
|`sn_sm_gen_ai_business_app_recommendation`|Recommendation records for human review. Records are numbered with a `BIZ` prefix. Stores proposed business applications, confidence ratings, and related app service candidates.|

## Role requirements

Access to all Business application candidate agent tables, forms, and configuration requires the `itil` role. This role is required to:

-   Activate and deactivate scheduled jobs
-   Configure system properties
-   View recommendations and work queue entries
-   Accept or reject recommendations
-   Create or modify business application records and relationships

**Parent Topic:**[ServiceNow Otto for CMDB reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-reference.md)

**Related topics**  


[Activate the Business application candidate agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-biz-app-candidate-act.md)

[Review Business application candidate agent recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-biz-app-candidate-rec.md)

