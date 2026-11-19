---
title: Exploring RaptorDB Professional
description: RaptorDB Professional is a hybrid transactional-analytical processing database that enables Live Archive and Live Connect capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/exploring-raptordb-professional.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [RaptorDB Professional, HTAP, Live Archive, Live Connect, data interface]
breadcrumb: [RaptorDB Professional, Extend ServiceNow AI Platform capabilities]
---

# Exploring RaptorDB Professional

RaptorDB Professional is a hybrid transactional-analytical processing database that enables Live Archive and Live Connect capabilities.

## RaptorDB Professional capabilities

RaptorDB Professional is a hybrid transactional-analytical processing \(HTAP\) database built on PostgreSQL. A single engine runs transactional and analytical workloads on the same data, so reports, dashboards, and workflows query current operational records without exporting data to an external system.

It enables two independent capabilities: Live Archive, which offloads inactive records to object storage, and Live Connect \(formerly known as SQL API\), which provides read-only SQL access to authorized tables through ODBC and JDBC drivers. Both require RaptorDB Professional and operate at the data access layer.

## RaptorDB Professional users

|User|Description|
|----|-----------|
|Platform administrator|Understands what archive tables are, configures ACLs for archive data access, and verifies Live Connect access before handing off to analysts.|
|Data analyst|Understands why archive tables behave differently from live tables before writing queries and confirms that Live Connect access is in place.|
|Evaluator|Compares RaptorDB Standard and RaptorDB Professional capabilities and determines which capabilities are available in each tier before requesting an entitlement.|

## Benefits

All users of an instance running RaptorDB Professional receive the following benefits. The Users column identifies who typically configures or acts on each feature.

|Benefit|Feature|Users|
|-------|-------|-----|
|Run analytical queries against operational data without exporting it to an external system.|HTAP engine|All users|
|Run analytical queries faster on large tables.|Column-store index and parallel query processing. For more information, see [Create a table index](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_CreateCustomIndex.md).|All users|
|Reduce the primary storage footprint, for leaner backups and faster clone operations.|Live Archive|Platform administrator|
|Query archived records without restoring them to primary tables.|Live Archive|Data analyst, platform administrator|
|Query ServiceNow data from existing SQL and business intelligence tools, with no data replication.|Live Connect|Data analyst|
|Deploy across shared, replicated, and self-hosted configurations.|Advanced instance topology|Platform administrator|

**Note:** Data Snapshots requires RaptorDB Professional. For more information, see [Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/multi-level-breakdowns.md).

## What to explore next

-   [Requirements for querying archive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/working-with-archive-data.md)
-   [Archive data query examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/archive-data-query-examples.md)
-   [Archive table schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/archive-table-schema.md)

