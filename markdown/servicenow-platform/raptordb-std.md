---
title: RaptorDB Standard and RaptorDB Professional
description: RaptorDB Standard is the ServiceNow database that supports the ServiceNow AI Platform. It optimizes transactional performance, so your organization can support more users, workflows, and data on a single platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/raptordb-std.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [RaptorDB Standard, database, PostgreSQL]
breadcrumb: [Explore, RaptorDB Professional, Extend ServiceNow AI Platform capabilities]
---

# RaptorDB Standard and RaptorDB Professional

RaptorDB Standard is the ServiceNow database that supports the ServiceNow AI Platform. It optimizes transactional performance, so your organization can support more users, workflows, and data on a single platform.

RaptorDB Standard underpins ServiceNow AI Platform core services, applications, and data.

**Note:** The roll-out of RaptorDB Standard is not tied to your organization's upgrade to Brazil. Contact your account team for more information.

RaptorDB Standard is built on PostgreSQL with ServiceNow optimizations for ServiceNow AI Platform workloads.

RaptorDB Professional adds analytical processing to the same transactional foundation. It introduces column-store indexing and parallel query processing, supports shared and replicated instance topologies, and is required for Live Connect and Live Archive. The following table compares the two tiers.

## RaptorDB Standard vs. RaptorDB Professional

|Capability|RaptorDB Standard|RaptorDB Professional|
|----------|-----------------|---------------------|
|PostgreSQL foundation|Yes|Yes|
|Optimized for ServiceNow AI Platform workloads|Yes|Yes|
|Column-store index and parallel query processing|No|Yes|
|Hybrid transactional-analytical processing \(HTAP\)|No|Yes|
|Live Connect|No|Yes|
|Live Archive|No|Yes|
|Shared and replicated instance topologies|No|Yes|
|Self-hosted deployment|No|Yes|

**Related topics**  


[Create a table index](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_CreateCustomIndex.md)

[Access your ServiceNow data using Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md)

[Live Archive with RaptorDB Professional V2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/data-archiving-with-raptordb-professional-v2.md)

